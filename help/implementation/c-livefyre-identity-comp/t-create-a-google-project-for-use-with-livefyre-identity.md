---
description: Vous pouvez utiliser Livefyre Identity avec Google pour permettre aux
  utilisateurs d'utiliser leurs connexions Google pour interagir avec les applications
  de votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Google pour permettre
  aux utilisateurs d'utiliser leurs connexions Google pour interagir avec les applications
  de votre site.
seo-title: Création d'un projet Google pour une utilisation avec Livefyre Identité
solution: Experience Manager
title: Création d'un projet Google pour une utilisation avec Livefyre Identité
uuid: b 0 a 6 bb 8 a-abea -4 f 5 c -92 ed -026 e 60183 e 1 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d'un projet Google pour une utilisation avec Livefyre Identité{#create-a-google-project-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Google pour permettre aux utilisateurs d'utiliser leurs connexions Google pour interagir avec les applications de votre site.

Pour permettre à vos utilisateurs de se connecter avec leurs informations d'identification Google, Livefyre requiert les informations de projet Google suivantes :

* ID du client
* Secret client

Pour créer un projet Google pour une utilisation avec Livefyre Identité :

1. Accédez à [https://console.cloud.google.com/project](https://console.cloud.google.com/project) et connectez-vous à votre compte Google pour créer un nouveau ou sélectionner une application existante pour l'utiliser avec Livefyre Identity.
1. Dans le tableau de bord Projet pour l'application, cliquez **[!UICONTROL Enable and Manage APIs]**sur.
1. Dans la page Aperçu de l'API, sous API Social, cliquez sur pour activer l'API Google +.
1. Dans la page Informations d'identification de l'API, sélectionnez **[!UICONTROL Credentials > New credentials > OAuth]** ID client. Dans **[!UICONTROL Create client ID]** la page qui s'ouvre :

   * Sélectionnez Type d'application : Application Web.
   * Saisissez un **[!UICONTROL Name]** pour **[!UICONTROL Client ID]**.
   * Laissez **[!UICONTROL Authorized JavaScript origins]** le champ vide.
   * Saisissez **[!UICONTROL Authorized redirect URIs]**: `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` (où **[!UICONTROL {networkName}]** est votre nom de réseau fourni par Livefyre). Par exemple : ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Cliquez sur **[!UICONTROL Create]** pour enregistrer vos informations d'identification.

Une fois l'opération terminée, la page Gestionnaire d'API de Google > Informations d'identification répertorie l'ID client du projet et la clé secrète client à utiliser dans la page Paramètres d'intégration de Studio.
