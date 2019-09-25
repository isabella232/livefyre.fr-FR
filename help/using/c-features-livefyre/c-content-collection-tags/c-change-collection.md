---
description: Permet aux utilisateurs de cliquer sur Collections à partir d’une mise en page et d’une URL uniques.
seo-description: Permet aux utilisateurs de cliquer sur Collections à partir d’une mise en page et d’une URL uniques.
seo-title: Modifier la collection
solution: Experience Manager
title: Modifier la collection
uuid: 69bafcc7-c55e-47d6-bc79-b0db80fdf138
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Modifier la collection{#change-collection}

Permet aux utilisateurs de cliquer sur Collections à partir d’une mise en page et d’une URL uniques.

Utilisez le délégué Modifier la collection pour modifier la collection affichée sur une page, sans modifier l’URL, pendant qu’une application Livefyre est déjà chargée. Utilisez cette fonction pour afficher des galeries de photos ou de vidéos ou d’autres applications dans lesquelles la collection affichée doit changer après une action de l’utilisateur.

Par exemple, un clic sur une vidéo ou une photo dans une galerie charge une collection spécifique à cette sélection, tandis que l’URL de la page ne change pas.

Pour charger l’une des trois collections à partir d’une seule page de comptage [des](/help/implementation/c-advanced-topics/t-display-comment-count.md) commentaires :

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

