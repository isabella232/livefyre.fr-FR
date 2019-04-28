---
description: Présentez plusieurs collections sur une seule page.
seo-description: Présentez plusieurs collections sur une seule page.
seo-title: Collections multiples
solution: Experience Manager
title: Collections multiples
uuid: 9675 ffd 7-1 a 59-42 a 1-b 3 ba -40 af 1744 cfd 1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Collections multiples {#multiple-collections}

Présentez plusieurs collections sur une seule page.

Vous pouvez inclure plusieurs collections sur une seule page de votre site. Par exemple, pour publier un événement, vous pouvez disposer d&#39;un blog direct ou d&#39;une discussion Chat pendant l&#39;événement, avec une application distincte sur le côté de la page, affichant le contenu traité associé depuis le Web social. Vous pouvez également inclure une application de commentaires sous un article, avec une conversation sur le côté.

Pour obtenir plusieurs conversations sur une page, ajoutez une ou plusieurs configurations dans un tableau et transmettez le tableau à l&#39;appel de chargement. Par exemple.

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
