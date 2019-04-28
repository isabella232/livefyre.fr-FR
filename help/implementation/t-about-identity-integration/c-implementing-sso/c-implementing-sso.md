---
description: Pour authentifier un utilisateur avec Livefyre par le biais d'un flux non déclenché par une application Livefyre, Livefyre vous conseille de mettre en œuvre la méthode foreachauthentication sur votre objet authdelegate.
seo-description: Pour authentifier un utilisateur avec Livefyre par le biais d'un flux non déclenché par une application Livefyre, Livefyre vous conseille de mettre en œuvre la méthode foreachauthentication sur votre objet authdelegate.
seo-title: Implémentation de la fonction SSO
solution: Experience Manager
title: Implémentation de la fonction SSO
uuid: c 96 d 456 c-b 1 ac -40 e 0-8 d 18-224652 b 9697 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implémentation de la fonction SSO{#implementing-sso}

Pour authentifier un utilisateur avec Livefyre par le biais d&#39;un flux non déclenché par une application Livefyre, Livefyre vous conseille de mettre en œuvre la méthode foreachauthentication sur votre objet authdelegate.

Cette action sera appelée lorsque la `authDelegate` transmission est transmise `auth.delegate`et transmet une fonction authentifiée qui peut être transmise plusieurs fois. Cette méthode fournit une inversion de contrôle pour les événements d&#39;authentification afin que vous `AuthDelegateobject` puissiez être autonome sans qu&#39;une référence globale soit nécessaire à l&#39;authentique.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre repose sur les jetons utilisateur pour coordonner l&#39;authentification. Par conséquent, ce jeton doit être renvoyé par votre service d&#39;identité pour authentifier un utilisateur avec Livefyre. Pour savoir comment créer un jeton d&#39;utilisateur Livefyre, reportez-vous à la page Création d&#39;un jeton d&#39;authentification utilisateur.

>[!NOTE]
>
>Après une connexion réussie, authentique créera une session pour l&#39;utilisateur et tente de charger la session d&#39;un utilisateur lors de l&#39;actualisation et du rechargement de la page. `auth.logout()` va effacer cette session. Cela signifie qu&#39;il n&#39;est pas nécessaire de gérer la session d&#39;un utilisateur indépendamment de l&#39;autorisation.

