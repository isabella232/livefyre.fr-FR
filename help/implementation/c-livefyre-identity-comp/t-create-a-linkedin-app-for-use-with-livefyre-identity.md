---
description: Vous pouvez utiliser Livefyre Identity avec LinkedIn pour permettre aux utilisateurs d'utiliser leurs connexions LinkedIn pour interagir avec les applications de votre site.
title: Création d’une application LinkedIn à utiliser avec l’identité Livefyre
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Création d’une application LinkedIn à utiliser avec l’identité Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec LinkedIn pour permettre aux utilisateurs d&#39;utiliser leurs connexions LinkedIn pour interagir avec les applications de votre site.

Pour activer la connexion LinkedIn, Livefyre requiert les informations suivantes sur l&#39;application LinkedIn :

* consumer key (clé API)
* secret du client (secret API)

Pour créer une application LinkedIn à utiliser avec l’identité Livefyre :

1. Accédez à https://www.linkedin.com/secure/developer, puis connectez-vous à votre compte LinkedIn pour créer une application ou sélectionner une application existante à utiliser avec Livefyre Identity.
1. Cliquez sur **[!UICONTROL Create Application]**.
1. Remplissez le formulaire pour créer l’application.
1. Dans **[!UICONTROL Default Application Permissions]**, activez les autorisations d&#39;application **[!UICONTROL r_basicprofile]** et **[!UICONTROL r_emailaddress]**.
1. Saisissez **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** comme `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Enregistrez l’application.
1. Dans **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, basculez la bascule **[!UICONTROL Enable LinkedIn Login]** sur **[!UICONTROL On]**.
1. Saisissez l’identifiant du client LinkedIn et la clé secrète du client LinkedIn.
1. Cliquez sur **[!UICONTROL Save Settings]**.

Une fois l’application terminée, la page des détails de l’application de LinkedIn liste la clé d’API (Consumer key) et la clé secrète d’API (Secret du client) de l’application pour l’utiliser dans la page des paramètres d’intégration de Studio.
