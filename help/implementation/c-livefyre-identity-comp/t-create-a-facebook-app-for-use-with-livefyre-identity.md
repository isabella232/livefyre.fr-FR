---
description: Vous pouvez utiliser l’identité Livefyre avec Facebook pour permettre aux utilisateurs d’utiliser leurs connexions Facebook pour interagir avec les applications de votre site.
title: Création d’une application Facebook à utiliser avec l’identité Livefyre
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# Création d’une application Facebook à utiliser avec l’identité Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Vous pouvez utiliser l’identité Livefyre avec Facebook pour permettre aux utilisateurs d’utiliser leurs connexions Facebook pour interagir avec les applications de votre site.

Pour permettre à vos utilisateurs de se connecter à l’aide de leurs informations d’identification Facebook, Livefyre requiert les informations suivantes sur l’application Facebook :

* ID application
* Secret de l’application

Pour créer une application Facebook à utiliser avec Livefyre Identity :

1. Accédez à [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Connectez-vous à votre compte de développeur Facebook.
1. Cliquez sur **[!UICONTROL Add New App]** ou sélectionnez une application existante à utiliser avec l’identité Livefyre.
1. Cliquez sur **[!UICONTROL Settings]**, puis sur **[!UICONTROL Basic]**. Entrez une adresse **[!UICONTROL Contact Email]**, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** et **[!UICONTROL Terms of Service URL]**.
1. Cliquez sur le signe plus ( **[!UICONTROL +]**) en regard de **[!UICONTROL Products]**.
1. Cliquez sur **[!UICONTROL Set Up]** sous **[!UICONTROL Facebook Login]**.
1. Cliquez sur **[!UICONTROL Settings]** et configurez les éléments suivants :

   * Définissez **[!UICONTROL Client OAuth Login]** sur **[!UICONTROL Yes]**.
   * Définissez **[!UICONTROL Web OAuth Login]** sur **[!UICONTROL Yes]**.
   * Définissez **[!UICONTROL Use Strict Mode for Redirect URIs]** sur **[!UICONTROL Yes]**.
   * Définissez **[!UICONTROL Enforce HTTPS for Web OAuth Login]** sur **[!UICONTROL Yes]**.
   * Sous **[!UICONTROL Valid OAuth redirect URLs]**, ajoutez l’URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (où `{networkName}` correspond à votre nom de réseau fourni par Livefyre).

1. Sous **[!UICONTROL App Review]** :

   * Rendez l’application publique.
   * Assurez-vous que **[!UICONTROL Approved Items]** pour **[!UICONTROL Login Permissions]** inclut `email`, `public_profile` et `user_friends`.

Une fois l’opération terminée, la page de Tableau de bord du développeur Facebook liste votre ID d’application et votre clé secrète d’application pour une utilisation dans les paramètres d’intégration de Studio.
