---
description: Vous pouvez utiliser Livefyre Identity avec github Identity pour permettre
  aux utilisateurs d'utiliser leurs identifiants github pour interagir avec les applications
  sur votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec github Identity pour
  permettre aux utilisateurs d'utiliser leurs identifiants github pour interagir avec
  les applications sur votre site.
seo-title: Création d'une application d'identité github pour une utilisation avec
  Livefyre Identité
title: Création d'une application d'identité github pour une utilisation avec Livefyre
  Identité
uuid: cf 56164 c -1521-4 a 42-89 cb -39483764807 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d'une application d'identité github pour une utilisation avec Livefyre Identité{#create-a-github-identity-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec github Identity pour permettre aux utilisateurs d'utiliser leurs identifiants github pour interagir avec les applications sur votre site.

Pour permettre aux utilisateurs de se connecter avec leurs informations d'identification github, Livefyre requiert les informations d'identité github suivantes :

* ID du client (clé privée)
* Secret client (mot de passe)

Pour créer une application d'identité github à utiliser avec Livefyre Identity :

1. Create or sign in to a GitHub account at [](https://github.com/settings/developers).
1. Enregistrez un nouveau ou sélectionnez une application existante pour l'utiliser avec Livefyre Identity.
1. Saisissez toutes les informations sur le formulaire. Entrez le **[!UICONTROL Authorization callback URL]**nom du réseau à la place `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`de.

1. Dans **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, basculez sur **[!UICONTROL Enable GitHub Login]****[!UICONTROL On]**la bascule.

1. Saisissez l'ID client github et la clé secrète client github.
1. Cliquez **[!UICONTROL Save Settings]**sur.

Une fois terminé, la page de détails de l'application github de github répertorie l'ID client de l'application (clé Consumer Key) et la clé secrète client (clé secrète Consumer) à utiliser dans la page Paramètres d'intégration de Studio.
