---
description: Livefyre. require fournit un module externe qui permet d'écouter le bus
  Janrain Backplane avec authenticité.
seo-description: Livefyre. require fournit un module externe qui permet d'écouter
  le bus Janrain Backplane avec authenticité.
seo-title: Connexion de Janrain à Livefyre à l'aide de authdelegate
title: Connexion de Janrain à Livefyre à l'aide de authdelegate
uuid: 9 d 56 e 3 f 4-960 a -4108-aab 5-2795 b 0 e 71 c 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Connexion de Janrain à Livefyre à l'aide de authdelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre. require fournit un module externe qui permet d'écouter le bus Janrain Backplane avec authenticité.

Lorsqu'un message d'identité/connexion est diffusé sur le canal Backplane, auth. authenticate () est appelé avec le jeton d'authentification Livefyre de l'utilisateur. Vous devez toujours implémenter authdelegate.

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
>L'objet window. Backplane doit être défini sur votre page avant d'appeler auth. plugin avec le plug-in Livefyre Backplane. Pour vérifier que l'objet Backplane est disponible, appelez le code d'instanciation Livefyre à partir d'un rappel onready. Contactez votre contact Janrain pour déterminer quand d'autres applications peuvent utiliser l'objet Backplane.

Voici quelques exemples de manière dont un délégué authentique peut rechercher une intégration de Janrain Capture.

>[!NOTE]
>
>Votre délégué authentique varie selon votre instance Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* Rappel transmis à la méthode de connexion de votre délégué authentique
* Référence à votre variable de capture Janrain.
* : Référence à votre objet Backplane.

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

* **Finishlogout :** Rappel transmis à la méthode de connexion de votre délégué authentique.

* **window. Backplane :** Référence à votre objet Backplane.

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

Cela peut lier à quelle partie du site vous souhaitez que les utilisateurs consultent leur propre page de profil. Cet exemple imprime simplement : out the author object transmis in.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Afficher le profil

Comme Modifier le profil, il doit renvoyer à la page d'un utilisateur différente de l'utilisateur actuellement connecté. Vous pouvez l'implémenter en conséquence. Cet exemple consigne simplement le paramètre d'auteur sur la console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

