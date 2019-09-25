---
description: Vous pouvez utiliser l’identité Livefyre avec l’identité GitHub pour permettre aux utilisateurs d’utiliser leurs connexions GitHub pour interagir avec les applications sur votre site.
seo-description: Vous pouvez utiliser l’identité Livefyre avec l’identité GitHub pour permettre aux utilisateurs d’utiliser leurs connexions GitHub pour interagir avec les applications sur votre site.
seo-title: Création d’une application d’identité GitHub à utiliser avec l’identité Livefyre
title: Création d’une application d’identité GitHub à utiliser avec l’identité Livefyre
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d’une application d’identité GitHub à utiliser avec l’identité Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

Vous pouvez utiliser l’identité Livefyre avec l’identité GitHub pour permettre aux utilisateurs d’utiliser leurs connexions GitHub pour interagir avec les applications sur votre site.

Pour permettre aux utilisateurs de se connecter avec leurs identifiants GitHub, Livefyre requiert les informations d’identité GitHub suivantes :

* ID client (clé privée)
* Secret client (mot de passe)

Pour créer une application d’identité GitHub à utiliser avec l’identité Livefyre :

1. Créez ou connectez-vous à un compte GitHub à [](https://github.com/settings/developers).
1. Enregistrez une nouvelle application ou sélectionnez une application existante à utiliser avec l’identité Livefyre.
1. Entrez toutes les informations du formulaire. Entrez le **[!UICONTROL Authorization callback URL]**, en utilisant votre nom de réseau au lieu de `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. Dans **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]** le cas présent, basculez la **[!UICONTROL Enable GitHub Login]** bascule sur **[!UICONTROL On]**.

1. Entrez l'ID client GitHub et la clé secrète client GitHub.
1. Cliquez sur **[!UICONTROL Save Settings]**.

Une fois l’application terminée, la page des détails de l’application d’identité GitHub répertorie l’ID client (clé du client) et la clé secrète client (clé du client) de l’application pour une utilisation dans la page des paramètres d’intégration de Studio.
