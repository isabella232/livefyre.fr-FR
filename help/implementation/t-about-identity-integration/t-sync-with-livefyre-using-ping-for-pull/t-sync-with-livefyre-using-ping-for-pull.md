---
description: Utilisez Ping pour Pull pour conserver Livefyre en synchronisation avec votre système de gestion des utilisateurs.
seo-description: Utilisez Ping pour Pull pour conserver Livefyre en synchronisation avec votre système de gestion des utilisateurs.
seo-title: Synchronisation avec Livefyre avec Ping pour pull
solution: Experience Manager
title: Synchronisation avec Livefyre avec Ping pour pull
uuid: 7 b 059064-1 cca -46 d 7-8055-dfe 59 f 493 ac 1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Synchronisation avec Livefyre avec Ping pour pull{#sync-with-livefyre-using-ping-for-pull}

Utilisez Ping pour Pull pour conserver Livefyre en synchronisation avec votre système de gestion des utilisateurs.

En général, ***vous pouvez faire ping*** Livefyre chaque fois qu&#39;un utilisateur de votre site Web/application met à jour son profil (nom d&#39;affichage, avatar, etc.) et que Livefyre ***récupère*** le profil mis à jour de cet utilisateur.

![](assets/Ping-for-Pull.png)

Ping pour séquence pull :

1. Le client envoie la demande Ping à Livefyre (y compris l&#39;utilisateur à mettre à jour).
1. Livefyre confirme réception de Ping avec HTTP 200/Success.
1. Livefyre traite la demande Pull.
1. Livefyre files files d&#39;attente.
1. Livefyre exécute la demande d&#39;extraction au endpoint de fin pour capturer les informations utilisateur mises à jour.
1. Le client reçoit une réponse Extraire et valide.
1. Livefyre met à jour les profils distants avec les informations de profil externes incluses dans le endpoint de fin Pull.

Ping Livefyre lorsqu&#39;un utilisateur met à jour ses informations de profil. Tandis que l&#39;heure de fin de l&#39;extraction peut varier selon le chargement du réseau, elle met à jour les informations de l&#39;utilisateur dans - entre 1 et 10 minutes. Les modifications de profil mises à jour s&#39;affichent en premier dans Livefyre Studio &gt; Users.

Les informations de profil mises à jour apparaîtront dans vos applications Livefyre après deux événements :

* Un utilisateur se déconnecte puis revient dans l&#39;application. Les valeurs de nom d&#39;affichage dans userauthtoken sont prioritaires sur Ping pour les mises à jour Pull. Une déconnexion/connexion utilisateur actualise le jeton pour mettre à jour la session.

   Pour générer de nouveaux identifiants userauthtokens lorsque les informations de profil sont mises à jour, utilisez l&#39;authentification unique SSO authdelegate pour déconnecter votre utilisateur puis en arrière-plan.

* Une mise à jour de démarrage vers la collection apporte les informations mises à jour (toutes les 5-10 minutes au maximum).

Pour implémenter Ping pour Pull pour votre système de profil utilisateur :

1. [Générez le endpoint de fin Pull](#t_build_the_pull_endpoint).

   >[!NOTE]
   >
   >La bibliothèque Livefyre comprend une méthode syncuser pour garder les profils utilisateur vers le haut - date. Ignorez les deux étapes suivantes si vous utilisez la bibliothèque Livefyre.

1. [Enregistrez le endpoint de fin Pull dans Studio](#register_the_endpoint_with_studio).
1. [Créez le ping](#t_build_the_ping).
1. [Créez le ping pour Réponse pull].(# reference_ n 3 x_ pzb_ mz)
