---
description: Ajoutez des actions personnalisées sur vos applications Livefyre.
title: Ajouter des boutons personnalisés
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
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
