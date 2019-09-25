---
description: Présente les collections les plus actives sur votre site ou réseau.
seo-description: Présente les collections les plus actives sur votre site ou réseau.
seo-title: Suivi des tendances
solution: Experience Manager
title: Suivi des tendances
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Suivi des tendances{#trending}

Présente les collections les plus actives sur votre site ou réseau.

Utilisez l’option Tendance pour présenter les collections présentant l’activité la plus récente de votre site ou réseau.

## Analytics {#section_wtz_whb_c1b}

Le moyen le plus rapide d’intégrer les tendances consiste à utiliser la version intégrée hébergée sur le CDN de Livefyre.

Tout d’abord, ajoutez [Livefyre.js](https://github.com/Livefyre/Livefyre.js) à votre page.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionnez ensuite l’élément dans lequel l’application apparaîtra.

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

Vous avez maintenant une application de tendance ! Tout cela est en action dans [cet exemple](https://codepen.io/gobengo/pen/GijEy).

## Configuration {#section_k5k_qhb_c1b}

`network`

Réseau à partir duquel les collections seront extraites. (requis.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Indiquez l’identifiant du site pour afficher uniquement les collections d’un seul site de votre réseau. (Facultatif.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Fournissez une balise Collection unique pour n’afficher que les collections avec cette balise. (Facultatif.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

