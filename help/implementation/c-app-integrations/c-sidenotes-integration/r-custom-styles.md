---
description: Les styles personnalisés sont appliqués par l'intermédiaire d'un objet injecté dans le constructeur des balises Sidenotes.
seo-description: Les styles personnalisés sont appliqués par l'intermédiaire d'un objet injecté dans le constructeur des balises Sidenotes.
seo-title: Numéros personnalisés des styles personnalisés
title: Numéros personnalisés des styles personnalisés
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2-b 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Numéros personnalisés des styles personnalisés{#sidenotes-custom-styles}

Les styles personnalisés sont appliqués par l&#39;intermédiaire d&#39;un objet injecté dans le constructeur des balises Sidenotes.

Les « clés » sont des clés d&#39;objet qui représentent les éléments DOM, tandis que les « propriétés » sont prises en charge par les propriétés CSS de la clé particulière. Par exemple, pour personnaliser le style du paramètre blockbtn (qui est le bouton qui lance le fichier Popenotes), vous pouvez créer un objet tel que :

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
| `anonymousAvatar` | &#39; hauteur &#39;,&#39;largeur &#39; | Image d&#39;avatar anonyme, à gauche de l&#39;éditeur de zone de texte. |
| `blockBtn` | &#39; Fontcolor &#39;,&#39;fontsize &#39;,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top &#39; | L&#39;icône « Lanceur » placée en regard des éléments spécifiés comme pouvant être identifiés. |
| `blockBtnActive` | &#39; Fontcolor &#39;,&#39;fontsize &#39;,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top &#39; | Icône Lanceur lorsqu&#39;elle est activée. |
| `commentAvatar` | &#39; hauteur &#39;,&#39;largeur &#39; | Image d&#39;avatar à gauche des notes de niveau supérieur. |
| `commentBody` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39; | Corps de texte des notes de threads. |
| `commentDisplayName` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39; | Nom d&#39;affichage de l&#39;utilisateur qui a quitté une note. |
| `commentDownvote` | &#39; Fontcolor &#39;,&#39;fontsize &#39; | Bouton Downvote sur une note. |
| `commentReplyExpand` | &#39; Backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39; | Bouton permettant de développer des threads avec un grand nombre de réponses. |
| `commentTags` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39; | Balises relatives à un utilisateur sur une note. |
| `commentUpvote` | &#39; Fontcolor &#39;,&#39;fontsize &#39; | Bouton Upvote sur une note. |
| `editorTextarea` | &#39; height &#39;,&#39;width &#39;,&#39;fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39; | Zone de saisie de zone de texte pour le renvoi des notes. |
| `mediaBlockBtn` | &#39; Fontcolor &#39;,&#39;fontsize &#39;,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top &#39; | Icône de lancement de média lorsqu&#39;elle est placée au-dessus d&#39;un élément multimédia (img, vidéo). |
| `mediaBlockBtnActive` | &#39; Fontcolor &#39;,&#39;fontsize &#39;,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top &#39; | Icône de lancement de média à l&#39;état actif. |
| `numSidenotes` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39;,&#39;backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;height &#39;,&#39;width &#39; | Bouton cliquable qui indique le nombre de mentions annexes dans la collection. |
| `numSidenotesPopover` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39;,&#39;backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;height &#39;,&#39;width &#39; | Fenêtre contextuelle avec une brève explication des commentaires de l&#39;utilisateur. |
| `popover` | &#39; Backgroundcolor &#39; | Fenêtre contextuelle qui est levée lorsque l&#39;icône de lancement est appelée. |
| `popoverArrowLeft` | &#39; Backgroundimage &#39;,&#39;hauteur &#39;,&#39;left &#39;,&#39;right &#39;,&#39;top &#39;,&#39;width &#39; | Elément fléché gauche sur la fenêtre contextuelle qui pointe vers l&#39;élément DOM contenant une icône de lancement. |
| `popoverArrorRight` | &#39; Backgroundimage &#39;,&#39;hauteur &#39;,&#39;left &#39;,&#39;right &#39;,&#39;top &#39;,&#39;width &#39; | Elément fléché droit sur la fenêtre contextuelle qui pointe vers l&#39;élément DOM contenant une icône de lanceur. |
| `popoverArrowTop` | &#39; Backgroundimage &#39;,&#39;hauteur &#39;,&#39;left &#39;,&#39;right &#39;,&#39;top &#39;,&#39;width &#39; | Elément fléché haut sur la fenêtre contextuelle qui pointe vers l&#39;élément DOM contenant une icône de lanceur. |
| `replyAvatar` | &#39; hauteur &#39;,&#39;largeur &#39; | Image d&#39;avatar à gauche des notes de niveau de réponse. |
| `streamPoweredBy` | &#39; Backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;lineheight &#39; | « Piloté par » sur la fenêtre contextuelle. |
| `streamQueueButton` | &#39; Backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsize &#39;,&#39;fontweight &#39;,&#39;lineheight &#39; | Bouton pour indiquer quand les nouvelles notes enchaînent dans une fenêtre contextuelle ouverte. |
| `userAvatar` | &#39; hauteur &#39;,&#39;largeur &#39; | Image d&#39;avatar d&#39;un utilisateur authentifié, à gauche de l&#39;éditeur de zone de texte. |

