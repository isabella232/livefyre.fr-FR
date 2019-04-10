---
description: Créez un mur multimédia, avec diffusion en continu de contenu en temps
  réel.
seo-description: Créez un mur multimédia, avec diffusion en continu de contenu en
  temps réel.
seo-title: Mur multimédia
solution: Experience Manager
title: Mur multimédia
uuid: c 6087 c 80-a 35 b -44 d 2-9 dd 4-ba 9 cd 471172 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Mur multimédia{#media-wall}

Créez un mur multimédia, avec diffusion en continu de contenu en temps réel.

Le mur multimédia vous permet de créer un mur social en temps réel pour votre site. Utilisez le plug-in streamhub-wallpack de Livefyre JavaScript pour afficher les flux sociaux Livefyre en tant qu'expérience de contenu en mosaïque visuelle et attrayante, idéal pour la couverture d'événements en direct, l'hébergement de concours de photos et l'activation de sections sociales de votre site Web.

## Analytics{#section_jfm_bwb_c1b}

La méthode la plus rapide pour ajouter un mur multimédia est d'utiliser la version construite hébergée sur le CDN de Livefyre.

Ajoutez d'abord [Livefyre. js](https://github.com/Livefyre/Livefyre.js) à votre site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionnez ensuite l'élément dans lequel le mur multimédia apparaîtra.

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

Vous avez maintenant un mur ! Reportez-vous à l'exemple suivant dans [cet exemple](https://codepen.io/gobengo/pen/dFwDL).

**Accès à une erreur ?** Vérifiez que vous transmettez le paramètre d'environnement correct. Les options incluent `livefyre.com` (production) ou `t402.livefyre.com` UAT.

>[!NOTE]
>
>Toute personnalisation de style des tweets rendus par votre application Mur multimédia doit être effectuée conformément aux exigences [d'affichage de Twitter](https://dev.twitter.com/terms/display-requirements).

## Options de configuration {#section_ucv_qvb_c1b}

`columns`

Permet de définir le nombre de colonnes pour votre mur multimédia lors de la construction du mur. Si cette option est définie, la largeur de chaque colonne s'adapte automatiquement à la taille du conteneur du mur multimédia, tout en conservant le nombre de colonnes spécifié.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Nombre d'éléments de contenu à rendre au chargement de la page. Par défaut, 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Permet de définir la largeur minimale (pixel) de chaque colonne dans l'élément conteneur du mur multimédia. (Votre mur multimédia sélectionne automatiquement le nombre de colonnes approprié, selon la largeur de son élément conteneur. Par défaut, la largeur du mur multimédia divisée par la largeur minimale du contenu (300 px, si non définie) détermine le nombre de colonnes.)

>[!NOTE]
>
>N'utilisez pas cette option conjointement avec l'option Colonnes.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Par défaut, lorsque des pièces jointes sont jointes à un élément de contenu, les murs de médias affichent une miniature cliquable. Lorsque vous cliquez dessus, l'application ouvre dans son intégralité un modal affichant la photo/la vidéo vidéo. Pour désactiver cette option, définissez la variable modale sur false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Définit [!UICONTROL Post Content] le bouton qui s'affiche sur votre mur. Cette option requiert que vous transfériez `opts.collection`et ajoutez une intégration Livefyre. js authentique à la page.

`postButton` paramètres :

* `false` (par défaut) : N'affichez pas le bouton Contenu de la publication. (Crée un mur multimédia en lecture seule).
* `true` (ou `LiveMediaWall.postButtons.contentWithPhotos`) : Insérez un bouton permettant aux utilisateurs d'ajouter du contenu texte avec des photos jointes.

* `LiveMediaWall.postButtons.content`: Insérez un bouton permettant aux utilisateurs d'ajouter du contenu texte, mais pas de joindre des photos.
* `LiveMediaWall.postButtons.photo`: Insérez un bouton permettant aux utilisateurs d'ajouter une photo, mais pas de texte.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Définit le nombre d'éléments de contenu à ajouter au mur lorsque l'utilisateur clique sur [!UICONTROL Show More] votre bouton.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Options de configuration de style {#section_ztv_dvb_c1b}

Le mur multimédia propose également plusieurs options de configuration permettant de personnaliser la couleur, le style et la taille du texte. Pour mettre en œuvre ces options, utilisez la syntaxe suivante :

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

Pour obtenir des données valides, reportez-vous aux normes W 3 C relatives à la famille [de polices CSS](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [à la taille de police](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [à la hauteur de ligne et](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) aux [propriétés de couleur](https://www.w3.org/TR/css3-color/#colorunits) .

* **Bodyfontsize** *(chaîne de taille de police CSS)* Taille de police du texte du corps de contenu.

* **Bodylineheight** *(chaîne de hauteur de ligne CSS)* Hauteur de ligne pour le texte du corps de contenu.

* **Buttonactivebackgroundcolor** *(chaîne de couleur CSS)** Couleur de l'arrière-plan du bouton activé.

* **Buttonbordercolor** *(chaîne de couleur CSS)** Couleur des bordures de bouton.

* **Buttonhoverbackgroundcolor** *(chaîne de couleur CSS)* Couleur de l'arrière-plan du bouton au survol.

* **Buttontextcolor** *(chaîne de couleur CSS)* Couleur des étiquettes de bouton.

* **Cardbackgroundcolor** *(chaîne de couleur CSS)* Couleur d'arrière-plan des cartes de contenu dans le mur multimédia.

* **Displaynamecolor** *(chaîne de couleur CSS)* Couleur des noms d'affichage dans la signature.

* **Fontfamily** *(String Font Family String)* Famille de polices pour le corps du texte.

* **Footertextcolor** *(chaîne de couleur CSS)* Couleur du texte secondaire (comme le texte du pied de page et le nom d'utilisateur dans la signature).

* **Linkattachmentbackgroundcolor** *(chaîne de couleur CSS)* Couleur d'arrière-plan des pièces jointes (pièces jointes empilées).

* **Linkattachmentbordercolor** *(chaîne de couleur CSS)* Couleur de bordure pour les liens joints (pièces jointes empilées).

* **Linkattachmenttextcolor** *(String Color String)* Color for link attachment attachment text.

* **Linkcolor** *(chaîne de couleur CSS)* Couleur des hyperliens (tels que les liens dans le texte du corps et les liens d'affichage).

* **Textcolor** *(chaîne de couleur CSS)* Couleur du texte de corps.

* **Titlefontsize** *(chaîne de taille de police CSS)* Taille de police des titres de contenu.

* **Titlelineheight** *(chaîne de hauteur de ligne CSS)* Hauteur de ligne des titres de contenu.

* **Sourcelogocolor** *(chaîne de couleur CSS)* Couleur du logo source.

* **Usernamecolor** *(chaîne de couleur CSS)* Couleur des noms d'utilisateur dans la signature.
