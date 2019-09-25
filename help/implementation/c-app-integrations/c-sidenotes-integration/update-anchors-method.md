---
description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-title: updateAnchors, méthode
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# updateAnchors, méthode {#updateAnchorsMethod}

Utilisez la méthode updateAnchors pour ajouter dynamiquement du contenu sidenoté à la page.

Cette méthode s’avère utile pour la pagination ou dans d’autres cas où du contenu localisable est ajouté dynamiquement à la page. Cette méthode définit de nouvelles ancres pour les éléments correspondants et utilise un seul argument : newSélecteurs.

**newSélecteurs**. Sélecteurs à ajouter aux Sidenotes. Il peut s’agir d’une chaîne de sélecteur, d’un objet jQuery ou d’un tableau d’éléments (tous les types acceptés par l’argument sélecteurs transmis lors de la construction de l’application).
Format:

```
app.updateAnchors(newSelectors);
```

Exemple :

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
