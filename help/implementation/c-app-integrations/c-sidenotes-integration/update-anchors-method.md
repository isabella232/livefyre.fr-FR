---
description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# updateAnchors, méthode {#updateAnchorsMethod}

Utilisez la méthode updateAnchors pour ajouter dynamiquement du contenu mis en place sur la page.

Cette méthode est utile pour la pagination, ou dans d’autres cas où du contenu pouvant être mis à part est ajouté dynamiquement à la page. Cette méthode définit de nouvelles ancres pour les éléments correspondants et prend un seul argument : newSélecteurs.

**newSélecteurs**. Sélecteurs à ajouter aux Sidenotes. Il peut s’agir d’une chaîne de sélecteur, d’un objet jQuery ou d’un tableau d’éléments (tous les types acceptés par l’argument sélecteurs transmis lors de la construction de l’application).
Format:

```
app.updateAnchors(newSelectors);
```

Exemple :

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
