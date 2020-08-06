---
description: Saisissez le nombre de publications et de commentaires pour certaines collections à afficher sur vos pages d’index.
seo-description: Saisissez le nombre de publications et de commentaires pour certaines collections à afficher sur vos pages d’index.
seo-title: Afficher le nombre de commentaires
solution: Experience Manager
title: Afficher le nombre de commentaires
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c2594f919f153d1230b3dc0370f31d64cb698146
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Afficher le nombre de commentaires{#display-comment-count}

Saisissez le nombre de publications et de commentaires pour certaines collections à afficher sur vos pages d’index.

Livefyre vous `CommentCount.js` permet de récupérer le nombre de contenus pour les collections de votre site. Bien que les applications affichent le nombre de commentaires pour la collection actuelle, il peut s’avérer utile de regrouper ces comptes sur l’ensemble de votre site. Cette fonctionnalité est particulièrement utile si vous ne conservez pas le contenu de votre base de données (ou si votre base de données CMS n’est pas synchronisée avec Livefyre).

1. Chargez le code JavaScript.

   Pour l’utiliser `CommentCount.js`, incorporez d’abord le fichier JavaScript dans la `<head>` section de la page ou du modèle dans lequel vous souhaitez l’utiliser.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Liez l’élément HTML.

   Une fois le script chargé, il tente de trouver d’autres éléments sur la page avec un nom de classe de `livefyre-commentcount`. Pour chacun de ces éléments, le script recherchera les attributs `data-lf-site-id` et `data-lf-article-id` HTML et les utilisera pour récupérer le contenu de Livefyre et mettre à jour chaque élément avec la dernière valeur.

   Par exemple, l’élément suivant sera mis à jour :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >Le `CommentCount.js` code recherche une valeur numérique à mettre à jour avec le nombre réel. Veillez à inclure une valeur numérique entre les balises.

   **Exemple 1** (Utilisation de l’URL comme ID d’article) :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Exemple 2** (utilisation d’un système numéroté comme ID d’article) :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurez les options.

   Pour mieux contrôler le remplacement du décompte du contenu, appelez `LF.CommentCount()` et transmettez un objet contenant les options de configuration. Assurez-vous d’appeler la fonction une fois que tous les éléments à remplacer sont dans le modèle DOM. Le meilleur emplacement pour appeler cette méthode est le pied de page. Cela se produit donc lorsque le modèle DOM est chargé, mais avant les événements prêts pour le document et la fenêtre.

   Nous autorisons les options de configuration suivantes :

* **replacer :** Fonction ou Regex utilisée pour remplacer le texte de chaque nombre de contenus.

* **function:** Utilisé pour effectuer le remplacement sur chaque élément. Les arguments de la fonction sont les suivants :

   **element:** Elément HTML en cours de mise à jour.
   **count :** Le contenu est comptabilisé pour cet élément.

* **regex :** Permet de déterminer quelle partie du texte de l’élément doit être remplacée par le nombre.

   **Exemple** :

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
   >Utilisez le replacer pour personnaliser ou internationaliser le message de nombre de commentaires.
