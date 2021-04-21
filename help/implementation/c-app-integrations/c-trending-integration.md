---
description: Présente les collections les plus principales de votre site ou réseau.
title: Suivi des tendances
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---

# Suivi des tendances{#trending}

Présente les collections les plus principales de votre site ou réseau.

Utilisez l’option de tendance pour présenter les collections présentant l’activité la plus récente de votre site ou réseau.

## Analytics {#section_wtz_whb_c1b}

Le moyen le plus rapide d&#39;intégrer avec Trending est d&#39;utiliser la version intégrée hébergée sur le CDN de Livefyre.

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

Vous disposez maintenant d’une application de tendance ! Voir tout cela en action dans [cet exemple](https://codepen.io/gobengo/pen/GijEy).

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

Indiquez l’identifiant du site pour n’afficher que les collections provenant d’un seul site de votre réseau. (Facultatif.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Fournissez une seule balise Collection pour n’afficher que les collections avec cette balise. (Facultatif.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```
