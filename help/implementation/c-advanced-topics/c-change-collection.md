---
description: Permet aux utilisateurs de cliquer sur les collections à partir d'une
  seule mise en page et d'une URL.
seo-description: Permet aux utilisateurs de cliquer sur les collections à partir d'une
  seule mise en page et d'une URL.
seo-title: Modifier la collection
solution: Experience Manager
title: Modifier la collection
uuid: 81 c 8 a 554-375 f -4659-9 e 25-5 b 3618824633
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Modifier la collection {#change-collection}

Permet aux utilisateurs de cliquer sur les collections à partir d'une seule mise en page et d'une URL.

Utilisez le délégué de collection Modifier la collection pour modifier la collection affichée sur une page sans modifier l'URL, alors qu'une application Livefyre est déjà chargée. Utilisez cette fonction pour afficher les galeries de photos ou de vidéos, ou d'autres applications dans lesquelles la collection affichée doit changer après une action de l'utilisateur.

Par exemple, cliquer sur une vidéo ou une photo dans une galerie chargera une collection spécifique à cette sélection, tandis que l'URL de la page ne change pas.

[Pour charger l'une des trois collections à partir d'une seule page](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
