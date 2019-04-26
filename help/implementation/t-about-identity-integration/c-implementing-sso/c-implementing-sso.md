---
description: Pour authentifier un utilisateur avec Livefyre par le biais d'un flux
  non déclenché par une application Livefyre, Livefyre vous conseille de mettre en
  œuvre la méthode foreachauthentication sur votre objet authdelegate.
seo-description: Pour authentifier un utilisateur avec Livefyre par le biais d'un
  flux non déclenché par une application Livefyre, Livefyre vous conseille de mettre
  en œuvre la méthode foreachauthentication sur votre objet authdelegate.
seo-title: Implémentation de la fonction SSO
solution: Experience Manager
title: Implémentation de la fonction SSO
uuid: c 96 d 456 c-b 1 ac -40 e 0-8 d 18-224652 b 9697 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implémentation de la fonction SSO{#implementing-sso}

Pour authentifier un utilisateur avec Livefyre par le biais d'un flux non déclenché par une application Livefyre, Livefyre vous conseille de mettre en œuvre la méthode foreachauthentication sur votre objet authdelegate.

Cette action sera appelée lorsque la `authDelegate` transmission est transmise `auth.delegate`et transmet une fonction authentifiée qui peut être transmise plusieurs fois. Cette méthode fournit une inversion de contrôle pour les événements d'authentification afin que vous `AuthDelegateobject` puissiez être autonome sans qu'une référence globale soit nécessaire à l'authentique.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre repose sur les jetons utilisateur pour coordonner l'authentification. Par conséquent, ce jeton doit être renvoyé par votre service d'identité pour authentifier un utilisateur avec Livefyre. Pour savoir comment créer un jeton d'utilisateur Livefyre, reportez-vous à la page Création d'un jeton d'authentification utilisateur.

>[!NOTE]
>
>Après une connexion réussie, authentique créera une session pour l'utilisateur et tente de charger la session d'un utilisateur lors de l'actualisation et du rechargement de la page. `auth.logout()` va effacer cette session. Cela signifie qu'il n'est pas nécessaire de gérer la session d'un utilisateur indépendamment de l'autorisation.

