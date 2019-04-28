---
description: Les clients qui utilisent Janrain Capture et Backplane peuvent utiliser Livefyre Authentic pour la connexion unique (SSO), ce qui permet aux utilisateurs d'entrer immédiatement en contact avec vos applications Livefyre lorsqu'ils se connectent à votre site.
seo-description: Les clients qui utilisent Janrain Capture et Backplane peuvent utiliser Livefyre Authentic pour la connexion unique (SSO), ce qui permet aux utilisateurs d'entrer immédiatement en contact avec vos applications Livefyre lorsqu'ils se connectent à votre site.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776 e 9626-db 04-4 c 34-adfe -681 a 71 b 552 c 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

Les clients qui utilisent Janrain Capture et Backplane peuvent utiliser Livefyre Authentic pour la connexion unique (SSO), ce qui permet aux utilisateurs d&#39;entrer immédiatement en contact avec vos applications Livefyre lorsqu&#39;ils se connectent à votre site.

Pour bénéficier de cette intégration de capture/Backplane intégrée, vous devez apporter des modifications de configuration à votre application Capture et à votre intégration Livefyre. js.

>[!NOTE]
>
>Ignorez cette section si vous n&#39;utilisez pas la capture de Janrain.

Pour plus d&#39;informations, reportez-vous à [la documentation Backplane de Janrain](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Configuration de Capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Facultatif) [Ajoutez Livefyre par défaut à votre application de capture](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Créez l&#39;objet authdelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Synchronisation avec Livefyre avec Ping pour Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Étape 1 : Configuration de la capture {#section_r2f_kxt_bbb}

Livefyre a besoin de certaines informations d&#39;identification de votre application Janrain Capture.

1. Configurez l&#39;application Janrain Capture.
1. Rassemblez les informations suivantes pour Livefyre :

   * Accès à l&#39;instance de Janrain Capture.
   * Accédez à votre tableau de bord Janrain Activate.
   * Vos paramètres et informations d&#39;identification de capture.
   * Vos informations d&#39;identification.
   * Votre URL d&#39;identité.

>[!NOTE]
>
>Livefyre reçoit directement les données du CNAME ; Cette URL d&#39;identité ne peut donc pas être un enregistrement CNAME (CNAME d&#39;URL Vanity) qui résout le CNAME réel de Janrain Capture.

## Étape 2 : (Facultatif) Ajoutez Livefyre par défaut à votre application de capture {#section_z2s_txt_bbb}

Ajoutez Livefyre par défaut aux utilisateurs stockés dans votre application Capture pour vous permettre d&#39;envoyer des notifications par courrier électronique aux utilisateurs ou de les laisser automatiquement suivre les conversations que les utilisateurs ont commentées.

1. Terminer [l&#39;étape 1 : Configuration de Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Ajoutez les champs par défaut Livefyre suivants. Tous les champs sont facultatifs.

| Paramètre | Type | Description |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Chaîne | Avertissez l&#39;utilisateur lorsqu&#39;un utilisateur figure sur un article qu&#39;il suit. Peut être immédiatement, souvent ou jamais. |
| **[!UICONTROL livefyre_likes]** | Chaîne | Avertissez l&#39;utilisateur lorsqu&#39;une personne aime l&#39;une de ses publications. Peut être immédiatement, souvent ou jamais. |
| **[!UICONTROL livefyre_replies]** | Chaîne | Avertissez l&#39;utilisateur lorsque quelqu&#39;un répond à l&#39;une de ses publications. Il peut être immédiatement, souvent ou jamais. |
| **[!UICONTROL livefyre_moderator_comments]** | Chaîne | Avertissez le modérateur lorsque quelqu&#39;un de votre choix est modéré. Il peut être immédiatement ou jamais. |
| **[!UICONTROL livefyre_moderator_flags]** | Chaîne | Avertissez le modérateur lorsqu&#39;un utilisateur marque une publication sur une conversation qu&#39;ils modélisent. Peut être immédiatement, souvent ou jamais. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booléen | Demandez à l&#39;utilisateur de suivre automatiquement une conversation lorsqu&#39;elle quitte une publication. Peut être vrai ou faux. |

## Étape 3 : Création de l&#39;objet authdelegate pour l&#39;intégration de Janrain {#section_asv_vyt_bbb}

Livefyre. require fournit un module externe qui permet d&#39;écouter le bus Janrain Backplane avec authenticité.

### Connexion {#login}

Lorsqu&#39;un message d&#39;identité/connexion est diffusé sur le canal Backplane, auth. authenticate () est appelé avec le jeton d&#39;authentification Livefyre de l&#39;utilisateur. Vous devez toujours implémenter authdelegate.

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
>L&#39;objet window. Backplane doit être défini sur votre page avant d&#39;appeler auth. plugin avec le plug-in Livefyre Backplane. Pour vérifier que l&#39;objet Backplane est disponible, appelez le code d&#39;instanciation Livefyre à partir d&#39;un rappel onready. Contactez votre contact Janrain pour déterminer quand d&#39;autres applications peuvent utiliser l&#39;objet Backplane.



>[!NOTE]
>
>Votre délégué authentique varie selon votre instance Janrain.

Voici quelques exemples de manière dont un délégué authentique peut rechercher une intégration de Janrain Capture.

* `errback`: Rappel transmis à la méthode de connexion de votre délégué authentique
* `janrain`: Référence à votre variable de capture Janrain.
* `window.Backplane`: Référence à votre objet Backplane.

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

### Déconnexion {#logout}

* `finishLogout`: Rappel transmis à la méthode de connexion de votre délégué authentique.

* `window.Backplane`: Référence à votre objet Backplane.

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

### Modifier le profil {#editprofile}

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

### Afficher le profil {#viewprofile}

Comme Modifier le profil, il doit renvoyer à la page d&#39;un utilisateur différente de l&#39;utilisateur actuellement connecté. Vous pouvez l&#39;implémenter en conséquence. Cet exemple consigne simplement le paramètre d&#39;auteur sur la console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Étape 4 : Synchronisation de Livefyre avec Ping for Pull for Janrain Intégration {#section_ilv_bzt_bbb}

Conserver les profils distants Livefyre en synchronisation avec votre système de gestion des utilisateurs de capture implique une série d&#39;étapes appelée Ping pour Pull. Ce processus requiert que vous obteniez un jeton d&#39;accès valide auprès de Janrain, puis transmettez ce jeton à un point de fin spécifié à l&#39;étape 3 ci-dessous.

1. Obtenez un code d&#39;accès à partir de Janrain.

   Pour obtenir le code d&#39;accès, saisissez les informations d&#39;identification nécessaires, indiquez le type user_ type comme « user » et uuid comme uuid de l&#39;utilisateur actuel à mettre à jour. Pour plus d&#39;informations, voir [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Transmettez le code d&#39;accès d&#39;un jeton d&#39;accès. Fournissez les informations d&#39;identification nécessaires, le code d&#39;accès reçu de l&#39;étape 1 et spécifiez grant_ type sous la forme « authorization_ code ».

   Pour plus d&#39;informations, voir [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Accès au endpoint de fin « Ping to Pull Capture » de Livefyre.

   URL du point de fin : [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] où ***{networkname}*** correspond au nom du réseau fourni par Livefyre et que le jrtoken est le jeton reçu de Janrain à l&#39;étape 2.

   Une fois que vous avez atteint ce point de fin, vous recevez une réponse 202 et Livefyre lance un processus asynchrone.

## Fonctionnement de tout {#concept_mty_f31_2cb}

Pour bénéficier de cette intégration de capture/Backplane intégrée, vous devez apporter des modifications de configuration à votre application Capture et à votre intégration Livefyre. js.

Janrain envoie les messages de connexion/déconnexion réussis via le bus Backplane, sur lequel l&#39;application Livefyre, lorsqu&#39;elle est correctement configurée, écoute. Ces messages contiennent toutes les informations nécessaires pour afficher les utilisateurs de l&#39;application comme étant connectés ou déconnectés. Les développeurs peuvent afficher les messages de bus Backplane en examinant l&#39;onglet Réseau dans la console développeur de votre navigateur.

## Exemple de code de connexion {#section_ftt_tvp_mz}

Demande :

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Réponse :

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

Réponse vide :

```
Backplane.response([]);
```

## Exemple de code déconnexion {#section_t52_svp_mz}

Demande :

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Réponse :

```
Backplane.finishInit("{CHANNEL}");
```

Si ces messages ne s&#39;affichent pas dans vos requêtes réseau, Livefyre ne connaît pas les tentatives de connexion/déconnexion. Par conséquent, Livefyre ne pourra pas intégrer l&#39;utilisateur dans l&#39;application.
