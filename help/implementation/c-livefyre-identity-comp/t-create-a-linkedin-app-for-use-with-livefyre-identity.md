---
description: Vous pouvez utiliser l’identité Livefyre avec LinkedIn pour permettre aux utilisateurs d’utiliser leurs connexions LinkedIn pour interagir avec les applications sur votre site.
seo-description: Vous pouvez utiliser l’identité Livefyre avec LinkedIn pour permettre aux utilisateurs d’utiliser leurs connexions LinkedIn pour interagir avec les applications sur votre site.
seo-title: Création d’une application LinkedIn à utiliser avec l’identité Livefyre
solution: Experience Manager
title: Création d’une application LinkedIn à utiliser avec l’identité Livefyre
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Création d’une application LinkedIn à utiliser avec l’identité Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Vous pouvez utiliser l’identité Livefyre avec LinkedIn pour permettre aux utilisateurs d’utiliser leurs connexions LinkedIn pour interagir avec les applications sur votre site.

Pour activer la connexion LinkedIn, Livefyre requiert les informations suivantes sur l’application LinkedIn :

* consumer key (clé API)
* secret du client (secret API)

Pour créer une application LinkedIn à utiliser avec l’identité Livefyre :

1. Accédez à https://www.linkedin.com/secure/developer, puis connectez-vous à votre compte LinkedIn pour créer une application ou sélectionner une application existante à utiliser avec l’identité Livefyre.
1. Cliquez sur **[!UICONTROL Create Application]**.
1. Remplissez le formulaire pour créer l’application.
1. Dans **[!UICONTROL Default Application Permissions]**, activez les autorisations d&#39;application **[!UICONTROL r_basicprofile]** et **[!UICONTROL r_emailaddress]**.
1. Saisissez **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** comme `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Enregistrez l’application.
1. Dans **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, basculez la bascule **[!UICONTROL Enable LinkedIn Login]** sur **[!UICONTROL On]**.
1. Saisissez l’ID client LinkedIn et la clé secrète client LinkedIn.
1. Cliquez sur **[!UICONTROL Save Settings]**.

Une fois l’application terminée, la page des détails de l’application de LinkedIn liste la clé d’API (Consumer key) et la clé secrète d’API de l’application (Secret du client) pour l’utiliser dans la page des paramètres d’intégration de Studio.
