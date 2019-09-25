---
description: Les styles personnalisés sont appliqués par le biais d’un objet injecté dans le constructeur Sidenotes.
seo-description: Les styles personnalisés sont appliqués par le biais d’un objet injecté dans le constructeur Sidenotes.
seo-title: Sidenotes Styles personnalisés
title: Sidenotes Styles personnalisés
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sidenotes Styles personnalisés{#sidenotes-custom-styles}

Les styles personnalisés sont appliqués par le biais d’un objet injecté dans le constructeur Sidenotes.

Les "clés" sont des clés d’objet qui représentent des éléments DOM, tandis que les "propriétés" sont des propriétés CSS prises en charge pour la clé particulière. Par exemple, pour personnaliser le style de blockBtn (le bouton qui lance la fenêtre contextuelle Sidenotes), vous devez créer un objet tel que :

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **Clé** | **Propriétés** | Description |
|---|---|---|
| `anonymousAvatar` | "hauteur", "largeur" | Image d’avatar anonyme, à gauche de l’éditeur de zone de texte. |
| `blockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | L'"icône de lanceur" est placée en regard des éléments spécifiés comme pouvant être mis à part. |
| `blockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icône de lanceur lorsque l’état est actif. |
| `commentAvatar` | "hauteur", "largeur" | Image d’avatar à gauche des notes de niveau supérieur. |
| `commentBody` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Corps de texte des notes liées. |
| `commentDisplayName` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Nom d’affichage de l’utilisateur qui a laissé une note. |
| `commentDownvote` | ‘fontColor’, ‘fontSize’ | Bouton de téléchargement sur une note. |
| `commentReplyExpand` | "BackgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Bouton permettant d’étendre les threads avec un grand nombre de réponses. |
| `commentTags` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Balises relatives à un utilisateur sur une note. |
| `commentUpvote` | ‘fontColor’, ‘fontSize’ | Bouton Mettre à jour sur une note. |
| `editorTextarea` | "height", "width", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Zone de saisie de zone de texte pour laisser des notes. |
| `mediaBlockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icône du lanceur de médias lorsqu’il se trouve au-dessus d’un élément multimédia (image, vidéo). |
| `mediaBlockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icône du lanceur de médias à l’état actif. |
| `numSidenotes` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "BackgroundColor", "borderColor", "borderWidth", "height", "width" | Bouton cliquable qui affiche le nombre de Sidenotes dans la collection. |
| `numSidenotesPopover` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "BackgroundColor", "borderColor", "borderWidth", "height", "width" | Popover avec une brève explication des Sidenotes pour l'utilisateur. |
| `popover` | "BackgroundColor" | Cette fenêtre contextuelle s’affiche lorsque l’icône de lancement est appelée. |
| `popoverArrowLeft` | "fondImage", "hauteur", "gauche", "droite", "haut", "largeur" | Elément de flèche gauche sur la fenêtre contextuelle qui pointe vers l’élément DOM contenant une icône de lanceur. |
| `popoverArrorRight` | "fondImage", "hauteur", "gauche", "droite", "haut", "largeur" | Elément de flèche vers la droite sur la fenêtre contextuelle qui pointe vers l’élément DOM contenant une icône de lanceur. |
| `popoverArrowTop` | "fondImage", "hauteur", "gauche", "droite", "haut", "largeur" | Elément de flèche supérieure dans la fenêtre contextuelle qui pointe vers l’élément DOM contenant une icône de lanceur. |
| `replyAvatar` | "hauteur", "largeur" | Image de l’avatar à gauche des notes de niveau réponse. |
| `streamPoweredBy` | "BackgroundColor", "borderColor", "lineHeight" | Pied de page "Optimisé par" dans la fenêtre contextuelle. |
| `streamQueueButton` | "BackgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Bouton pour indiquer quand les nouvelles notes se répandent dans une fenêtre contextuelle ouverte. |
| `userAvatar` | "hauteur", "largeur" | L’avatar de l’utilisateur authentifié, à gauche de l’éditeur de zone de texte. |

