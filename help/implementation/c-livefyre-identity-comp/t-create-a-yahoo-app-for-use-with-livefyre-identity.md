---
description: Vous pouvez utiliser Livefyre Identity avec Yahoo ! pour permettre aux utilisateurs d'utiliser leur connexion pour interagir avec les applications sur votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Yahoo ! pour permettre aux utilisateurs d'utiliser leur connexion pour interagir avec les applications sur votre site.
seo-title: Création d'un Application à utiliser avec Livefyre Identité
solution: Experience Manager
title: Création d'un Application à utiliser avec Livefyre Identité
uuid: 6863 cd 2 e-eb 0 d -465 b-b 706-88 ecaccf 41 bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d&#39;un Application à utiliser avec Livefyre Identité{#create-a-yahoo-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Yahoo ! pour permettre aux utilisateurs d&#39;utiliser leur connexion pour interagir avec les applications sur votre site.

Pour permettre à vos utilisateurs de se connecter avec leurs informations d&#39;identification Yahoo, Livefyre requiert les informations suivantes de Yahoo App :

* ID du client (clé du consommateur)
* Secret client (secret du consommateur)

Pour créer une application à utiliser avec Livefyre Identity :

1. Accédez à [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)et connectez-vous à Yahoo ! pour créer un nouveau ou sélectionner une application existante pour l&#39;utiliser avec Livefyre Identity.
1. Sélectionnez **[!UICONTROL Application Type: Web Application]**.
1. Entrer **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. Sélectionnez **[!UICONTROL API Permissions: Profiles (Social Directory)]** et **[!UICONTROL Read Public]**.

   Une fois l&#39;opération terminée, la page Détails de l&#39;application Yahoo répertorie l&#39;ID client de l&#39;application (clé du consommateur) et la clé secrète client (clé secrète du consommateur) à utiliser dans la page Paramètres d&#39;intégration de Studio.

   >[!NOTE]
   >
   >Si vous activez Yahoo ! connexion sans créer de Yahoo ! et si vous laissez les champs ID client et Secret client dans Studio vide, Livefyre utilise openid pour enregistrer ces utilisateurs dans vos applications Livefyre. Oauth et la marque personnalisée ne seront pas disponibles dans ce cas.