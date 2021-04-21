---
description: L’incorporation de l’application de commentaires suit le processus d’incorporation d’une application principale.
title: Incorporer une application de commentaires
exl-id: 5eb191f8-ee52-4a9d-9180-90457a49fd4e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Incorporer une application de commentaires {#embed-a-comments-app}

L’incorporation de l’application de commentaires suit le processus d’incorporation d’une application principale.

L’incorporation de l’application Commentaires suit le processus d’incorporation d’une application principale décrite dans [Incorporation d’une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

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

Comme indiqué dans la section Building CollectionMeta, CollectionMeta est un objet JSON codé. Dans l’exemple ci-dessus, l’objet JSON utilise le format suivant avant d’être codé en JWT :

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```
