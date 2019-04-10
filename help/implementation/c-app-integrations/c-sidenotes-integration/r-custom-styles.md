---
description: Les styles personnalisés sont appliqués par l'intermédiaire d'un objet
  injecté dans le constructeur des balises Sidenotes.
seo-description: Les styles personnalisés sont appliqués par l'intermédiaire d'un
  objet injecté dans le constructeur des balises Sidenotes.
seo-title: Numéros personnalisés des styles personnalisés
title: Numéros personnalisés des styles personnalisés
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2-b 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Numéros personnalisés des styles personnalisés{#sidenotes-custom-styles}

Les styles personnalisés sont appliqués par l'intermédiaire d'un objet injecté dans le constructeur des balises Sidenotes.

Les « clés » sont des clés d'objet qui représentent les éléments DOM, tandis que les « propriétés » sont prises en charge par les propriétés CSS de la clé particulière. Par exemple, pour personnaliser le style du paramètre blockbtn (qui est le bouton qui lance le fichier Popenotes), vous pouvez créer un objet tel que :

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
| `anonymousAvatar` | ' hauteur ','largeur ' | Image d'avatar anonyme, à gauche de l'éditeur de zone de texte. |
| `blockBtn` | ' Fontcolor ','fontsize ','left ','position ','right ','top ' | L'icône « Lanceur » placée en regard des éléments spécifiés comme pouvant être identifiés. |
| `blockBtnActive` | ' Fontcolor ','fontsize ','left ','position ','right ','top ' | Icône Lanceur lorsqu'elle est activée. |
| `commentAvatar` | ' hauteur ','largeur ' | Image d'avatar à gauche des notes de niveau supérieur. |
| `commentBody` | ' Fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ' | Corps de texte des notes de threads. |
| `commentDisplayName` | ' Fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ' | Nom d'affichage de l'utilisateur qui a quitté une note. |
| `commentDownvote` | ' Fontcolor ','fontsize ' | Bouton Downvote sur une note. |
| `commentReplyExpand` | ' Backgroundcolor ','bordercolor ','borderwidth ','fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ' | Bouton permettant de développer des threads avec un grand nombre de réponses. |
| `commentTags` | ' Fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ' | Balises relatives à un utilisateur sur une note. |
| `commentUpvote` | ' Fontcolor ','fontsize ' | Bouton Upvote sur une note. |
| `editorTextarea` | ' height ','width ','fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ' | Zone de saisie de zone de texte pour le renvoi des notes. |
| `mediaBlockBtn` | ' Fontcolor ','fontsize ','left ','position ','right ','top ' | Icône de lancement de média lorsqu'elle est placée au-dessus d'un élément multimédia (img, vidéo). |
| `mediaBlockBtnActive` | ' Fontcolor ','fontsize ','left ','position ','right ','top ' | Icône de lancement de média à l'état actif. |
| `numSidenotes` | ' Fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ','backgroundcolor ','bordercolor ','borderwidth ','height ','width ' | Bouton cliquable qui indique le nombre de mentions annexes dans la collection. |
| `numSidenotesPopover` | ' Fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ','backgroundcolor ','bordercolor ','borderwidth ','height ','width ' | Fenêtre contextuelle avec une brève explication des commentaires de l'utilisateur. |
| `popover` | ' Backgroundcolor ' | Fenêtre contextuelle qui est levée lorsque l'icône de lancement est appelée. |
| `popoverArrowLeft` | ' Backgroundimage ','hauteur ','left ','right ','top ','width ' | Elément fléché gauche sur la fenêtre contextuelle qui pointe vers l'élément DOM contenant une icône de lancement. |
| `popoverArrorRight` | ' Backgroundimage ','hauteur ','left ','right ','top ','width ' | Elément fléché droit sur la fenêtre contextuelle qui pointe vers l'élément DOM contenant une icône de lanceur. |
| `popoverArrowTop` | ' Backgroundimage ','hauteur ','left ','right ','top ','width ' | Elément fléché haut sur la fenêtre contextuelle qui pointe vers l'élément DOM contenant une icône de lanceur. |
| `replyAvatar` | ' hauteur ','largeur ' | Image d'avatar à gauche des notes de niveau de réponse. |
| `streamPoweredBy` | ' Backgroundcolor ','bordercolor ','lineheight ' | « Piloté par » sur la fenêtre contextuelle. |
| `streamQueueButton` | ' Backgroundcolor ','bordercolor ','borderwidth ','fontcolor ','fontfamily ','fontsize ','fontweight ','lineheight ' | Bouton pour indiquer quand les nouvelles notes enchaînent dans une fenêtre contextuelle ouverte. |
| `userAvatar` | ' hauteur ','largeur ' | Image d'avatar d'un utilisateur authentifié, à gauche de l'éditeur de zone de texte. |

