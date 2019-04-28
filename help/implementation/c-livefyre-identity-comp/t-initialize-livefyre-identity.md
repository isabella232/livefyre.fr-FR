---
description: Le package authentique Livefyre. js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d'authentification unique.
seo-description: Le package authentique Livefyre. js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d'authentification unique.
seo-title: Initialisation de Livefyre Identity
title: Initialisation de Livefyre Identity
uuid: 9365 d 827-2734-4 a 84-bfe 7-9 be 573 b 2 b 03 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Initialisation de Livefyre Identity{#initialize-livefyre-identity}

Le package authentique Livefyre. js garantit que tous les composants sociaux de votre page peuvent découvrir une intégration d&#39;authentification unique.

Livefyre fournit `lfep-auth-delegate` un pack qui deviendra un délégué authentique approprié pour vous. L&#39;authenticité doit être fournie à un objet authdelegate qui sait comment effectuer des actions d&#39;authentification, telles que la connexion et la déconnexion.

1. Ajoutez Livefyre. js à votre webpage Web.
1. Pour indiquer à Authentic de déléguer ces actions à Livefyre Identité, ajoutez les éléments suivants :

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
