---
seo-title: Incorporer une application
solution: Experience Manager
title: Incorporer une application
uuid: e75caf0e-04ea-4b04-89ed-fea1183ecf63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Incorporer une application{#embed-an-app}

Ajoutez des applications Livefyre à vos pages Web à l’aide de la structure de code intégré Livefyre.js.

Cette documentation est destinée à un public technique. Pour obtenir des informations [non techniques sur les applications](/help/using/c-about-apps/c-about-apps.md).

Cette section décrit la structure de code que vous devrez inclure dans le modèle de page pour incorporer les applications Livefyre à votre site.

1. Créez un fichier .html avec un espace réservé Livefyre.

   Créez un fichier .html dans l’éditeur de texte de votre choix. Créez un `<div>` élément Livefyre d’espace réservé dans lequel l’application sera intégrée.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Incluez la bibliothèque Livefyre.js.

   Incluez ensuite la bibliothèque Livefyre JS. Placez la référence suivante dans un `<script>` élément de votre `<head>` élément. Ouvrez ensuite votre page dans un navigateur et utilisez l’inspecteur Web de votre navigateur pour confirmer que Livefyre est chargé.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Créez l’application Livefyre.

   Utilisez `Livefyre.require` pour créer des applications de base et des applications SDK en transmettant le ou les packages Livefyre que vous prévoyez d’utiliser.

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

      Voir [plus d’informations sur des applications](/help/using/c-about-apps/c-about-apps.md)spécifiques. Il est recommandé d’épingler la dernière version majeure du paquet (qui peut être trouvée via [Livefyre.require](https://cdn.livefyre.com/packages.html)), afin d’éviter des intégrations inattendues.

Suivant : Ajoutez une authentification à votre site pour permettre aux utilisateurs de publier des commentaires.
