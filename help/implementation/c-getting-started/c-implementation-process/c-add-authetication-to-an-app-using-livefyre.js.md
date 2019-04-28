---
description: Utilisez Livefyre. js pour ajouter une authentification à l'échelle de la page pour vos applications Livefyre.
seo-description: Utilisez Livefyre. js pour ajouter une authentification à l'échelle de la page pour vos applications Livefyre.
seo-title: Ajout d'une authentification à une application à l'aide de Livefyre. js
solution: Experience Manager
title: Ajout d'une authentification à une application à l'aide de Livefyre. js
uuid: b 7 c 61 e 07-e 341-45 d 7-9112-c 50155 e 38 f 1 d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Ajout d&#39;une authentification à une application à l&#39;aide de Livefyre. js{#add-authetication-to-an-app-using-livefyre-js}

Utilisez Livefyre. js pour ajouter une authentification à l&#39;échelle de la page pour vos applications Livefyre.

`Livefyre.js Aut`h est un paquet JavaScript développé par Livefyre qui permet à toutes les applications de votre site Web de partager une intégration d&#39;authentification unique. Authentique vous permet de définir la manière dont les utilisateurs doivent s&#39;enregistrer, se connecter et se déconnecter en déléguant ces flux à un objet authdelegate que vous définissez.

## Étape 1 : Activation de l&#39;authentification pour une page {#section_pgp_jtt_bbb}

Utilisez `Livefyre.js` cette option pour activer l&#39;authentification d&#39;une page afin de permettre aux utilisateurs de se connecter et d&#39;interagir avec les applications à l&#39;aide de votre système d&#39;authentification existant.

1. Pour activer l&#39;authentification sur une page, ajoutez `Livefyre.js` à l&#39;élément *&lt; head &gt;* de votre page Web ou modèle de site Web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Permet `Livefyre.require` d&#39;activer l&#39;authentification. L&#39;utilisation `Livefyre.require` de cette méthode est semblable à l&#39;utilisation d&#39;un appel pour appeler d&#39;autres packages. Le code d&#39;intégration à exiger un aspect authentique comme :

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Étape 2 : Enregistrement d&#39;un authdelegate {#section_oqm_15t_bbb}

Pour activer l&#39;authentification, créez-la `AuthDelegate` et transmettez-la à `Livefyre.js` Authentification.

Un `AuthDelegate` objet que vous définissez détermine comment les utilisateurs se connectent, se déconnectent et affichent les profils.

1. Créez une `AuthDelegate`. La manière dont vous créez une méthode `AuthDelegate` dépend de votre fournisseur d&#39;identité. Voir Intégration d&#39;identité pour obtenir des instructions plus détaillées.

1. Transmettez l&#39; `AuthDelegate` authentification `Livefyre.js` . La plus simple `AuthDelegate` de figure le même utilisateur lorsqu&#39;un utilisateur a déclenché la méthode de connexion déléguée à partir d&#39;une application :

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Étape 3 : Synchronisation des données utilisateur {#section_u4m_j5t_bbb}

Synchronisez les informations de profil utilisateur entre Livefyre et votre fournisseur d&#39;identité.

Vous devez synchroniser les informations de profil utilisateur entre Livefyre et votre fournisseur d&#39;identité. Pour plus d&#39;informations, voir [Intégration de Janrain Capture](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
