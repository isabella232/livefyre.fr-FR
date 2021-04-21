---
description: Livefyre.require fournit un plugin qui permet à l'auteur d'écouter le bus du Backplane de Janrain.
title: Connexion de Janrain à Livefyre à l’aide d’AuthDelegate
exl-id: d0fe0e88-5827-478b-b2ef-03f06fb3902c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# Connexion de Janrain à Livefyre à l’aide d’AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require fournit un plugin qui permet à l&#39;auteur d&#39;écouter le bus du Backplane de Janrain.

Lorsqu’un message d’identité/de connexion est diffusé sur le canal du fond de panier, la fonction auth.authenticate() est appelée pour vous avec le jeton d’authentification Livefyre de l’utilisateur. Vous devez tout de même implémenter un AuthDelegate.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>L’objet window.Backplane doit être défini sur votre page avant d’appeler auth.plugin avec le module externe Livefyre Backplane. Pour vous assurer que l’objet Backplane est disponible, appelez le code d’instanciation Livefyre à partir d’un rappel onReady. Consultez votre contact Janrain pour déterminer si d&#39;autres applications peuvent utiliser l&#39;objet Backplane.

Vous trouverez ci-dessous quelques exemples de la manière dont un délégué d’authentification peut rechercher une intégration de capture Janrain.

>[!NOTE]
>
>Votre délégué d’authentification varie en fonction de votre instance Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* Rappel transmis à la méthode de connexion du délégué d’authentification
* Référence à votre variable de capture Janrain.
* : Référence à l’objet Backplane.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

Déconnexion

* **completeLogout :** rappel transmis à la méthode de connexion du délégué d’authentification.

* **window.Backplane :** référence à l’objet Backplane.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

Modifier le profil

Ce lien peut renvoyer à n&#39;importe quelle partie du site que vous souhaitez que les utilisateurs visitent pour accéder à la vue de leur propre page de profil. Cet exemple montre comment simplement imprimer l&#39;objet auteur transmis.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Profil vue

Tout comme Modifier le Profil, ce lien doit renvoyer à la page d’un utilisateur qui diffère de celle de l’utilisateur actuellement connecté. Cela peut être mis en oeuvre comme bon vous semble. Cet exemple montre comment simplement consigner le paramètre author dans la console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```
