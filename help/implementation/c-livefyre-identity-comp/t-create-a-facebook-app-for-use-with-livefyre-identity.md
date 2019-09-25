---
description: Vous pouvez utiliser l’identité Livefyre avec Facebook pour permettre aux utilisateurs d’utiliser leurs connexions Facebook pour interagir avec les applications de votre site.
seo-description: Vous pouvez utiliser l’identité Livefyre avec Facebook pour permettre aux utilisateurs d’utiliser leurs connexions Facebook pour interagir avec les applications de votre site.
seo-title: Création d’une application Facebook à utiliser avec l’identité Livefyre
solution: Experience Manager
title: Création d’une application Facebook à utiliser avec l’identité Livefyre
uuid: a7f7be4e-8986-4e79-831a-0bb0ae55599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d’une application Facebook à utiliser avec l’identité Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Vous pouvez utiliser l’identité Livefyre avec Facebook pour permettre aux utilisateurs d’utiliser leurs connexions Facebook pour interagir avec les applications de votre site.

Pour permettre à vos utilisateurs de se connecter à l’aide de leurs informations d’identification Facebook, Livefyre requiert les informations suivantes sur l’application Facebook :

* ID application
* Secret de l’application

Pour créer une application Facebook à utiliser avec l’identité Livefyre :

1. Accédez à [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Connectez-vous à votre compte de développeur Facebook.
1. Cliquez **[!UICONTROL Add New App]** ou sélectionnez une application existante à utiliser avec l’identité Livefyre.
1. Cliquez sur **[!UICONTROL Settings]**, puis **[!UICONTROL Basic]**. Entrez une **[!UICONTROL Contact Email]** adresse, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** et **[!UICONTROL Terms of Service URL]**.
1. Cliquez sur le signe plus ( **[!UICONTROL +]**) en regard de **[!UICONTROL Products]**.
1. Cliquez sur **[!UICONTROL Set Up]** sous **[!UICONTROL Facebook Login]**.
1. Cliquez sur **[!UICONTROL Settings]** et configurez les éléments suivants :

   * Set **[!UICONTROL Client OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Use Strict Mode for Redirect URIs]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Enforce HTTPS for Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Sous **[!UICONTROL Valid OAuth redirect URLs]**, ajoutez l’URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (où `{networkName}` est votre nom réseau fourni par Livefyre).

1. Under **[!UICONTROL App Review]**:

   * Rendre l’application publique.
   * Assurez-vous que le **[!UICONTROL Approved Items]** pour **[!UICONTROL Login Permissions]** inclut `email`, `public_profile`et `user_friends`.

Une fois l’opération terminée, la page Tableau de bord du développeur Facebook répertorie votre ID d’application et votre secret d’application pour une utilisation dans les paramètres d’intégration de Studio.