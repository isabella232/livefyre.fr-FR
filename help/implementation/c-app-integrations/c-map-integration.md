---
description: Faire correspondre le contenu d'un utilisateur à une carte interactive.
seo-description: Faire correspondre le contenu d'un utilisateur à une carte interactive.
seo-title: Carte
solution: Experience Manager
title: Carte
uuid: 1 c 3 e 399 d-a 610-4 b 80-a 3 b 2-a 5502 b 31480 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Carte{#map}

Faire correspondre le contenu d'un utilisateur à une carte interactive.

Carte vous permet de diffuser du contenu géographiquement placé sur une carte du monde, ce qui vous permet de localiser l'buzz social autour de la rupture d'actualités ou d'un événement en direct. Tous les contenus applicables s'affichent, y compris le texte, les commentaires, les photos et les tweets.

>[!NOTE]
>
>Les cartes sont pilotées par [© openstreetmap](https://www.openstreetmap.org/copyright), qui fournit les données utilisées par Livefyre pour générer ses cartes.

## Analytics{#section_w2m_db2_d1b}

La méthode la plus rapide pour utiliser Carte consiste à utiliser la version construite hébergée sur le CDN Livefyre.

Ajoutez d'abord [Livefyre. js](https://github.com/Livefyre/Livefyre.js) à votre page.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Positionnez ensuite l'élément dans lequel l'application Map apparaîtra.

```
<div id="map" style="height: 500px;"></div>
```

Enfin, utilisez Livefyre. require pour construire le mappage et obtenir une collection à afficher à partir de streamhub-sdk. N'oubliez pas que Carte peut afficher uniquement le contenu avec des métadonnées géographiquement. Twitter et Instagram Traitate prennent en charge cette fonctionnalité. Pour garantir de meilleures performances, incluez un filtre de géolocalisation sur toutes vos règles de traitement pour la collection.

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

Consultez cet [exemple en direct](https://codepen.io/cheung31/pen/wkmbF).

## Configuration {#section_jc5_gxb_c1b}

`initial`

nombre initial d'éléments à charger à partir de la collection et affichés sur la carte. Une fois ce nombre chargé, les utilisateurs peuvent cliquer sur un bouton pour afficher plus d'informations. (Facultatif. Par défaut, 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Options à transmettre à la carte [sous-jacente,](https://leafletjs.com/) que Carte utilise pour le rendu. Utilisez cette option pour définir [les options de Carte de la feuille](https://leafletjs.com/reference.html#map-options), y compris le point centré initial de la carte, ainsi que les niveaux de zoom initial et maximal. (Facultatif)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

