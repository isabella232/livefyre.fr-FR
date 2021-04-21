---
description: Les styles personnalisés sont appliqués par le biais d’un objet injecté dans le constructeur Sidenotes.
title: Identifie les styles personnalisés
exl-id: 846605b7-a21e-4600-bf17-18841d2ed96d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Identifie les styles personnalisés{#sidenotes-custom-styles}

Les styles personnalisés sont appliqués par le biais d’un objet injecté dans le constructeur Sidenotes.

Les &quot;clés&quot; sont des clés d’objet qui représentent des éléments DOM, tandis que les &quot;propriétés&quot; sont des propriétés CSS prises en charge pour la clé particulière. Par exemple, pour personnaliser le style de blockBtn (qui est le bouton qui lance la fenêtre contextuelle Sidenotes), vous devez créer un objet tel que :

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
| `anonymousAvatar` | &quot;hauteur&quot;, &quot;largeur&quot; | Image d’avatar anonyme, à gauche de l’éditeur de zone de texte. |
| `blockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | &quot;Icône de lancement&quot; placée en regard des éléments spécifiés comme pouvant être mis à part. |
| `blockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icône du lanceur lorsque l’état est principal. |
| `commentAvatar` | &quot;hauteur&quot;, &quot;largeur&quot; | Image d’avatar à gauche des notes de niveau supérieur. |
| `commentBody` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Corps de texte des notes liées. |
| `commentDisplayName` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Nom d’affichage de l’utilisateur qui a laissé une note. |
| `commentDownvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Bouton Télévoter sur une note. |
| `commentReplyExpand` | &quot;BackgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Bouton permettant d’étendre les threads avec un grand nombre de réponses. |
| `commentTags` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Balises relatives à un utilisateur sur une note. |
| `commentUpvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Bouton Mettre à jour sur une note. |
| `editorTextarea` | &quot;height&quot;, &quot;width&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Zone de saisie de zone de texte pour les notes de fin. |
| `mediaBlockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icône du lanceur de médias lorsqu’il se trouve au-dessus d’un élément multimédia (image, vidéo). |
| `mediaBlockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icône du lanceur de médias dans un état principal. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;BackgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Bouton cliquable qui affiche le nombre de Sidenotes dans la collection. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;BackgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Popover avec une brève explication des Sidenotes pour l’utilisateur. |
| `popover` | &quot;BackgroundColor&quot; | Popup qui est affiché lorsque l’icône de lancement est appelée. |
| `popoverArrowLeft` | &quot;BackgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elément flèche gauche sur la fenêtre contextuelle qui pointe vers l’élément DOM contenant une icône de lancement. |
| `popoverArrorRight` | &quot;BackgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elément de flèche vers la droite sur la fenêtre contextuelle qui pointe vers l’élément DOM contenant une icône de lancement. |
| `popoverArrowTop` | &quot;BackgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elément flèche supérieure sur la fenêtre contextuelle qui pointe vers l’élément DOM contenant une icône de lancement. |
| `replyAvatar` | &quot;hauteur&quot;, &quot;largeur&quot; | Image d’avatar à gauche des notes de niveau réponse. |
| `streamPoweredBy` | &quot;BackgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Pied de page &quot;Powered by&quot; sur la fenêtre contextuelle. |
| `streamQueueButton` | &quot;BackgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Bouton pour indiquer quand les nouvelles notes se propagent dans une fenêtre contextuelle ouverte. |
| `userAvatar` | &quot;hauteur&quot;, &quot;largeur&quot; | L’avatar de l’utilisateur authentifié, à gauche de l’éditeur de zone de texte. |
