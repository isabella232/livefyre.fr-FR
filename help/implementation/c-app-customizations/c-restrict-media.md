---
description: Limitez le type de média dans le flux de l'application.
seo-description: Limitez le type de média dans le flux de l'application.
seo-title: Restreindre le support
solution: Experience Manager
title: Restreindre le support
uuid: c 470 c 985-d 221-4 f 39-8 bd 4-4 e 44 ec 14 db 95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Restreindre le support{#restrict-media}

Limitez le type de média dans le flux de l'application.

Par défaut, toutes les pièces jointes multimédia peuvent être incorporées dans les applications. Livefyre vous permet de modifier cette option pour empêcher les utilisateurs de publier des types de pièce jointe sélectionnés dans vos applications.

>[!NOTE]
>
>Partenaires Livefyre avec Incorporation de médias. Pour plus d'informations, voir Intégration de contenu > Intégration implicite. Contactez votre gestionnaire de compte technique pour toute question sur l'extension des liens ou les sources.

Cet exemple bloque YouTube et Vimeo incorpore à partir de votre flux de commentaires :

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

