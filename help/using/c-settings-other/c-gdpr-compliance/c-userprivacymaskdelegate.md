---
description: Vous pouvez modifier le texte d'avertissement qui s'affiche sur les masques
  vidéo à l'aide de.
seo-description: Vous pouvez modifier le texte d'avertissement qui s'affiche sur les
  masques vidéo à l'aide de.
seo-title: Userprivacymaskdelegate
solution: Experience Manager
title: Userprivacymaskdelegate
uuid: 8 e 5 a 2750-bf 45-4 e 70-a 5 f 9-37 f 5 e 7 c 61 f 8 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacymaskdelegate{#userprivacymaskdelegate}

Vous pouvez modifier le texte d'avertissement qui s'affiche sur les masques vidéo à l'aide de.

Ce texte existe pour se conformer au règlement GDPR. Si une source ne prend pas en charge un proxy, Livefyre affiche ce texte et un masque sur le contenu, sauf si un utilisateur clique sur la vidéo et approuve le suivi potentiel de cette source.

Si vous n'utilisez `userPrivacyMaskDelegate`pas, le texte par défaut suivant s'affiche :

Ajoutez `userPrivacyMaskDelegate` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité Livefyre à la fois dans le cadre d'un objet Livefyre.

Voici un exemple d'utilisation `userPrivacyMaskDelegate`:

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
