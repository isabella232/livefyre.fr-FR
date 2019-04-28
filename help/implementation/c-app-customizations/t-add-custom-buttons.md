---
description: Ajoutez des actions personnalisées à vos applications Livefyre.
seo-description: Ajoutez des actions personnalisées à vos applications Livefyre.
seo-title: Ajout de boutons personnalisés
solution: Experience Manager
title: Ajout de boutons personnalisés
uuid: 27 d 24 c 21-d 83 f -49 df -9 b 3 f -15 d 7 abbd 2 bd 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Ajout de boutons personnalisés{#add-custom-buttons}

Ajoutez des actions personnalisées à vos applications Livefyre.

Livefyre vous permet d&#39;ajouter des boutons personnalisés à côté des boutons d&#39;action existants (tels **[!UICONTROL Share]** que et **[!UICONTROL Flag]**) sur un élément de contenu.

Utilisez l&#39;argument mobile pour définir si le bouton s&#39;affichera sur les périphériques mobiles.

Par exemple, pour ajouter un bouton d&#39;action personnalisé à votre interface de périphérique mobile :

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. Transmettez un argument supplémentaire dans l&#39;objet convconfig nommé actionbuttons, contenant un tableau d&#39;objets décrivant chaque bouton à ajouter.
1. Définissez une clé pour le texte à afficher pour chaque bouton.
1. Ajoutez un rappel qui sera appelé lors d&#39;un événement click pour chaque bouton.

Le rappel est appelé avec un objet avec deux clés : `authorId` et `contentId`.
