---
description: Créez un mur multimédia avec un contenu en flux continu en temps réel.
title: Mur multimédia
exl-id: 597af7e1-9ada-4893-9071-e17c21ef0d04
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Media Wall{#media-wall}

Créez un mur multimédia avec un contenu en flux continu en temps réel.

Le mur multimédia vous permet de créer un mur social en temps réel pour votre site. Utilisez le package streaming hub-wallpackage du SDK JavaScript de Livefyre pour afficher les flux sociaux Livefyre comme une expérience de contenu visuellement attrayante, plein écran et en mosaïque qui permet de couvrir des événements en direct, d’héberger des concours de photos et de mettre en oeuvre des sections sociales de votre site Web.

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

Vous avez maintenant un mur ! Voir tout cela en action dans [cet exemple](https://codepen.io/gobengo/pen/dFwDL).

**Accès à une erreur ?** Vérifiez que vous transmettez le paramètre d’environnement correct. Les options sont `livefyre.com` (production) ou `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Toute personnalisation de style des tweets rendus par votre application Media Wall App doit être effectuée conformément aux [exigences d’affichage](https://dev.twitter.com/terms/display-requirements) de Twitter.

## Options de configuration {#section_ucv_qvb_c1b}

`columns`

Permet de définir le nombre de colonnes de votre mur multimédia lors de la construction de ce mur. Si cette option est définie, la largeur de chaque colonne s’adaptera automatiquement à la taille du conteneur de la paroi multimédia, tout en conservant le nombre spécifié de colonnes.

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

Permet de définir la largeur minimale (en pixels) de chaque colonne dans l’élément de conteneur de la paroi multimédia. (Votre mur multimédia sélectionne automatiquement un nombre approprié de colonnes, en fonction de la largeur de son élément de conteneur. Par défaut, la largeur du mur multimédia divisée par la largeur minimale de contenu (300 px, si elle n’est pas définie) détermine le nombre de colonnes.

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

Par défaut, lorsqu’il existe des pièces jointes pour un élément de contenu, les murs multimédia affichent une miniature cliquable. Lorsque l’utilisateur clique dessus, l’application ouvre une fenêtre modale affichant la pièce jointe photo/vidéo dans son intégralité. Pour désactiver cette option, définissez modal sur false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Définit le bouton [!UICONTROL Post Content] à afficher sur votre mur. Cette option nécessite de transmettre `opts.collection` et d’ajouter une intégration Livefyre.js Auth à la page.

`postButton` parameters:

* `false` (par défaut) : N’affichez pas de bouton Contenu de la publication. (Crée un mur multimédia en lecture seule.)
* `true` ou  `LiveMediaWall.postButtons.contentWithPhotos`: Incluez un bouton qui permet aux utilisateurs d’ajouter du contenu de texte, avec les photos jointes.

* `LiveMediaWall.postButtons.content`: Incluez un bouton qui permet aux utilisateurs d’ajouter du texte, mais pas de joindre des photos.
* `LiveMediaWall.postButtons.photo`: Incluez un bouton qui permet aux utilisateurs d’ajouter une photo, mais sans texte.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Définit le nombre d’éléments de contenu à ajouter au mur lorsque l’utilisateur clique sur le bouton [!UICONTROL Show More].

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Options de configuration de style {#section_ztv_dvb_c1b}

Media Wall offre également plusieurs options de configuration qui vous permettent de personnaliser la couleur, le style et la taille du texte. Pour mettre en oeuvre ces options, utilisez la syntaxe suivante :

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

Pour une entrée valide, consultez les normes W3C pour les propriétés CSS [Font Family](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Font Size](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Line Height,](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) et [Color](https://www.w3.org/TR/css3-color/#colorunits).

* **bodyFontSize** *(Chaîne de taille de police CSS)* Taille de police du corps du contenu.

* **bodyLineHeight** *(Chaîne de hauteur de ligne CSS)* Hauteur de ligne pour le corps du contenu.

* **buttonActiveBackgroundColor** *(Chaîne de couleur CSS)** Couleur de l’arrière-plan du bouton sur principal.

* **buttonBorderColor** *(Chaîne de couleur CSS)** Couleur des bordures de bouton.

* **buttonHoverBackgroundColor** *(Chaîne de couleur CSS)* Couleur d’arrière-plan du bouton au survol.

* **buttonTextColor** *(Chaîne de couleur CSS)* Couleur des libellés de bouton.

* **cardBackgroundColor** *(Chaîne de couleur CSS)* Couleur d’arrière-plan des cartes de contenu dans le mur multimédia.

* **displayNameColor** *(Chaîne de couleur CSS)* Couleur des noms d’affichage dans la signature.

* **fontFamily** *(Chaîne de famille de polices CSS)* Famille de polices pour le corps du texte.

* **footerTextColor** *(Chaîne de couleur CSS)* Couleur du texte secondaire (par exemple, le texte de pied de page et le nom d’utilisateur de la signature).

* **linkAttachmentBackgroundColor** *(Chaîne de couleur CSS)* Couleur d’arrière-plan des pièces jointes de lien (pièces jointes empilées).

* **linkAttachmentBorderColor** *(Chaîne de couleur CSS)* Couleur de bordure des pièces jointes de lien (pièces jointes empilées).

* **linkAttachmentTextColor** *(Chaîne de couleur CSS)* Couleur du texte de la pièce jointe du lien.

* **linkColor** *(Chaîne de couleur CSS)* Couleur des hyperliens (tels que les liens dans le corps du texte et les liens de nom d’affichage).

* **textColor** *(Chaîne de couleur CSS)* Couleur du corps du texte.

* **titleFontSize** *(Chaîne CSS Font Size)* Taille de police des titres de contenu.

* **titleLineHeight** *(Chaîne de hauteur de ligne CSS)* Hauteur de ligne pour les titres de contenu.

* **sourceLogoColor** *(Chaîne de couleur CSS)* Couleur du logo source.

* **usernameColor** *(chaîne de couleur CSS)* Couleur des noms d’utilisateur dans la signature.
