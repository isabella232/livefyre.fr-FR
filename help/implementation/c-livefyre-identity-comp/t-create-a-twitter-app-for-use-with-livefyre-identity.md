---
description: Vous pouvez utiliser l’identité Livefyre avec Twitter pour permettre aux utilisateurs d’utiliser leurs identifiants de connexion Twitter pour interagir avec les applications de votre site.
seo-description: Vous pouvez utiliser l’identité Livefyre avec Twitter pour permettre aux utilisateurs d’utiliser leurs identifiants de connexion Twitter pour interagir avec les applications de votre site.
seo-title: Création d’une application Twitter à utiliser avec l’identité Livefyre
solution: Experience Manager
title: Création d’une application Twitter à utiliser avec l’identité Livefyre
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Créer une application Twitter à utiliser avec l’identité Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Vous pouvez utiliser l’identité Livefyre avec Twitter pour permettre aux utilisateurs d’utiliser leurs identifiants de connexion Twitter pour interagir avec les applications de votre site.

Pour activer la connexion Twitter, Livefyre requiert les informations suivantes sur l&#39;application Twitter :

* consumer key (clé API)
* secret du client (secret API)

Pour créer une application Twitter à utiliser avec l’identité Livefyre :

1. Accédez à [https://apps.twitter.com/](https://apps.twitter.com/) et connectez-vous à votre compte Twitter pour créer une nouvelle application ou sélectionner une application existante à utiliser avec l’identité Livefyre.
1. Dans la page Paramètres de l’application :

   * Saisissez **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (où **{networkName}** correspond au nom réseau fourni par Livefyre. Par exemple :** [!UICONTROL labs]** dans **[!UICONTROL `labs.fyre.co`]**.)
   * Désélectionnez **[!UICONTROL Enable Callback Locking]**.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Dans l&#39;onglet **[!UICONTROL Permissions]**, sélectionnez **[!UICONTROL Access: Read only]**.

Une fois l’opération terminée, la page Gestion des applications de Twitter > Clés et Jetons d&#39;accès liste le Consumer key de l’application (clé d’API) et le Secret du client (clé secrète d’API) à utiliser dans la page Paramètres d’intégration de Studio.
