---
description: Vous pouvez modifier le texte d’avertissement qui s’affiche sur les masques vidéo à l’aide de .
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Vous pouvez modifier le texte d’avertissement qui s’affiche sur les masques vidéo à l’aide de .

Ce texte existe pour se conformer au règlement sur le RMPD. Si une source ne prend pas en charge de proxy, Livefyre affiche ce texte et un masque sur le contenu, sauf si un utilisateur clique sur la vidéo et approuve le suivi potentiel à partir de cette source.

Si vous n’utilisez pas `userPrivacyMaskDelegate`, le texte par défaut suivant s’affiche :

Ajoutez `userPrivacyMaskDelegate` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité de Livefyre en même temps dans le cadre d’un seul objet Livefyre.

Voici un exemple d&#39;utilisation de `userPrivacyMaskDelegate` :

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
