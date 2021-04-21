---
description: Vous pouvez connecter un utilisateur par le biais de la console lors de l’intégration et du test de l’autorisation de débogage.
title: Débogage du délégué d’authentification
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
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
