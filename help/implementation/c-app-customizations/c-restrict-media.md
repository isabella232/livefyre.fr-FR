---
description: Limitez le type de média entrant dans le flux d’application.
title: Restreindre le média
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Restreindre le média{#restrict-media}

Limitez le type de média entrant dans le flux d’application.

Par défaut, toutes les pièces jointes peuvent être incorporées dans des applications. Livefyre vous permet de modifier cette option pour empêcher les utilisateurs de publier certains types de pièces jointes dans vos applications.

>[!NOTE]
>
>Livefyre travaille en partenariat avec Embetly pour l&#39;intégration des médias. Pour plus d’informations, voir Intégration de contenu > Intégration héritée. Contactez votre gestionnaire de compte technique pour toute question concernant l&#39;extension des liens ou les sources.

Cet exemple bloque les intégrations YouTube et Vimeo de votre flux de commentaires :

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
