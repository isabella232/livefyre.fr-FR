---
description: Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d'utiliser leurs identifiants Twitter pour interagir avec les applications sur votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d'utiliser leurs identifiants Twitter pour interagir avec les applications sur votre site.
seo-title: Création d'une application Twitter pour une utilisation avec Livefyre Identité
solution: Experience Manager
title: Création d'une application Twitter pour une utilisation avec Livefyre Identité
uuid: 841 cce 7 c -618 d -4154-85 a 3-1 de 96 d 04 bb 69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d&#39;une application Twitter pour une utilisation avec Livefyre Identité{#create-a-twitter-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Twitter pour permettre aux utilisateurs d&#39;utiliser leurs identifiants Twitter pour interagir avec les applications sur votre site.

Pour activer la connexion Twitter, Livefyre requiert les informations de l&#39;application Twitter suivantes :

* Clé du consommateur (clé API)
* Secret du consommateur (secret API)

Pour créer une application Twitter à utiliser avec Livefyre Identité :

1. Accédez à [https://apps.twitter.com/](https://apps.twitter.com/), puis connectez-vous à votre compte Twitter pour créer une application existante ou sélectionnez une application existante pour l&#39;utiliser avec Livefyre Identity.
1. Dans la page Paramètres de l&#39;application :

   * Saisissez **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (où **{networkname}** correspond à votre nom de réseau fourni par Livefyre. Par exemple : ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Désélectionnez **[!UICONTROL Enable Callback Locking]**-la.
   * Sélectionnez **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Dans **[!UICONTROL Permissions]** l&#39;onglet, sélectionnez **[!UICONTROL Access: Read only]**.

Une fois l&#39;opération terminée, la page Gestion des applications de Twitter &gt; Clés et jetons d&#39;accès répertorie la clé Consumer Key (clé API) de l&#39;application et la clé secrète Consumer (clé secrète API) pour l&#39;utilisation dans la page Paramètres d&#39;intégration de Studio.
