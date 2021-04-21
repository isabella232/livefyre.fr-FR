---
description: Modifiez l’icône affichée pour les utilisateurs Livefyre dans le menu déroulant mention.
title: Modifier l’icône de mention
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# Modifier `@mention` Icône {#change-mention-icon}

Modifiez l’icône affichée pour les utilisateurs de Livefyre dans le menu déroulant `@mention`.

Remplacez l’icône Livefyre utilisée dans le menu déroulant `@mention` par une icône de votre choix, ce qui vous permet d’indiquer les membres de votre communauté avec votre propre icône.

## Exemple

Pour modifier cette icône, ajoutez le fichier CSS suivant à votre feuille de style. Remplacez &quot;a0/>votre URL de ressources *par l’URL de l’image sélectionnée pour remplacer le badge Livefyre par défaut.*

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
