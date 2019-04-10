---
description: Découvrez comment générer des jetons Livefyre à l'aide de la langue « C
seo-description: Découvrez comment générer des jetons Livefyre à l'aide de la langue
  « C
seo-title: Création de jetons Livefyre C
solution: Experience Manager
title: Création de jetons Livefyre C
uuid: c 5 e 05625-8550-4 b 51-9211-134600 e 20 ec 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Création de jetons Livefyre C\ # {#creating-livefyre-tokens-c}

Découvrez comment générer des jetons Livefyre à l’aide du langage ``C#``.

Vous pouvez utiliser la documentation héritée et le code à utiliser pour `C#.NET` écrire des méthodes pour créer des jetons.

Pour référencer les bibliothèques officielles de Livefyre, utilisez la bibliothèque [Java](https://github.com/Livefyre/livefyre-java-utils) comme point de départ pour `C#` les développeurs.

Vous pouvez également utiliser la bibliothèque [Node. js](https://github.com/Livefyre/livefyre-nodejs-utils) à partir de la ligne de commande pour générer des jetons de référence et vous familiariser avec la structure de la méthode.

* [Accéder au jeton meta de collection](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Accéder à un jeton authentique](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dépendances {#section_c15_fnh_xz}

* Vous aurez besoin du package [JWT nuget](https://www.nuget.org/packages/JWT) dans votre projet pour générer les jetons.
* Les exemples de code de cette page utilisent le package [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) .

## Collectionmeta Token {#section_dzt_4mh_xz}

Le jeton collectionmeta est transmis à Livefyre lorsque vous incorporez des commentaires sur une page et que notre système dispose des métadonnées nécessaires pour votre nouvelle collection. En outre, vous allez créer un MD 5 `checksum` de ces données que Livefyre vérifie pour vérifier si les métadonnées ont changé. (par exemple, si le titre ou l'URL de votre article a été modifié).

Ce jeton est signé avec votre `Site Key`, qui vous a été fourni par votre gestionnaire de compte Techncial à Livefyre.

Voir également:

* Documents collectionmeta officiels
* [Exemple Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Créez un dictionnaire contenant les métadonnées de la collection. Nous allons uniquement ajouter certains des champs nécessaires à cette étape, car nous souhaitons créer une somme de contrôle de cet objet AVANT d'ajouter l'ID articleid.

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

   * **titre** *requis*: Titre de la collection, généralement le titre de votre article. La longueur max. est de 255 caractères. Ne prend pas en charge les entités html. Veuillez coder des caractères spéciaux à l'aide de UTF -8.
   * **url** *requise*: URL canonique de votre article. Cette fonction est utilisée par les fonctions de partage de commentaires et de synchronisation sociale, ainsi que les liens vers votre article depuis le tableau de bord Admin. Si vous effectuez des tests localement, notez que Livefyre n'accepte pas « localhost » comme domaine.
   * **balises** *facultatives*: Liste de balises séparées par des virgules que vous souhaitez ajouter à la collection dans le tableau de bord Livefyre. Les balises ne peuvent pas contenir d'espaces. Utilisez des traits de soulignement si vous souhaitez qu'un espace apparaisse dans le tableau de bord Admin.
   * **type** *facultatif*: Chaîne indiquant le type de collection à créer. Les valeurs valides sont les suivantes :

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Si elle n'est pas spécifiée, une collection livecomments est créée par défaut.


1. JSON encoder ce dictionnaire et génère une somme de contrôle md 5 de celui-ci.

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

1. Ajoutez l' **ID articleid** au dictionnaire. La **somme de contrôle** ne figure pas dans le jeton collectionmeta, mais doit être envoyée comme paramètre seaprate dans l'objet js convconfig.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **Articleid** *requis*: Identifiant unique de votre collection sur votre site Livefyre. En règle générale, l'ID unique unique utilisé dans votre CMS. (par exemple, votre identifiant de publication wordpress) Cette valeur ne devrait jamais changer. Livefyre identifie les collections uniques par combinaison de siteid et d'articleid.

1. Générez un jeton JWT signé du dictionnaire, à l'aide de la clé du site qui vous a été fournie par Livefyre. Veuillez noter que vous devez spécifier l'algorithme de hachage correct, car le package JWT n'utilise pas la version 256 par défaut.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Jeton utilisateur authentique {#section_g1d_43h_xz}

Le jeton utilisateur authentique est utilisé pour signer un utilisateur dans Livefyre. Lorsqu'un utilisateur se connecte à votre site, le site génère un jeton utilisateur authentique qui est transmis au widget Livefyre sur la page. (Pour plus d'informations sur le processus d'authentification, voir Profils distants.)

Ce jeton nécessite votre nom réseau (network. fyre. co) et est signé avec votre clé réseau qui vous est fourni par votre gestionnaire de compte technique chez Livefyre.

Voir également:

* Documents jeton authentiques officiels
* [Exemple Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

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

   * **domain :** le nom de votre réseau (fourni par Livefyre). par exemple mynetwork. fyre. co
   * **user_ id :** Utilisateur unique - id de l'utilisateur dans le système de profils de votre site. Caractères alphanumériques uniquement (A-Z, a-z, 0-9). Si votre ID d'utilisateur système contient des caractères charaacters non valides, pensez à envoyer Livefyre un hachage md 5 de l'utilisateur - id ou une version codée en base 64. (Indiquez à votre gestionnaire de compte si vous le faites.)
   * **expire :** Date (à la date considérée) que le jeton expire. Ceci doit correspondre à la durée de session des connexions sur votre site, de sorte que l'état connecté de Livefyre reste synchronisé avec l'état connecté de votre site.
   * **display_ name :** Nom d'affichage de l'utilisateur dans votre système de profil, tel qu'il doit être affiché dans le flux de commentaires.

1. Générez un jeton JWT signé du dictionnaire, à l'aide de la clé réseau qui vous a été fournie par Livefyre. Veuillez noter que vous devez spécifier l'algorithme de hachage correct, car le package JWT n'utilise pas la version 256 par défaut.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
