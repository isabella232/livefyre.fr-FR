---
seo-title: Incorporation d'une application
solution: Experience Manager
title: Incorporation d'une application
uuid: e 75 caf 0 e -04 ea -4 b 04-89 ed-fea 1183 ecf 63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Incorporation d'une application{#embed-an-app}

Ajoutez des applications Livefyre à vos pages Web à l'aide de la structure de code intégré Livefyre. js.

Cette documentation est destinée à une audience technique. Pour [des informations non techniques sur les applications](/help/using/c-about-apps/c-about-apps.md).

Cette section décrit la structure de code que vous devez inclure dans votre modèle de page pour incorporer les applications Livefyre sur votre site.

1. Créez un fichier.html avec un espace réservé Livefyre.

   Créez un fichier.html dans l'éditeur de texte de votre choix. Créez un élément Livefyre `<div>` fictif dans lequel l'application sera incorporée.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Incluez la bibliothèque Livefyre. js.

   Incluez ensuite la bibliothèque JS Livefyre. Placez la référence suivante dans un `<script>` élément de votre `<head>` élément. Ouvrez ensuite votre page dans un navigateur et utilisez l'inspecteur Web de votre navigateur pour vérifier que Livefyre est chargé.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Générez l'application Livefyre.

   Utilisez cette option pour `Livefyre.require` créer des applications de base et de SDK en transmettant le ou les packs Livefyre que vous prévoyez d'utiliser.

   1. Créez une application de base.

      Pour créer une application de base (commentaires, blog en direct ou chat), utilisez la structure suivante :

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Créez une application SDK.

      Pour créer une application SDK telle que le mur ou le flux multimédia, utilisez la structure suivante :

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

      Voir [plus d'informations sur les applications spécifiques](/help/using/c-about-apps/c-about-apps.md). Il est recommandé d'épingler la dernière version majeure du pack (qui est disponible via [Livefyre. require)](https://cdn.livefyre.com/packages.html)pour éviter les intégrations rompues inattendues.

Suivant : Ajoutez une authentification à votre site pour permettre à vos utilisateurs de publier des commentaires.
