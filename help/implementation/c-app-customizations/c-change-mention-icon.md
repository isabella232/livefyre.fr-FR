---
description: Modifiez l’icône affichée pour les utilisateurs Livefyre dans le menu déroulant @mention.
seo-description: Modifiez l’icône affichée pour les utilisateurs Livefyre dans le menu déroulant mention.
seo-title: Modifier l’icône de mention
solution: Experience Manager
title: Modifier l’icône de @mention
uuid: a 395 f 4 ff-a 774-454 a -8 d 94-4 a 3371 d 8 cc 2 c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Change `@mention` Icon {#change-mention-icon}

Modifiez l&#39;icône affichée pour les utilisateurs Livefyre dans le menu `@mention` déroulant.

Remplacez l&#39;icône Livefyre utilisée dans le menu `@mention` déroulant par une icône de votre choix, ce qui vous permet d&#39;indiquer les membres de la communauté à votre propre icône.

## Exemple

Pour modifier cette icône, ajoutez la feuille CSS suivante à votre feuille de style. Remplacez &lt;*votre ressource*&gt; url par l&#39;URL de l&#39;image sélectionnée pour remplacer le badge Livefyre par défaut.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
