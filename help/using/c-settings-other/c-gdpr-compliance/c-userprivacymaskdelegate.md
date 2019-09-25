---
description: Vous pouvez modifier le texte d’avertissement qui s’affiche sur les masques vidéo à l’aide de .
seo-description: Vous pouvez modifier le texte d’avertissement qui s’affiche sur les masques vidéo à l’aide de .
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Vous pouvez modifier le texte d’avertissement qui s’affiche sur les masques vidéo à l’aide de .

Ce texte existe pour se conformer au règlement sur le RMPC. Si une source ne prend pas en charge de proxy, Livefyre affiche ce texte et un masque sur le contenu, sauf si un utilisateur clique sur la vidéo et approuve le suivi potentiel à partir de cette source.

Si vous n’utilisez pas `userPrivacyMaskDelegate`, le texte par défaut suivant s’affiche :

Ajouter `userPrivacyMaskDelegate` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité de Livefyre simultanément dans le cadre d’un seul objet Livefyre.

Voici un exemple d’utilisation `userPrivacyMaskDelegate`:

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
