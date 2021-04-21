---
description: Vous pouvez utiliser Livefyre Identity avec Yahoo! pour permettre aux utilisateurs d’utiliser leur Yahoo! se connecte pour interagir avec les applications sur votre site.
title: Créez un Yahoo! Application à utiliser avec l’identité Livefyre
exl-id: 6b4c6ea9-1cb0-4496-aabe-70811f464a3d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Créez un Yahoo! Application à utiliser avec l’identité Livefyre{#create-a-yahoo-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Yahoo! pour permettre aux utilisateurs d’utiliser leur Yahoo! se connecte pour interagir avec les applications sur votre site.

Pour permettre à vos utilisateurs de se connecter à l’aide de leurs identifiants Yahoo, Livefyre requiert les informations suivantes sur l’application Yahoo :

* ID de client (Consumer key)
* Secret client (Secret du client)

Pour créer un Yahoo! application à utiliser avec l’identité Livefyre :

1. Accédez à [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) et connectez-vous à votre Yahoo! pour créer une nouvelle application ou sélectionner une application existante à utiliser avec l’identité Livefyre.
1. Select **[!UICONTROL Application Type: Web Application]**.
1. Entrée **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Sélectionnez **[!UICONTROL API Permissions: Profiles (Social Directory)]** et **[!UICONTROL Read Public]**.

   Une fois l’application terminée, la page des détails de l’application de Yahoo liste l’identifiant client (Consumer key) et la clé secrète client (Secret du client) de l’application pour l’utiliser dans la page des paramètres d’intégration de Studio.

   >[!NOTE]
   >
   >Si vous activez Yahoo! connexion sans créer de Yahoo! et si vous laissez les champs ID client et Clé secrète client dans Studio vides, Livefyre utilisera OpenID pour connecter ces utilisateurs à vos applications Livefyre. Dans ce cas, OAuth et l’identité graphique personnalisée ne seront pas disponibles.
