---
description: Le package Auth de Livefyre.js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d’authentification unique.
seo-description: Le package Auth de Livefyre.js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d’authentification unique.
seo-title: Initialiser l'identité Livefyre
title: Initialiser l'identité Livefyre
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Initialiser l’identité Livefyre{#initialize-livefyre-identity}

Le package Auth de Livefyre.js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d’authentification unique.

Livefyre fournit un package `lfep-auth-delegate` qui fera un délégué d’authentification approprié pour vous. Auth doit être fourni un objet AuthDelegate qui sait comment effectuer des actions d&#39;authentification, telles que la connexion et la déconnexion.

1. Ajoutez Livefyre.js sur votre page Web.
1. Pour indiquer à Auth de déléguer ces actions à Livefyre Identity, ajoutez ce qui suit :

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
