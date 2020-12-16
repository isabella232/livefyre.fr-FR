---
description: Vous pouvez connecter un utilisateur par le biais de la console lors de l’intégration et du test de l’autorisation de débogage.
seo-description: Vous pouvez connecter un utilisateur par le biais de la console lors de l’intégration et du test de l’autorisation de débogage.
seo-title: Débogage du délégué d’authentification
solution: Experience Manager
title: Débogage du délégué d’authentification
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Débogage du délégué Auth{#debugging-auth-delegate}

Vous pouvez connecter un utilisateur par le biais de la console lors de l’intégration et du test de l’autorisation de débogage.

Connectez un utilisateur via la console à l’aide du `auth.authenticate` (jeton) suivant et transmettez un jeton d’utilisateur Livefyre pour authentifier les utilisateurs sur la page.

Vous pouvez également modifier l’exemple ci-dessus et ajouter le fragment de code suivant en ligne dans votre code JavaScript pour connecter rapidement un utilisateur à Livefyre (requiert une référence à l’authentification).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

