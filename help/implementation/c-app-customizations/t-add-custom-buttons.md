---
description: Ajoutez des actions personnalisées à vos applications Livefyre.
seo-description: Ajoutez des actions personnalisées à vos applications Livefyre.
seo-title: Ajouter des boutons personnalisés
solution: Experience Manager
title: Ajouter des boutons personnalisés
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Ajouter des boutons personnalisés{#add-custom-buttons}

Ajoutez des actions personnalisées à vos applications Livefyre.

Livefyre vous permet d’ajouter des boutons personnalisés en regard des boutons d’action existants (comme **[!UICONTROL Share]**, et **[!UICONTROL Flag]**) sur un élément de contenu.

Utilisez l’argument mobile pour définir si le bouton doit être affiché sur les périphériques mobiles.

Par exemple, pour ajouter un bouton d’action personnalisé pour l’interface de votre périphérique mobile :

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

1. Transmettez un argument supplémentaire dans l’objet ConvConfig nommé actionButtons, contenant un tableau d’objets décrivant chaque bouton que vous souhaitez ajouter.
1. Définissez une clé pour le texte à afficher pour chaque bouton.
1. Ajoutez un rappel qui sera appelé lors d’un événement click pour chaque bouton.

Le rappel est appelé avec un objet avec deux clés : `authorId` et `contentId`.
