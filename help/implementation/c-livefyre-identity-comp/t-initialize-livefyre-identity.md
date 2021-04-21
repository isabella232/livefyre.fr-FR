---
description: Le package Auth de Livefyre.js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d’authentification unique.
title: Initialiser l'identité Livefyre
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
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
