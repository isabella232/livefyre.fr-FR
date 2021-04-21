---
description: Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity pour permettre aux utilisateurs d'utiliser leurs connexions Facebook pour interagir avec les applications de votre site.
title: Création d’une application d’identité Microsoft Live pour une utilisation avec l’identité Livefyre
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Création d’une application d’identité Microsoft Live pour une utilisation avec l’identité Livefyre{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity pour permettre aux utilisateurs d&#39;utiliser leurs connexions Facebook pour interagir avec les applications de votre site.

Pour permettre aux utilisateurs de se connecter à l’aide de leurs identifiants Microsoft Live Identity, Livefyre requiert les informations d’identité Microsoft Live suivantes :

* ID client (clé privée)
* Secret client (mot de passe)

Pour créer une application Microsoft Live Identity à utiliser avec Livefyre Identity :

1. Créez ou connectez-vous à un compte Microsoft Live à l’adresse [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/).
1. Créez une application ou sélectionnez-en une pour l’utiliser avec l’identité Livefyre.
1. Cliquez sur **[!UICONTROL Add Platform]**, puis sélectionnez Web comme type de plate-forme.
1. Assurez-vous que l&#39;option **[!UICONTROL Allow Implicit Flow]** est cochée et saisissez l&#39;URL de redirection en utilisant votre nom de réseau au lieu de {network-name} : `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Générez une nouvelle paire mot de passe/clé pour obtenir la clé privée.
1. Dans **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, basculez la bascule **[!UICONTROL Enable Microsoft Live Login]** sur **[!UICONTROL On]**.
1. Saisissez l’ID client Microsoft Live et la clé secrète client Microsoft Live.
1. Cliquez sur **[!UICONTROL Save Settings]**.

Une fois l’application terminée, la page des détails de l’application de Microsoft Live Identity liste l’identifiant client (Consumer key) et la clé secrète client (Secret du client) de l’application pour l’utiliser dans la page des paramètres d’intégration de Studio.
