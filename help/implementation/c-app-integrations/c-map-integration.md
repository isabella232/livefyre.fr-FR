---
description: Traçage du contenu utilisateur vers une carte interactive.
seo-description: Traçage du contenu utilisateur vers une carte interactive.
seo-title: Carte
solution: Experience Manager
title: Carte
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Carte{#map}

Traçage du contenu utilisateur vers une carte interactive.

Map vous permet de diffuser du contenu géolocalisé sur une carte du monde, ce qui vous permet de localiser le buzz social autour des dernières nouvelles ou d'un événement en direct. Tout le contenu applicable s’affiche, y compris le texte, les commentaires, les photos et les tweets.

>[!NOTE]
>
>Les cartes sont alimentées par [© OpenStreetMap](https://www.openstreetmap.org/copyright), qui fournit les données que Livefyre utilise pour rendre ses cartes.

## Analytics {#section_w2m_db2_d1b}

Le moyen le plus rapide d'utiliser Map est d'utiliser la version intégrée hébergée sur le CDN de Livefyre.

Tout d’abord, ajoutez [Livefyre.js](https://github.com/Livefyre/Livefyre.js) à votre page.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Positionnez ensuite l’élément dans lequel l’application de mappage apparaîtra.

```
<div id="map" style="height: 500px;"></div>
```

Enfin, utilisez Livefyre.require pour construire la carte, et obtenir une collection à l'entrée à partir du streaming hub-sdk. Gardez à l’esprit que le mappage ne peut afficher que le contenu avec des métadonnées géolocalisées. Twitter et Instagram Curate prennent en charge cette fonctionnalité. Pour optimiser les performances, incluez un filtre de géolocalisation sur toutes les règles de traitement de la collection.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

Regardez cet exemple [en](https://codepen.io/cheung31/pen/wkmbF)direct.

## Configuration {#section_jc5_gxb_c1b}

`initial`

Nombre initial d’éléments à charger à partir de la collection et à afficher sur la carte. Une fois ce nombre chargé, les utilisateurs peuvent cliquer sur un bouton pour en afficher davantage. (Facultatif. La valeur par défaut est 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Options à transmettre au mappage [de la brochure](https://leafletjs.com/) sous-jacente, que Map utilise pour le rendu. Utilisez cette option pour définir les options [de zone cliquable](https://leafletjs.com/reference.html#map-options)de la brochure, y compris le point central initial de la carte et les niveaux de zoom initial et maximal. (Facultatif.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

