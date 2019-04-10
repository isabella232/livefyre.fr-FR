---
description: Prenez la publication et le nombre de commentaires pour que certaines
  collections s'affichent sur vos pages d'index.
seo-description: Prenez la publication et le nombre de commentaires pour que certaines
  collections s'affichent sur vos pages d'index.
seo-title: Afficher le nombre de commentaires
solution: Experience Manager
title: Afficher le nombre de commentaires
uuid: 0 f 39 b 25 e -11 e 0-4945-be 71-55 fb 4798 b 6 c 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Afficher le nombre de commentaires{#display-comment-count}

Prenez la publication et le nombre de commentaires pour que certaines collections s'affichent sur vos pages d'index.

Livefyre `CommentCount.js` vous permet de récupérer le nombre de contenus pour les collections de votre site. Bien que les applications affichent le nombre de commentaires pour la collection actuelle, la présence de ces comptes syndicés sur votre site peut s'avérer utile. Cette fonctionnalité est particulièrement utile si vous n'avez pas conservé le contenu de votre base de données (ou si votre base de données CMS n'est pas synchronisée avec Livefyre).

1. Chargez le code JavaScript.

   Pour ce faire, `CommentCount.js`incluez d'abord le fichier JavaScript dans la `<head>` section de la page ou du modèle dans lequel vous souhaitez l'utiliser.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Liez l'élément HTML.

   Once the script is loaded, it will attempt to find other elements on the page with a class name of `livefyre-commentcount`. Pour chacun de ces éléments, le script recherche `data-lf-site-id` et utilise des attributs `data-lf-article-id` HTML et les utilise pour récupérer le contenu de Livefyre et mettre à jour chaque élément avec la dernière valeur.

   Par exemple, l'élément suivant serait mis à jour :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {importance = « high »}
   >
   >`CommentCount.js` Le code recherche une valeur numérique à mettre à jour avec le nombre réel. Veillez à inclure une valeur numérique entre les balises.

   **Exemple 1** (Utilisation de l'URL comme ID d'article) :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Exemple 2** (Utilisation d'un système numéroté comme ID d'article) :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configuration des options.

   Pour plus de contrôle sur le remplacement du nombre de contenus, appelez `LF.CommentCount()` et transmettez un objet contenant les options de configuration. Veillez à appeler la fonction après l'utilisation de tous les éléments à remplacer dans le modèle DOM. Le meilleur emplacement pour appeler cette méthode réside dans le pied de page ; il se produit donc lorsque le DOM est chargé, mais avant les événements ready de document et de fenêtre.

   Les options de configuration suivantes sont autorisées :

* **replacer :** Fonction ou Regex utilisée pour remplacer le texte de chaque nombre de contenus.

* **fonction :** Utilisé pour effectuer le remplacement sur chaque élément. Les arguments de la fonction sont les suivants :

   **element :** Elément HTML en cours de mise à jour.
   **count :** Nombre de contenus pour cet élément.

* **regex :** Utilisé pour déterminer la partie du texte de l'élément qui doit être remplacée par le nombre.

   **Exemple**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >Utilisez le replacer pour personnaliser ou internationaliser le message du nombre de commentaires.
