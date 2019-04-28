---
description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-title: Méthode updateanchors
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Méthode updateanchors {#updateAnchorsMethod}

Utilisez la méthode updateanchors pour ajouter dynamiquement du contenu sidenoted à la page.

Cette méthode est utile pour la pagination ou dans d&#39;autres cas où le contenu sidenote est ajouté dynamiquement à la page. Cette méthode définit de nouveaux ancrages pour les éléments correspondants et utilise un seul argument : Newselectors.

**Newselectors**. Sélecteurs à ajouter aux commentaires annexes. Il peut s&#39;agir d&#39;une chaîne de sélecteur, d&#39;un objet jquery ou d&#39;un tableau d&#39;éléments (tous les types acceptés par l&#39;argument sélecteurs transmis lors de la construction de l&#39;application).
Format :

```
app.updateAnchors(newSelectors);
```

Exemple :

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
