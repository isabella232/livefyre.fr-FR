---
description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur
  votre site.
seo-description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre
  sur votre site.
seo-title: Méthode updateanchors
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Méthode updateanchors {#updateAnchorsMethod}

Utilisez la méthode updateanchors pour ajouter dynamiquement du contenu sidenoted à la page.

Cette méthode est utile pour la pagination ou dans d'autres cas où le contenu sidenote est ajouté dynamiquement à la page. Cette méthode définit de nouveaux ancrages pour les éléments correspondants et utilise un seul argument : Newselectors.

**Newselectors**. Sélecteurs à ajouter aux commentaires annexes. Il peut s'agir d'une chaîne de sélecteur, d'un objet jquery ou d'un tableau d'éléments (tous les types acceptés par l'argument sélecteurs transmis lors de la construction de l'application).
Format :

```
app.updateAnchors(newSelectors);
```

Exemple :

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
