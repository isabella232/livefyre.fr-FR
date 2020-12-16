---
description: Utilisez Livefyre.js pour ajouter une authentification à l’échelle de la page pour vos applications Livefyre.
seo-description: Utilisez Livefyre.js pour ajouter une authentification à l’échelle de la page pour vos applications Livefyre.
seo-title: Ajouter l’authentification à une application à l’aide de Livefyre.js
solution: Experience Manager
title: Ajouter l’authentification à une application à l’aide de Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# Ajouter l’authentification à une application à l’aide de Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Utilisez Livefyre.js pour ajouter une authentification à l’échelle de la page pour vos applications Livefyre.

`Livefyre.js Aut`Il s’agit d’un package JavaScript développé par Livefyre qui permet à toutes les applications de votre site Web de partager une intégration d’authentification unique. Auth vous permet de définir comment vos utilisateurs doivent s&#39;enregistrer, se connecter et se déconnecter en déléguant ces flux à un objet AuthDelegate que vous définissez.

## Étape 1 : Activer l&#39;authentification pour une page {#section_pgp_jtt_bbb}

Utilisez `Livefyre.js` pour activer l&#39;authentification pour une page afin de permettre aux utilisateurs de se connecter et d&#39;interagir avec les applications à l&#39;aide de votre système d&#39;authentification existant.

1. Pour activer l’authentification sur une page, ajoutez `Livefyre.js` à l’élément *&lt;head>* de votre page Web ou modèle de site Web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Utilisez `Livefyre.require` pour activer l&#39;authentification. L&#39;utilisation de `Livefyre.require` est similaire à l&#39;utilisation de require pour appeler d&#39;autres packages. Le code d’intégration qui requiert une authentification ressemble à ceci :

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Étape 2 : Enregistrer un AuthDelegate {#section_oqm_15t_bbb}

Pour activer l&#39;authentification, créez une `AuthDelegate` et transmettez-la à `Livefyre.js` authentification.

Un `AuthDelegate` est un objet que vous définissez qui détermine comment les utilisateurs se connectent, se déconnectent et se connectent aux profils de vue.

1. Créez une `AuthDelegate`. La façon dont vous construisez un `AuthDelegate` dépend de votre fournisseur d&#39;identité. Voir Intégration d’identité pour obtenir des instructions plus détaillées.

1. Transmettez l&#39;authentification `AuthDelegate` à `Livefyre.js`. Le plus simple `AuthDelegate` consigne le même utilisateur chaque fois qu’un utilisateur déclenche la méthode de connexion déléguée à partir d’une application :

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Étape 3 : Synchroniser les données utilisateur {#section_u4m_j5t_bbb}

Synchronisez les informations de profil utilisateur entre Livefyre et votre fournisseur d&#39;identité.

Vous devez synchroniser vos informations de profil d’utilisateur entre Livefyre et votre fournisseur d’identité. Pour plus d’informations, voir [Intégration de capture de janvier](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
