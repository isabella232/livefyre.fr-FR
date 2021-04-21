---
description: Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d'utiliser leurs connexions Twitter pour interagir avec les applications de votre site.
title: Création d’une application Twitter à utiliser avec l’identité Livefyre
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Création d’une application Twitter à utiliser avec l’identité Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d&#39;utiliser leurs connexions Twitter pour interagir avec les applications de votre site.

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

Une fois l’opération terminée, la page Gestion des applications > Clés et Jetons d&#39;accès de Twitter liste le Consumer key (clé d’API) et le Secret du client (clé secrète d’API) de l’application pour l’utiliser dans la page Paramètres d’intégration de Studio.
