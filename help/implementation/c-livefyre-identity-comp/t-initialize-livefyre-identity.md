---
description: Le package Auth de Livefyre.js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d’authentification unique.
seo-description: Le package Auth de Livefyre.js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d’authentification unique.
seo-title: Initialiser l'identité Livefyre
title: Initialiser l'identité Livefyre
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Initialiser l'identité Livefyre{#initialize-livefyre-identity}

Le package Auth de Livefyre.js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d’authentification unique.

Livefyre fournit un `lfep-auth-delegate` package qui fera en sorte qu’un délégué d’authentification approprié vous soit affecté. Auth doit disposer d’un objet AuthDelegate qui sait exécuter des actions d’authentification, telles que la connexion et la déconnexion.

1. Ajoutez Livefyre.js à votre page Web.
1. Pour indiquer à Auth de déléguer ces actions à l’identité Livefyre, ajoutez ce qui suit :

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
