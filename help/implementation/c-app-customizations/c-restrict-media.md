---
description: Limitez le type de média entrant dans le flux d’application.
seo-description: Limitez le type de média entrant dans le flux d’application.
seo-title: Restreindre le média
solution: Experience Manager
title: Restreindre le média
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Restreindre le média{#restrict-media}

Limitez le type de média entrant dans le flux d’application.

Par défaut, toutes les pièces jointes peuvent être incorporées dans des applications. Livefyre vous permet de modifier cette option pour empêcher les utilisateurs de publier certains types de pièces jointes dans vos applications.

>[!NOTE]
>
>Livefyre travaille en partenariat avec Embetly pour l&#39;intégration des médias. Pour plus d’informations, voir Intégration de contenu > Intégration héritée. Contactez votre gestionnaire de compte technique pour toute question concernant l&#39;extension des liens ou les sources.

Cet exemple bloque l’intégration de YouTube et de Vimeo dans votre flux de commentaires :

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

Lors du chargement de la conversation :

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

