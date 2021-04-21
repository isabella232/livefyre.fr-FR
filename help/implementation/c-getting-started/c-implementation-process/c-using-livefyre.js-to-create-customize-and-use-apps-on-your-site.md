---
title: Incorporer une application
description: Incorporer une application
exl-id: 12f75093-1b4d-4cf1-8593-dbd17ff33872
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Incorporer une application {#embed-an-app}

Ajoutez les applications Livefyre sur vos pages Web à l’aide de la structure de code intégrée Livefyre.js.

Cette documentation est destinée à une audience technique. Pour [des informations non techniques sur les applications](/help/using/c-about-apps/c-about-apps.md).

Cette section décrit la structure de code que vous devrez inclure dans votre modèle de page pour incorporer les applications Livefyre sur votre site.

1. Créez un fichier .html avec un espace réservé Livefyre.

   Créez un fichier .html dans l’éditeur de texte de votre choix. Créez un espace réservé Livefyre `<div>` dans lequel l’application sera incorporée.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Incluez la bibliothèque Livefyre.js.

   Incluez ensuite la bibliothèque Livefyre JS. Placez la référence suivante dans un élément `<script>` de votre élément `<head>`. Ouvrez ensuite votre page dans un navigateur et utilisez l’inspecteur Web de votre navigateur pour confirmer que Livefyre est chargé.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Créez l’application Livefyre.

   Utilisez `Livefyre.require` pour construire des applications de base et des applications SDK en transmettant le ou les packages Livefyre que vous prévoyez d’utiliser.

   1. Créez une application principale.

      Pour créer une application principale (commentaires, blog en direct ou conversation), utilisez la structure suivante :

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Créez une application SDK.

      Pour créer une application SDK telle que Media Wall ou Feed, utilisez la structure suivante :

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      Voir [plus d&#39;informations sur des applications spécifiques](/help/using/c-about-apps/c-about-apps.md). Il est recommandé d’épingler la dernière version majeure du package (qui peut être trouvée via [Livefyre.require](https://cdn.livefyre.com/packages.html)), afin d’éviter des intégrations inattendues rompues.

Suivant : Ajoutez l’authentification sur votre site pour permettre aux utilisateurs de publier des commentaires.
