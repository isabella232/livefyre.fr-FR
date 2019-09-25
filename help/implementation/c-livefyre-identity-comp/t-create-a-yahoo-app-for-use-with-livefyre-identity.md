---
description: Vous pouvez utiliser Livefyre Identity avec Yahoo! pour permettre aux utilisateurs d’utiliser leur Yahoo! se connecte pour interagir avec les applications sur votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Yahoo! pour permettre aux utilisateurs d’utiliser leur Yahoo! se connecte pour interagir avec les applications sur votre site.
seo-title: Créez un Yahoo! Application à utiliser avec identité Livefyre
solution: Experience Manager
title: Créez un Yahoo! Application à utiliser avec identité Livefyre
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Créez un Yahoo! Application à utiliser avec identité Livefyre{#create-a-yahoo-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Yahoo! pour permettre aux utilisateurs d’utiliser leur Yahoo! se connecte pour interagir avec les applications sur votre site.

Pour permettre à vos utilisateurs de se connecter à l’aide de leurs informations d’identification Yahoo, Livefyre requiert les informations suivantes sur l’application Yahoo :

* ID client (clé de consommateur)
* Secret client (Secret client)

Pour créer un Yahoo! application à utiliser avec l’identité Livefyre :

1. Accédez à [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)et connectez-vous à Yahoo! pour créer une application ou sélectionner une application existante à utiliser avec l’identité Livefyre.
1. Select **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Sélectionnez **[!UICONTROL API Permissions: Profiles (Social Directory)]** et **[!UICONTROL Read Public]**.

   Une fois l’application terminée, la page des détails de l’application de Yahoo dressera la liste des identifiants client (clé du consommateur) et client secret (clé du client) de l’application à utiliser dans la page des paramètres d’intégration de Studio.

   >[!NOTE]
   >
   >Si vous activez Yahoo! connexion sans créer de Yahoo! et si vous laissez les champs ID client et Secret client dans Studio vides, Livefyre utilisera OpenID pour connecter ces utilisateurs à vos applications Livefyre. OAuth et la marque personnalisée ne seront pas disponibles dans ce cas.