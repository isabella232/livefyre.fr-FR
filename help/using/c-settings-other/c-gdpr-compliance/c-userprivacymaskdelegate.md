---
description: Vous pouvez modifier le texte d'avertissement qui s'affiche sur les masques vidéo à l'aide de.
seo-description: Vous pouvez modifier le texte d'avertissement qui s'affiche sur les masques vidéo à l'aide de.
seo-title: Userprivacymaskdelegate
solution: Experience Manager
title: Userprivacymaskdelegate
uuid: 8 e 5 a 2750-bf 45-4 e 70-a 5 f 9-37 f 5 e 7 c 61 f 8 e
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacymaskdelegate{#userprivacymaskdelegate}

Vous pouvez modifier le texte d&#39;avertissement qui s&#39;affiche sur les masques vidéo à l&#39;aide de.

Ce texte existe pour se conformer au règlement GDPR. Si une source ne prend pas en charge un proxy, Livefyre affiche ce texte et un masque sur le contenu, sauf si un utilisateur clique sur la vidéo et approuve le suivi potentiel de cette source.

Si vous n&#39;utilisez `userPrivacyMaskDelegate`pas, le texte par défaut suivant s&#39;affiche :

Ajoutez `userPrivacyMaskDelegate` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité Livefyre à la fois dans le cadre d&#39;un objet Livefyre.

Voici un exemple d&#39;utilisation `userPrivacyMaskDelegate`:

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
