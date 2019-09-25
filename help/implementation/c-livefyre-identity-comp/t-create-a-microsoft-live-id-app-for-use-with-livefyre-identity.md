---
description: Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity pour permettre aux utilisateurs d'utiliser leurs connexions Facebook pour interagir avec les applications de votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity pour permettre aux utilisateurs d'utiliser leurs connexions Facebook pour interagir avec les applications de votre site.
seo-title: Création d'une application d'identité Microsoft Live pour une utilisation avec l'identité Livefyre
solution: Experience Manager
title: Création d'une application d'identité Microsoft Live pour une utilisation avec l'identité Livefyre
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d'une application d'identité Microsoft Live pour une utilisation avec l'identité Livefyre{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity pour permettre aux utilisateurs d'utiliser leurs connexions Facebook pour interagir avec les applications de votre site.

Pour permettre aux utilisateurs de se connecter à l’aide de leurs informations d’identification Microsoft Live Identity, Livefyre requiert les informations d’identité Microsoft Live suivantes :

* ID client (clé privée)
* Secret client (mot de passe)

Pour créer une application Microsoft Live Identity à utiliser avec Livefyre Identity :

1. Créez ou connectez-vous à un compte Microsoft Live à l’adresse [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Créez une application ou sélectionnez-en une pour l’utiliser avec l’identité Livefyre.
1. Cliquez sur **[!UICONTROL Add Platform]**, puis sélectionnez Web comme type de plate-forme.
1. Vérifiez que l’ **[!UICONTROL Allow Implicit Flow]** option est cochée et saisissez l’URL de redirection, en utilisant votre nom réseau au lieu de {network-name} : `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Générez une nouvelle paire mot de passe/clé pour obtenir la clé privée.
1. Dans **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]** le cas présent, basculez la **[!UICONTROL Enable Microsoft Live Login]** bascule sur **[!UICONTROL On]**.
1. Saisissez l’ID client Microsoft Live et la clé secrète client Microsoft Live.
1. Cliquez sur **[!UICONTROL Save Settings]**.

Une fois l’application terminée, la page des détails de l’application de Microsoft Live Identity répertorie l’ID client (clé du consommateur) et la clé secrète client (clé du client) de l’application pour les utiliser dans la page des paramètres d’intégration de Studio.
