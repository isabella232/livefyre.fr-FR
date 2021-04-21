---
description: Pour authentifier un utilisateur avec Livefyre via un flux non déclenché par une application Livefyre, Livefyre vous recommande de mettre en oeuvre la méthode forEveryAuthentication sur votre objet AuthDelegate.
title: Implémentation d’une authentification unique
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Implémentation de l’authentification unique {#implementing-sso}

Pour authentifier un utilisateur avec Livefyre via un flux non déclenché par une application Livefyre, Livefyre vous recommande de mettre en oeuvre la méthode forEveryAuthentication sur votre objet AuthDelegate.

Cette fonction sera appelée lorsque `authDelegate` est transmis à `auth.delegate` et sera transmise à une fonction d&#39;authentification qui peut être transmise plusieurs fois. Cette méthode fournit une inversion du contrôle pour les événements d&#39;authentification de sorte que votre `AuthDelegateobject` puisse être autonome sans nécessiter une référence globale à l&#39;authentification.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre utilise des jetons d&#39;utilisateur pour coordonner l&#39;authentification. Par conséquent, ce jeton doit être renvoyé par votre service d’identité pour authentifier un utilisateur auprès de Livefyre. Pour savoir comment créer un jeton d’utilisateur Livefyre, consultez Création d’un jeton d’authentification d’utilisateur.

>[!NOTE]
>
>Après une connexion réussie, l’authentification crée une session pour l’utilisateur et tente de charger la session d’un utilisateur lors de l’actualisation et du rechargement de la page. `auth.logout()` effacera cette session. Cela signifie qu’il n’est pas nécessaire de gérer la session d’un utilisateur indépendamment de l’autorisation.
