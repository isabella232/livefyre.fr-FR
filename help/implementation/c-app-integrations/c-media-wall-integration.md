---
description: Créez un mur multimédia avec diffusion en temps réel du contenu.
seo-description: Créez un mur multimédia avec diffusion en temps réel du contenu.
seo-title: Media Wall
solution: Experience Manager
title: Media Wall
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Media Wall{#media-wall}

Créez un mur multimédia avec diffusion en temps réel du contenu.

Media Wall vous permet de créer un mur social en temps réel pour votre site. Utilisez le paquet streaming-wallpackage du SDK JavaScript Livefyre pour afficher les flux sociaux Livefyre sous forme de contenu en mosaïque et plein écran visuellement attrayant, idéal pour couvrir des événements en direct, héberger des concours de photos et alimenter des sections sociales de votre site Web.

## Analytics {#section_jfm_bwb_c1b}

Le moyen le plus rapide d’ajouter un mur multimédia consiste à utiliser la version intégrée hébergée sur le CDN de Livefyre.

Tout d’abord, ajoutez [Livefyre.js](https://github.com/Livefyre/Livefyre.js) à votre site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionnez ensuite l’élément dans lequel le mur multimédia apparaîtra.

```
<div id="wall"></div>
```

Enfin, utilisez `Livefyre.require` pour construire le composant.

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

Vous avez maintenant un Mur ! Tout cela est en action dans [cet exemple](https://codepen.io/gobengo/pen/dFwDL).

**Accès à une erreur ?** Vérifiez que vous transmettez le paramètre d’environnement correct. Les options incluent `livefyre.com` (production) ou `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Toute personnalisation de style des tweets rendus par votre application Media Wall App doit être effectuée conformément aux exigences [d’](https://dev.twitter.com/terms/display-requirements)affichage de Twitter.

## Options de configuration {#section_ucv_qvb_c1b}

`columns`

Permet de définir le nombre de colonnes de votre mur multimédia lors de la construction du mur. Si cette option est définie, la largeur de chaque colonne s’adaptera automatiquement à la taille du conteneur de la paroi multimédia, tout en conservant le nombre spécifié de colonnes.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Nombre d’éléments de contenu à rendre au chargement de la page. La valeur par défaut est 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Permet de définir la largeur minimale (en pixels) de chaque colonne dans l’élément conteneur du mur multimédia. (Votre mur multimédia sélectionne automatiquement un nombre approprié de colonnes, selon la largeur de son élément conteneur. Par défaut, la largeur du mur de supports divisée par la largeur minimale du contenu (300 px, si elle n’est pas définie) détermine le nombre de colonnes.

>[!NOTE]
>
>N’utilisez pas cette option en combinaison avec l’option Colonnes.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Par défaut, lorsqu’il existe des pièces jointes pour un élément de contenu, les murs multimédia affichent une miniature cliquable. Lorsque vous cliquez dessus, l’application ouvre un module qui affiche la pièce jointe photo/vidéo dans son intégralité. Pour désactiver cette option, définissez modale sur false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Définit le [!UICONTROL Post Content] bouton à afficher sur votre mur. Cette option nécessite de vous connecter `opts.collection`et d’ajouter une intégration Livefyre.js Auth à la page.

`postButton` parameters :

* `false` (par défaut) : N’affichez pas de bouton Contenu de la publication. (Crée un mur de supports en lecture seule.)
* `true` (ou `LiveMediaWall.postButtons.contentWithPhotos`) : Ajoutez un bouton permettant aux utilisateurs d’ajouter du texte, avec les photos jointes.

* `LiveMediaWall.postButtons.content`: Incluez un bouton qui permet aux utilisateurs d’ajouter du texte, mais pas de joindre des photos.
* `LiveMediaWall.postButtons.photo`: Incluez un bouton permettant aux utilisateurs d’ajouter une photo, mais sans texte.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Définit le nombre d’éléments de contenu à ajouter au mur lorsque vous cliquez sur votre [!UICONTROL Show More] bouton.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Options de configuration du style {#section_ztv_dvb_c1b}

Media Wall propose également plusieurs options de configuration qui vous permettent de personnaliser la couleur, le style et la taille du texte. Pour implémenter ces options, utilisez la syntaxe suivante :

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

Pour une entrée valide, consultez les normes W3C pour les propriétés CSS [Font Family](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Font Size](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Line Height,](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) and [Color.](https://www.w3.org/TR/css3-color/#colorunits)

* **bodyFontSize***(Chaîne CSS Font Size)* Taille de police du texte de contenu.

* **bodyLineHeight** *(Chaîne de hauteur de ligne CSS)* Hauteur de ligne pour le texte du corps du contenu.

* **buttonActiveBackgroundColor** *(chaîne de couleur CSS)** Couleur de l’arrière-plan du bouton sur actif.

* **buttonBorderColor** *(chaîne de couleur CSS)** Couleur des bordures de bouton.

* **buttonHoverBackgroundColor** *(chaîne de couleur CSS)* Couleur de l’arrière-plan du bouton au survol.

* **buttonTextColor** *(chaîne de couleur CSS)* Couleur des libellés de bouton.

* **cardBackgroundColor** *(chaîne de couleur CSS)* Couleur d’arrière-plan des cartes de contenu dans le mur multimédia.

* **displayNameColor** *(chaîne de couleur CSS)* Couleur des noms d’affichage dans la ligne d’origine.

* **fontFamily** *(Chaîne de famille de polices CSS)* Famille de polices pour le texte du corps.

* **footerTextColor***(chaîne de couleur CSS)* Couleur du texte secondaire (comme le texte de pied de page et le nom d’utilisateur de la ligne d’entrée).

* **linkAttachmentBackgroundColor** *(chaîne de couleur CSS)* Couleur d’arrière-plan des pièces jointes de lien (pièces jointes empilées).

* **linkAttachmentBorderColor***(chaîne de couleur CSS)* Couleur de bordure des pièces jointes de lien (pièces jointes empilées).

* **linkAttachmentTextColor***(Chaîne de couleur CSS)* Couleur du texte de la pièce jointe du lien.

* **linkColor** *(chaîne de couleur CSS)* Couleur des hyperliens (tels que les liens dans le corps du texte et les liens de nom d’affichage).

* **textColor** *(chaîne de couleur CSS)* Couleur du texte du corps.

* **titleFontSize** *(Chaîne CSS Font Size)* Taille de police des titres de contenu.

* **titleLineHeight** *(chaîne de hauteur de ligne CSS)* Hauteur de ligne pour les titres de contenu.

* **sourceLogoColor***(chaîne de couleur CSS)* Couleur du logo source.

* **usernameColor** *(chaîne de couleur CSS)* Couleur des noms d’utilisateur dans la ligne d’origine.
