---
description: L’incorporation de l’application de commentaires suit le processus d’incorporation d’une application principale.
seo-description: L’incorporation de l’application de commentaires suit le processus d’incorporation d’une application principale.
seo-title: Incorporer une application de commentaires
solution: Experience Manager
title: Incorporer une application de commentaires
uuid: e4982ad3-cab1-4805-a55c-594cca3b7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e

---


# Incorporer une application de commentaires{#embed-a-comments-app}

L’incorporation de l’application de commentaires suit le processus d’incorporation d’une application principale.

L’incorporation de l’application de commentaires suit le processus d’incorporation d’une application principale décrite dans [Incorporation d’une application.](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

## Exemple

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Comme indiqué dans la section Building CollectionMeta, CollectionMeta est un objet JSON codé. Dans l’exemple ci-dessus, l’objet JSON utilise le format suivant avant d’être codé JWT :

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

