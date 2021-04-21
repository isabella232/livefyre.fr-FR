---
description: Découvrez comment générer des jetons Livefyre en utilisant le langage "C#".
title: Création de jetons Livefyre `C#'
exl-id: 6360c325-0c3f-4ecb-90f7-951ef4e6f410
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 2%

---

# Création de jetons Livefyre C\# {#creating-livefyre-tokens-c}

Découvrez comment générer des jetons Livefyre à l’aide du langage ``C#``.

Vous pouvez utiliser la documentation héritée et un exemple de code pour utiliser `C#.NET` pour créer des méthodes de création de jetons.

Pour référencer les bibliothèques officielles de Livefyre, utilisez la [bibliothèque Java](https://github.com/Livefyre/livefyre-java-utils) comme point de départ pour les développeurs `C#`.

Vous pouvez également utiliser la [bibliothèque Node.js](https://github.com/Livefyre/livefyre-nodejs-utils) de la ligne de commande pour générer des jetons de référence pour vous-même et pour vous familiariser avec la structure des méthodes.

* [Accéder au méta-jeton de la collection](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Accéder au jeton d’authentification](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dépendances {#section_c15_fnh_xz}

* Vous aurez besoin du [paquet nuget JWT](https://www.nuget.org/packages/JWT) dans votre projet pour générer les jetons.
* Les exemples de code de cette page utilisent le package [JSON Newtonsoft](https://www.nuget.org/packages/newtonsoft.json/).

## CollectionMeta Token {#section_dzt_4mh_xz}

Le jeton CollectionMeta est transmis à Livefyre lorsque vous incorporez des commentaires sur une page et fournit à notre système les métadonnées nécessaires à votre nouvelle collection. En outre, vous allez créer un MD5 `checksum` de ces données, que Livefyre vérifie pour voir si les métadonnées ont changé. (par exemple, si le titre ou l’URL de votre article a été modifié).

Ce jeton est signé avec votre `Site Key`, qui vous a été fourni par votre gestionnaire de compte technique chez Livefyre.

Voir également :

* Documents officiels de collectionMeta Token
* [Exemple de graphique](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Créez un dictionnaire contenant les métadonnées de la collection. Nous allons uniquement ajouter certains des champs nécessaires à cette étape, car nous voulons créer une somme de contrôle de cet objet AVANT d&#39;ajouter l&#39;articleId.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **** *titlerequired* : Titre de la collection, généralement celui de votre article. La longueur maximale est de 255 caractères. Ne prend pas en charge les entités html. Veuillez coder des caractères spéciaux au format UTF-8.
   * **** *obligatoire* : URL canonique de votre article. Il est utilisé par les fonctions de partage de commentaires et de synchronisation sociale, ainsi que les liens vers votre article depuis le tableau de bord d’administration. Si vous testez localement, veuillez noter que Livefyre n&#39;acceptera pas &quot;localhost&quot; comme domaine.
   * **** *tagsfacultative* : Liste de balises séparées par des virgules que vous souhaitez ajouter à la collection dans le tableau de bord Livefyre. Les balises ne peuvent pas contenir d’espaces. Utilisez des traits de soulignement si vous souhaitez qu’un espace s’affiche dans le tableau de bord d’administration.
   * **** *typeoptional* : Chaîne indiquant le type de collection à créer. Les valeurs valides sont :

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`

      Si elle n’est pas spécifiée, une collection LiveComments est créée par défaut.


1. JSON code ce dictionnaire et en génère une somme de contrôle md5.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. Ajoutez **articleId** au dictionnaire. **checksum** ne figure pas dans le jeton collectionMeta, mais doit être envoyé en tant que paramètre distinct dans l’objet js convConfig.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **** *articleIdrequired* : Identificateur unique de votre collection sur votre site Livefyre. En règle générale, l’articleId unique utilisé dans votre CMS. (par exemple, votre ID de publication WordPress) Cette valeur ne doit jamais changer. Livefyre identifie les collections uniques par la combinaison de siteId et articleId.

1. Générez un jeton JWT signé du dictionnaire à l’aide de la clé de site fournie par Livefyre. Veuillez noter que vous devez spécifier l’algorithme de hachage correct, car le paquet JWT n’utilise pas HS256 par défaut.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Jeton d&#39;authentification de l&#39;utilisateur {#section_g1d_43h_xz}

Le jeton d’authentification de l’utilisateur est utilisé pour signer un utilisateur dans Livefyre. Lorsqu’un utilisateur se connecte à votre site, le site génère un jeton d’authentification de l’utilisateur qui est transmis au widget Livefyre sur la page. (Pour plus d’informations sur le processus d’authentification, voir Profils distants.)

Ce jeton requiert votre nom réseau (network.fyre.co) et est signé avec votre clé réseau qui vous est fournie par votre gestionnaire de compte technique chez Livefyre.

Voir également :

* Documents officiels du jeton d&#39;authentification
* [Exemple de graphique](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Créez un dictionnaire contenant les informations nécessaires.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **domaine :** nom de votre réseau (fourni par Livefyre). par exemple, monnetwork.fyre.co
   * **user_id :** identifiant utilisateur unique de l’utilisateur dans le système de profil de votre site. Doit contenir uniquement des caractères alphanumériques (A-Z, a-z, 0-9). Si les identifiants utilisateur de votre système contiennent des caractères non valides, pensez à envoyer un hachage md5 à Livefyre de l’identifiant utilisateur ou une version codée en base 64 de celui-ci. (Indiquez au gestionnaire de compte si vous effectuez cette opération.)
   * **expire : date** d’expiration (en heure) du jeton. Cela doit correspondre à l’heure de session des connexions sur votre site, de sorte que l’état de connexion de Livefyre reste synchronisé avec l’état de connexion de votre site.
   * **nom_affichage : nom d’affichage** de l’utilisateur dans votre système de profil, tel qu’il doit être affiché dans le flux de commentaires.

1. Générez un jeton JWT signé du dictionnaire à l’aide de la clé réseau fournie par Livefyre. Veuillez noter que vous devez spécifier l’algorithme de hachage correct, car le paquet JWT n’utilise pas HS256 par défaut.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
