---
description: Vous pouvez utiliser Livefyre Identity avec Facebook pour permettre aux
  utilisateurs d'utiliser leurs identifiants Facebook pour interagir avec les applications
  de votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Facebook pour permettre
  aux utilisateurs d'utiliser leurs identifiants Facebook pour interagir avec les
  applications de votre site.
seo-title: Création d'une application Facebook à utiliser avec Livefyre Identité
solution: Experience Manager
title: Création d'une application Facebook à utiliser avec Livefyre Identité
uuid: a 7 f 7 be 4 e -8986-4 e 79-831 a -0 bb 0 ae 555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d'une application Facebook à utiliser avec Livefyre Identité{#create-a-facebook-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Facebook pour permettre aux utilisateurs d'utiliser leurs identifiants Facebook pour interagir avec les applications de votre site.

Pour permettre à vos utilisateurs de se connecter avec leurs informations d'identification Facebook, Livefyre requiert les informations d'application Facebook suivantes :

* ID de l'application
* Secret de l'application

Pour créer une application Facebook à utiliser avec Livefyre Identity :

1. Accédez [à https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Connectez-vous à votre compte développeur Facebook.
1. Cliquez **[!UICONTROL Add New App]** ou sélectionnez une application existante pour l'utiliser avec Livefyre Identity.
1. Cliquez sur **[!UICONTROL Settings]**, puis **[!UICONTROL Basic]**sur. Entrez **[!UICONTROL Contact Email]** une adresse **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]**et **[!UICONTROL Terms of Service URL]**.
1. Cliquez sur le signe plus ( **[!UICONTROL +]**) en regard **[!UICONTROL Products]**de.
1. Cliquez sur **[!UICONTROL Set Up]** sous **[!UICONTROL Facebook Login]**.
1. Cliquez **[!UICONTROL Settings]** sur et configurez les éléments suivants :

   * Défini **[!UICONTROL Client OAuth Login]** sur **[!UICONTROL Yes]**.
   * Défini **[!UICONTROL Web OAuth Login]** sur **[!UICONTROL Yes]**.
   * Défini **[!UICONTROL Use Strict Mode for Redirect URIs]** sur **[!UICONTROL Yes]**.
   * Défini **[!UICONTROL Enforce HTTPS for Web OAuth Login]** sur **[!UICONTROL Yes]**.
   * Sous **[!UICONTROL Valid OAuth redirect URLs]**, ajoutez l'URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (où `{networkName}` correspond votre nom de réseau fourni par Livefyre).

1. Sous **[!UICONTROL App Review]**:

   * Rendre l'application publique.
   * Veillez à **[!UICONTROL Approved Items]****[!UICONTROL Login Permissions]** inclure `email`, `public_profile`et `user_friends`.

Une fois l'opération terminée, la page Tableau de bord du développeur Facebook répertorie votre ID d'application et votre clé secrète de l'application à utiliser dans les paramètres d'intégration de Studio.
