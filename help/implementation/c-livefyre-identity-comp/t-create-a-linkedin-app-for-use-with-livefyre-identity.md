---
description: Vous pouvez utiliser Livefyre Identity avec linkedin pour permettre aux
  utilisateurs d'utiliser leurs connexions linkedin pour interagir avec les applications
  sur votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec linkedin pour permettre
  aux utilisateurs d'utiliser leurs connexions linkedin pour interagir avec les applications
  sur votre site.
seo-title: Création d'une application linkedin pour une utilisation avec Livefyre
  Identité
solution: Experience Manager
title: Création d'une application linkedin pour une utilisation avec Livefyre Identité
uuid: c 5112 f 24-a 4 e 0-4526-afe 8-b 8 f 27 a 3 b 2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d'une application linkedin pour une utilisation avec Livefyre Identité{#create-a-linkedin-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec linkedin pour permettre aux utilisateurs d'utiliser leurs connexions linkedin pour interagir avec les applications sur votre site.

Pour activer la connexion linkedin, Livefyre requiert les informations d'application linkedin suivantes :

* Clé du consommateur (clé API)
* Secret du consommateur (secret API)

Pour créer une application linkedin à utiliser avec Livefyre Identity :

1. Accédez à https://www.linkedin.com/secure/developer, puis connectez-vous à votre compte linkedin pour créer une nouvelle application ou sélectionnez une application existante pour l'utiliser avec Livefyre Identity.
1. Cliquez **[!UICONTROL Create Application]**sur.
1. Remplissez le formulaire pour créer l'application.
1. Dans le **[!UICONTROL Default Application Permissions]**, activez les autorisations **[!UICONTROL r_basicprofile]** et **[!UICONTROL r_emailaddress]** l'application.
1. Entrez le **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** sous `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`-formulaire.
1. Enregistrez l'application.
1. Dans **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, basculez sur **[!UICONTROL Enable LinkedIn Login]****[!UICONTROL On]**la bascule.
1. Saisissez l'identifiant client linkedin et la clé secrète client linkedin.
1. Cliquez **[!UICONTROL Save Settings]**sur.

Une fois l'opération terminée, la page Détails de l'application linkedin répertorie la clé API de l'application (clé du consommateur) et la clé secrète API (clé secrète Consumer) à utiliser dans la page Paramètres d'intégration de Studio.
