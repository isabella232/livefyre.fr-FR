---
description: Utilisez Ping for Pull pour synchroniser Livefyre avec votre système de gestion des utilisateurs.
seo-description: Utilisez Ping for Pull pour synchroniser Livefyre avec votre système de gestion des utilisateurs.
seo-title: Synchronisation avec Livefyre à l’aide de Ping pour extraction
solution: Experience Manager
title: Synchronisation avec Livefyre à l’aide de Ping pour extraction
uuid: 7b059064-1cca-46d7-8055-dfe59f493ac1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Synchronisation avec Livefyre à l’aide de Ping pour extraction{#sync-with-livefyre-using-ping-for-pull}

Utilisez Ping for Pull pour synchroniser Livefyre avec votre système de gestion des utilisateurs.

En général, vous ***Ping*** Livefyre chaque fois qu’un utilisateur de votre site Web/application met à jour son profil (nom d’affichage, avatar, etc.) et Livefyre ****** récupère le profil mis à jour de cet utilisateur.

![](assets/Ping-for-Pull.png)

Ping pour la séquence d’extraction :

1. Le client envoie la demande Ping à Livefyre (y compris l’utilisateur à mettre à jour).
1. Livefyre confirme la réception de Ping avec HTTP 200/Success.
1. Livefyre traite la demande d’extraction.
1. Livefyre file d’attente Demande d’extraction.
1. Livefyre exécute la requête d’extraction vers le point de fin pour capturer les informations utilisateur mises à jour.
1. Le client reçoit une réponse d’extraction et la valide.
1. Livefyre met à jour les profils distants avec les informations de profil externes incluses dans le point de fin de extraction.

Ping Livefyre chaque fois qu’un utilisateur met à jour ses informations de profil. Bien que le temps d’achèvement de Ping pour Pull puisse varier en fonction de la charge réseau, il met à jour les informations utilisateur d’ici 1 à 10 minutes. Les modifications de profil mises à jour s’afficheront d’abord dans Livefyre Studio &gt; Utilisateurs.

Les informations de profil mises à jour s’affichent dans vos applications Livefyre après deux événements :

* Un utilisateur se déconnecte, puis se reconnecte à l’application. Les valeurs de nom d’affichage dans userAuthToken sont prioritaires sur Ping pour les mises à jour de type extraction. Une déconnexion/connexion utilisateur actualise le jeton pour mettre à jour la session.

   Pour générer de nouveaux userAuthTokens lorsque les informations de profil sont mises à jour, utilisez SSO authDelegate pour déconnecter votre utilisateur puis de nouveau en arrière-plan.

* Une mise à jour de l’amorçage de la collection permet d’apporter les informations mises à jour (au plus toutes les 5 à 10 minutes).

Pour mettre en oeuvre Ping for Pull pour votre système de profil utilisateur :

1. [Créez le point de fin](#t_build_the_pull_endpoint)d’extraction.

   >[!NOTE]
   >
   >La bibliothèque Livefyre comprend une méthode syncUser pour tenir vos profils utilisateur à jour. Ignorez les deux étapes suivantes si vous utilisez la bibliothèque Livefyre.

1. [Enregistrez le point de fin Pull dans Studio](#register_the_endpoint_with_studio).
1. [Construisez le Ping](#t_build_the_ping).
1. [Créez le ping pour une réponse]à tirer.(#reference_n3x_pzb_mz)
