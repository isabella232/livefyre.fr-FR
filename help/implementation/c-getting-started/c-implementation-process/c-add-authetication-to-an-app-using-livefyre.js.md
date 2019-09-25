---
description: Utilisez Livefyre.js pour ajouter une authentification à l’échelle de la page pour vos applications Livefyre.
seo-description: Utilisez Livefyre.js pour ajouter une authentification à l’échelle de la page pour vos applications Livefyre.
seo-title: Ajout d’une authentification à une application à l’aide de Livefyre.js
solution: Experience Manager
title: Ajout d’une authentification à une application à l’aide de Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Ajout d’une authentification à une application à l’aide de Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Utilisez Livefyre.js pour ajouter une authentification à l’échelle de la page pour vos applications Livefyre.

`Livefyre.js Aut`Il s’agit d’un package JavaScript développé par Livefyre qui permet à toutes les applications de votre site Web de partager une intégration d’authentification unique. Auth vous permet de définir la manière dont vos utilisateurs doivent s’enregistrer, se connecter et se déconnecter en déléguant ces flux à un objet AuthDelegate que vous définissez.

## Étape 1 : Activer l’authentification pour une page {#section_pgp_jtt_bbb}

Utilisez `Livefyre.js` pour activer l’authentification pour une page afin de permettre aux utilisateurs de se connecter et d’interagir avec les applications à l’aide de votre système d’authentification existant.

1. Pour activer l’authentification sur une page, ajoutez `Livefyre.js` à l’élément *&lt;head&gt;* de votre page Web ou modèle de site Web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Utilisez `Livefyre.require` pour activer l’authentification. Utiliser `Livefyre.require` est similaire à utiliser require pour appeler d'autres packages. Le code d’intégration pour exiger une authentification se présente comme suit :

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Étape 2 : Enregistrement d’un AuthDelegate {#section_oqm_15t_bbb}

Pour activer l’authentification, créez une `AuthDelegate` et transmettez-la à `Livefyre.js` Authentification.

Un `AuthDelegate` objet que vous définissez détermine la manière dont les utilisateurs se connecteront, se déconnecteront et afficheront les profils.

1. Créez une `AuthDelegate`. La façon dont vous construisez un `AuthDelegate` système dépend de votre fournisseur d'identité. Voir Intégration des identités pour obtenir des instructions plus détaillées.

1. Transmettez le `AuthDelegate` à `Livefyre.js` Authentification. Le plus simple `AuthDelegate` consigne le même utilisateur lorsqu’un utilisateur déclenche la méthode de connexion déléguée à partir d’une application :

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

Synchronisez les informations de profil utilisateur entre Livefyre et votre fournisseur d’identité.

Vous devez synchroniser vos informations de profil utilisateur entre Livefyre et votre fournisseur d’identité. Pour plus d’informations, voir Intégration [de capture de](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)Janrain.
