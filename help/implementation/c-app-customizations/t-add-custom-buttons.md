---
description: Ajoutez des actions personnalisées sur vos applications Livefyre.
seo-description: Ajoutez des actions personnalisées sur vos applications Livefyre.
seo-title: Ajouter des boutons personnalisés
solution: Experience Manager
title: Ajouter des boutons personnalisés
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Ajouter des boutons personnalisés{#add-custom-buttons}

Ajoutez des actions personnalisées sur vos applications Livefyre.

Livefyre vous permet d’ajouter des boutons personnalisés en regard des boutons d’action existants (tels que **[!UICONTROL Share]** et **[!UICONTROL Flag]**) sur un élément de contenu.

Utilisez l’argument mobile pour définir si le bouton doit s’afficher sur les périphériques mobiles.

Par exemple, pour ajouter un bouton d’action personnalisée pour l’interface de votre périphérique mobile :

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

1. Transférez un argument supplémentaire dans l’objet ConvConfig appelé actionButtons, contenant un tableau d’objets décrivant chaque bouton à ajouter.
1. Définissez une clé pour le texte à afficher pour chaque bouton.
1. Ajoutez un rappel qui sera appelé sur un événement de clic pour chaque bouton.

Le rappel est appelé avec un objet avec deux clés : `authorId` et `contentId`.
