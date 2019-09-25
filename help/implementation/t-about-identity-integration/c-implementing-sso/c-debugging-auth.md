---
description: Vous pouvez connecter un utilisateur par le biais de la console pendant l’intégration et les tests pour l’autorisation de débogage.
seo-description: Vous pouvez connecter un utilisateur par le biais de la console pendant l’intégration et les tests pour l’autorisation de débogage.
seo-title: Débogage du délégué d’authentification
solution: Experience Manager
title: Débogage du délégué d’authentification
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Débogage du délégué d’authentification{#debugging-auth-delegate}

Vous pouvez connecter un utilisateur par le biais de la console pendant l’intégration et les tests pour l’autorisation de débogage.

Connectez un utilisateur via la console à l’aide du jeton `auth.authenticate` (jeton) suivant et transmettez un jeton utilisateur Livefyre pour authentifier les utilisateurs de la page.

Vous pouvez également modifier l’exemple ci-dessus et ajouter le fragment de code suivant en ligne dans votre code JavaScript pour connecter rapidement un utilisateur à Livefyre (nécessite une référence à l’authentification).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

