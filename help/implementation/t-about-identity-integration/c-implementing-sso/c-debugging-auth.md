---
description: Vous pouvez enregistrer un utilisateur dans la console pendant l'intégration
  et le test pour déboguer l'autorisation.
seo-description: Vous pouvez enregistrer un utilisateur dans la console pendant l'intégration
  et le test pour déboguer l'autorisation.
seo-title: Débogage du délégué authentique
solution: Experience Manager
title: Débogage du délégué authentique
uuid: fb 0 c 7396-190 e -4 dc 9-bf 26-23 dde 9 efd 45 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Débogage du délégué authentique{#debugging-auth-delegate}

Vous pouvez enregistrer un utilisateur dans la console pendant l'intégration et le test pour déboguer l'autorisation.

Enregistrez un utilisateur dans la console à l'aide de ce qui suit `auth.authenticate` (jeton) et transmettez un jeton utilisateur Livefyre pour authentifier les utilisateurs sur la page.

Vous pouvez également modifier l'exemple illustré ci-dessus et ajouter le fragment de code suivant dans le code JavaScript pour enregistrer rapidement un utilisateur dans Livefyre (une référence à l'authenticité est nécessaire).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

