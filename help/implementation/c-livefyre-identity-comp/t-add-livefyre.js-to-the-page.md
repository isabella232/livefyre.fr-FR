---
description: Livefyre.js est une petite bibliothèque de base qui fournit une authentification pour les applications sur votre site.
title: Ajouter Livefyre.js à la page
exl-id: 4c5dfb31-b7e5-48f7-826c-cddbee06d876
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# Ajouter Livefyre.js à la page{#add-livefyre-js-to-the-page}

Livefyre.js est une petite bibliothèque de base qui fournit une authentification pour les applications sur votre site.

Pour activer l&#39;authentification :

1. Ajoutez Livefyre.js à l’élément `<head>` de votre page Web ou modèle de site Web.
1. Ajoutez l’un des éléments suivants sur votre page :

   * `globalwindow.Livefyre` la variable
   * `Livefyre.require` pour charger d&#39;autres packs Livefyre à la demande

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```
