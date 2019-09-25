---
description: Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d’utiliser leurs identifiants de connexion Twitter pour interagir avec les applications sur votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d’utiliser leurs identifiants de connexion Twitter pour interagir avec les applications sur votre site.
seo-title: Création d’une application Twitter à utiliser avec l’identité Livefyre
solution: Experience Manager
title: Création d’une application Twitter à utiliser avec l’identité Livefyre
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d’une application Twitter à utiliser avec l’identité Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d’utiliser leurs identifiants de connexion Twitter pour interagir avec les applications sur votre site.

Pour activer la connexion Twitter, Livefyre requiert les informations suivantes sur l’application Twitter :

* Clé de consommateur (clé API)
* Secret consommateur (secret API)

Pour créer une application Twitter à utiliser avec l’identité Livefyre :

1. Accédez à [https://apps.twitter.com/](https://apps.twitter.com/), puis connectez-vous à votre compte Twitter pour créer une application ou sélectionner une application existante à utiliser avec l’identité Livefyre.
1. Dans la page Paramètres de l’application :

   * Entrez **[!UICONTROL Callback URL:]** (où `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` {networkName} **** est le nom réseau fourni par Livefyre). For example:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Désélectionnez **[!UICONTROL Enable Callback Locking]**.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Dans l’ **[!UICONTROL Permissions]** onglet, sélectionnez **[!UICONTROL Access: Read only]**.

Une fois l’application terminée, la page Gestion des applications &gt; Clés et jetons d’accès de Twitter répertorie la clé de consommateur (clé d’API) et la clé de consommateur (clé secrète d’API) de l’application pour les utiliser dans la page des paramètres d’intégration de Studio.
