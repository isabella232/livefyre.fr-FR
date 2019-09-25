---
description: Vous pouvez utiliser l’identité Livefyre avec LinkedIn pour permettre aux utilisateurs d’utiliser leurs connexions LinkedIn pour interagir avec les applications sur votre site.
seo-description: Vous pouvez utiliser l’identité Livefyre avec LinkedIn pour permettre aux utilisateurs d’utiliser leurs connexions LinkedIn pour interagir avec les applications sur votre site.
seo-title: Création d’une application LinkedIn à utiliser avec l’identité Livefyre
solution: Experience Manager
title: Création d’une application LinkedIn à utiliser avec l’identité Livefyre
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d’une application LinkedIn à utiliser avec l’identité Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Vous pouvez utiliser l’identité Livefyre avec LinkedIn pour permettre aux utilisateurs d’utiliser leurs connexions LinkedIn pour interagir avec les applications sur votre site.

Pour activer la connexion LinkedIn, Livefyre requiert les informations suivantes sur l’application LinkedIn :

* Clé de consommateur (clé API)
* Secret consommateur (secret API)

Pour créer une application LinkedIn à utiliser avec l’identité Livefyre :

1. Accédez à https://www.linkedin.com/secure/developer, puis connectez-vous à votre compte LinkedIn pour créer une application ou sélectionner une application existante à utiliser avec l’identité Livefyre.
1. Cliquez sur **[!UICONTROL Create Application]**.
1. Remplissez le formulaire pour créer l’application.
1. Dans **[!UICONTROL Default Application Permissions]**, activez les autorisations **[!UICONTROL r_basicprofile]** et **[!UICONTROL r_emailaddress]** d’application.
1. Entrez la **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** valeur sous `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Enregistrez l’application.
1. Dans **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]** le cas présent, basculez la **[!UICONTROL Enable LinkedIn Login]** bascule sur **[!UICONTROL On]**.
1. Saisissez l’ID client LinkedIn et la clé secrète client LinkedIn.
1. Cliquez sur **[!UICONTROL Save Settings]**.

Une fois l’application terminée, la page des détails de l’application LinkedIn répertorie la clé d’API de l’application (clé du consommateur) et la clé secrète de l’API (clé du consommateur) à utiliser dans la page des paramètres d’intégration de Studio.
