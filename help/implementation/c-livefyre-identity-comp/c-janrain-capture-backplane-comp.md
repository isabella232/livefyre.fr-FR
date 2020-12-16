---
description: Les clients qui utilisent la capture et le fond de panier de Janrain peuvent utiliser l’authentification Livefyre pour l’authentification unique (SSO), ce qui permet aux utilisateurs de contacter immédiatement vos applications Livefyre lorsqu’ils se connectent à votre site.
seo-description: Les clients qui utilisent la capture et le fond de panier de Janrain peuvent utiliser l’authentification Livefyre pour l’authentification unique (SSO), ce qui permet aux utilisateurs de contacter immédiatement vos applications Livefyre lorsqu’ils se connectent à votre site.
seo-title: Capture/fond de panier en janvier
solution: Experience Manager
title: Capture/fond de panier en janvier
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 1%

---


# Capture/fond de panier de janvier{#janrain-capture-backplane}

Les clients qui utilisent la capture et le fond de panier de Janrain peuvent utiliser l’authentification Livefyre pour l’authentification unique (SSO), ce qui permet aux utilisateurs de contacter immédiatement vos applications Livefyre lorsqu’ils se connectent à votre site.

Pour bénéficier de cette intégration Capture/Backplane intégrée, vous devez modifier la configuration de votre application Capture et de votre intégration Livefyre.js.

>[!NOTE]
>
>Ignorez cette section si vous n’utilisez pas Janrain Capture.

Pour plus d’informations, voir la [documentation de Janrain’s Backplane](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Configuration de la capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Facultatif) [Ajoutez par défaut Livefyre à votre application Capture](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Créez l’objet AuthDelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Synchronisation avec Livefyre avec Ping pour Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Étape 1 : Configurer la capture {#section_r2f_kxt_bbb}

Livefyre a besoin de certaines informations d&#39;identification de votre application Janrain Capture.

1. Configurez l’application Janrain Capture.
1. Rassemblez les informations suivantes pour Livefyre :

   * Accédez à votre instance de capture Janrain.
   * Accès à votre tableau de bord d&#39;engagement Janrain.
   * Vos paramètres et informations d’identification Capturer.
   * Vos informations d’identification Interagir.
   * Votre URL d&#39;identité.

>[!NOTE]
>
>Livefyre reçoit directement les données du CNAME ; par conséquent, cette URL d’identité ne peut pas être un enregistrement CNAMEd (un CNAME d’URL vanity) qui correspond au CNAME réel de Janrain Capture.

## Étape 2 : (Facultatif) Ajoutez les valeurs par défaut de Livefyre sur votre application de capture {#section_z2s_txt_bbb}

Ajouter Livefyre permet par défaut aux utilisateurs stockés dans votre application Capture d’envoyer des notifications électroniques aux utilisateurs ou de les autoriser à suivre automatiquement les conversations sur lesquelles les utilisateurs commentent.

1. Terminer [Étape 1 : Configurer Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Ajoutez les champs par défaut suivants pour Livefyre. Tous les champs sont facultatifs.

| Paramètre | Type | Description |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Chaîne | Avertissez l’utilisateur lorsqu’un utilisateur commente un article qu’il suit. Peut être immédiatement, souvent, ou jamais. |
| **[!UICONTROL livefyre_likes]** | Chaîne | Avertissez l’utilisateur lorsqu’un utilisateur aime une de ses publications. Peut être immédiatement, souvent, ou jamais. |
| **[!UICONTROL livefyre_replies]** | Chaîne | Avertissez l’utilisateur lorsqu’un utilisateur répond à l’une de ses publications. Peut être immédiatement, souvent ou jamais. |
| **[!UICONTROL livefyre_moderator_comments]** | Chaîne | Avertissez le modérateur lorsqu’une personne commente une conversation qu’elle modérait. Cela peut être immédiat, fréquent ou jamais. |
| **[!UICONTROL livefyre_moderator_flags]** | Chaîne | Avertissez le modérateur lorsqu’un utilisateur marque une publication sur une conversation qu’il modérait.Cela peut être immédiat, fréquent ou jamais. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booléen | Demandez à l’utilisateur de suivre automatiquement une conversation lorsqu’il quitte une publication. Peut être vrai ou faux. |

## Étape 3 : Création de l&#39;objet AuthDelegate pour l&#39;intégration de Janrain {#section_asv_vyt_bbb}

Livefyre.require fournit un plugin qui permet à l&#39;auteur d&#39;écouter le bus du Backplane de Janrain.

### Connexion {#login}

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



>[!NOTE]
>
>Votre délégué d’authentification varie en fonction de votre instance Janrain.

Vous trouverez ci-dessous quelques exemples de la manière dont un délégué d’authentification peut rechercher une intégration de capture Janrain.

* `errback`: Rappel transmis à la méthode de connexion du délégué d’authentification
* `janrain`: Référence à votre variable de capture Janrain.
* `window.Backplane`: Référence à l’objet Backplane.

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

* `finishLogout`: Rappel transmis à la méthode de connexion du délégué d’authentification.

* `window.Backplane`: Référence à l’objet Backplane.

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

### Profil de vue {#viewprofile}

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

## Étape 4 : Synchroniser avec Livefyre avec Ping pour Pull pour l’intégration Janrain {#section_ilv_bzt_bbb}

Pour synchroniser les Profils distants de Livefyre avec votre système de gestion des utilisateurs Capture, vous devez suivre une série d&#39;étapes appelées Ping for Pull. Ce processus nécessite que vous obteniez un jeton d&#39;accès valide auprès de Janrain, puis que vous transmettiez ce jeton à un point de terminaison spécifié à l’étape 3 ci-dessous.

1. Obtenez un code d&#39;accès de Janrain.

   Pour obtenir le code d’accès, fournissez les informations d’identification nécessaires, spécifiez user_type comme &quot;user&quot; et uuid comme uuid de l’utilisateur actuel à mettre à jour. Pour plus d’informations, voir [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Échangez le code d&#39;accès d&#39;un jeton d&#39;accès. Fournissez les informations d’identification nécessaires, le code d’accès reçu de l’étape 1 et spécifiez grant_type comme &quot;authorized_code&quot;.

   Pour plus d’informations, voir [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Accédez au point de terminaison Livefyre &quot;Ping to Pull Capture&quot;.

   URL du point de terminaison : [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] où ***{networkName}*** est le nom réseau fourni par Livefyre et le jeton est le jeton reçu de Janrain à l’étape 2.

   Une fois que vous avez atteint ce point de terminaison, vous recevez une réponse 202 et Livefyre commence un processus asynchrone.

## Fonctionnement de tout {#concept_mty_f31_2cb}

Pour bénéficier de cette intégration Capture/Backplane intégrée, vous devez apporter quelques modifications à la configuration de votre application Capture et de votre intégration Livefyre.js.

Janrain envoie des messages de connexion/déconnexion réussis via le bus Backplane, sur lequel l&#39;application Livefyre, lorsqu&#39;elle est correctement configurée, écoute. Ces messages contiennent toutes les informations nécessaires pour montrer aux utilisateurs de l’application qu’ils sont connectés ou déconnectés. Les développeurs peuvent vue les messages du bus du fond de panier en consultant l’onglet Réseau de la console de développement de votre navigateur.

## Exemple de code de connexion {#section_ftt_tvp_mz}

Demande:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Réponse:

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

## Exemple de code de déconnexion {#section_t52_svp_mz}

Demande:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Réponse:

```
Backplane.finishInit("{CHANNEL}");
```

Si ces messages ne s’affichent pas dans vos requêtes réseau, Livefyre ne sera pas au courant des tentatives de connexion/déconnexion et, par conséquent, Livefyre ne pourra pas intégrer l’utilisateur dans l’application.
