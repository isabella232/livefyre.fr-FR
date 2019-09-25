---
description: Présente plusieurs collections sur une seule page.
seo-description: Présente plusieurs collections sur une seule page.
seo-title: Collections multiples
solution: Experience Manager
title: Collections multiples
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Collections multiples {#multiple-collections}

Présente plusieurs collections sur une seule page.

Vous pouvez inclure plusieurs collections sur une seule page de votre site. Par exemple, pour publier un événement, vous pouvez avoir un blog en direct ou une discussion sur le chat pendant l’événement, avec une application distincte sur le côté de votre page, affichant le contenu traité associé sur le Web social. Vous pouvez également inclure une application de commentaires sous un article, avec un chat sur le côté.

Pour obtenir plusieurs conversations sur une page, ajoutez une ou plusieurs configurations dans une baie et transmettez la baie à l’appel de chargement. Par exemple :

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
