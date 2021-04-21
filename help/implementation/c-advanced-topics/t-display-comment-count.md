---
description: Saisissez le nombre de publications et de commentaires pour certaines collections à afficher sur vos pages d’index.
title: Afficher le nombre de commentaires
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Afficher le nombre de commentaires{#display-comment-count}

Saisissez le nombre de publications et de commentaires pour certaines collections à afficher sur vos pages d’index.

La fonction `CommentCount.js` de Livefyre vous permet de récupérer le nombre de contenus pour les collections de votre site. Bien que les applications affichent le nombre de commentaires pour la collection actuelle, il peut s’avérer utile de regrouper ces comptes sur l’ensemble de votre site. Cette fonctionnalité est particulièrement utile si vous ne conservez pas le contenu de votre base de données (ou si votre base de données CMS n’est pas synchronisée avec Livefyre).

1. Chargez le code JavaScript.

   Pour utiliser `CommentCount.js`, vous devez d’abord incorporer le fichier JavaScript dans la section `<head>` de la page ou du modèle dans lequel vous souhaitez l’utiliser.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Liez l’élément HTML.

   Une fois le script chargé, il tente de trouver d&#39;autres éléments sur la page avec le nom de classe `livefyre-commentcount`. Pour chacun de ces éléments, le script recherche les attributs HTML `data-lf-site-id` et `data-lf-article-id` et les utilise pour récupérer le contenu de Livefyre et mettre à jour chaque élément avec la dernière valeur.

   Par exemple, l’élément suivant sera mis à jour :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >Le code `CommentCount.js` recherche une valeur numérique à mettre à jour avec le nombre réel. Veillez à inclure une valeur numérique entre les balises.

   **Exemple 1**  (Utilisation de l’URL comme ID d’article) :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Exemple 2**  (utilisation d’un système numéroté comme identifiant d’article) :

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurez les options.

   Pour plus de contrôle sur la manière dont le contenu est remplacé, appelez `LF.CommentCount()` et transmettez un objet contenant les options de configuration. Assurez-vous d’appeler la fonction une fois que tous les éléments à remplacer sont dans le modèle DOM. Le meilleur emplacement pour appeler cette méthode est le pied de page. Cela se produit donc lorsque le modèle DOM est chargé, mais avant les événements prêts pour le document et la fenêtre.

   Nous autorisons les options de configuration suivantes :

* **replacer:** Fonction ou Regex utilisé pour remplacer le texte de chaque nombre de contenus.

* **fonction :** permet d’effectuer le remplacement de chaque élément. Les arguments de la fonction sont les suivants :

   **élément:** élément HTML en cours de mise à jour.
   **count :** nombre de contenu pour cet élément.

* **regex :** permet de déterminer quelle partie du texte de l’élément doit être remplacée par le nombre.

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
