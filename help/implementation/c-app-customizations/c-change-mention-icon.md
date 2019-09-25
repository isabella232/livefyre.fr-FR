---
description: Modifiez l’icône affichée pour les utilisateurs Livefyre dans le menu déroulant @mention.
seo-description: Modifiez l’icône affichée pour les utilisateurs Livefyre dans le menu déroulant mention.
seo-title: Modifier l’icône de mention
solution: Experience Manager
title: Modifier l’icône de @mention
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Modifier l’ `@mention` icône {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

Remplacez l’icône Livefyre utilisée dans le menu `@mention` déroulant par une icône de votre choix, ce qui vous permet d’indiquer aux membres de votre communauté votre propre icône.

## Exemple

Pour modifier cette icône, ajoutez le fichier CSS suivant à votre feuille de style. Remplacez &lt;*votre ressource*&gt; url par l’URL de l’image sélectionnée pour remplacer le badge Livefyre par défaut.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
