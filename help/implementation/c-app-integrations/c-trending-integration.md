---
description: Présentez les collections les plus actives sur votre site ou réseau.
seo-description: Présentez les collections les plus actives sur votre site ou réseau.
seo-title: Tendances
solution: Experience Manager
title: Tendances
uuid: 3031523 d-b 487-4 eee-bba 6-5 d 8 f 9971874 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Tendances{#trending}

Présentez les collections les plus actives sur votre site ou réseau.

Utilisez les tendances pour présenter les collections avec l&#39;activité la plus récente de votre site ou réseau.

## Analytics{#section_wtz_whb_c1b}

La méthode la plus rapide pour intégrer les tendances est d&#39;utiliser la version construite hébergée sur le CDN Livefyre.

Ajoutez d&#39;abord [Livefyre. js](https://github.com/Livefyre/Livefyre.js) à votre page.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionnez ensuite l&#39;élément dans lequel l&#39;application apparaîtra.

```
<div id="trending"></div>
```

Enfin, utilisez `Livefyre.require` pour construire le composant.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

Vous disposez maintenant d&#39;une application de tendance. Reportez-vous à l&#39;exemple suivant dans [cet exemple](https://codepen.io/gobengo/pen/GijEy).

## Configuration {#section_k5k_qhb_c1b}

`network`

Réseau d&#39;où les collections seront extraites. (Obligatoire.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Indiquez l&#39;ID du site pour afficher les collections uniquement à partir d&#39;un seul site sur votre réseau. (Facultatif)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Fournissez une balise Collection unique pour n&#39;afficher que les collections avec cette balise. (Facultatif)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

