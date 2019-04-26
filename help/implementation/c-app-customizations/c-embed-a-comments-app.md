---
description: L'incorporation de l'application de commentaires suit le processus d'incorporation
  d'une application de base.
seo-description: L'incorporation de l'application de commentaires suit le processus
  d'incorporation d'une application de base.
seo-title: Incorporation d'une application de commentaires
solution: Experience Manager
title: Incorporation d'une application de commentaires
uuid: e 4982 ad 3-cab 1-4805-a 55 c -594 cca 3 b 7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e

---


# Incorporation d'une application de commentaires{#embed-a-comments-app}

L'incorporation de l'application de commentaires suit le processus d'incorporation d'une application de base.

Incorporation de l'application de commentaires Suit le processus d'incorporation d'une application de base décrite dans [Incorporation d'une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

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

Comme indiqué dans la section Building collectionmeta, collectionmeta est un objet JSON codé. Dans l'exemple ci-dessus, l'objet JSON adopte le format suivant avant son codage JWT :

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

