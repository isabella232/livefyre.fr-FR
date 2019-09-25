---
description: Permet aux utilisateurs de personnaliser l’image qui s’affiche avec leur contenu.
seo-description: Permet aux utilisateurs de personnaliser l’image qui s’affiche avec leur contenu.
seo-title: Avatars
title: Avatars
uuid: bf20f3bc-3dcc-4e16-a629-3380d1a7a3f2
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# Avatars{#avatars}

Permet aux utilisateurs de personnaliser l’image qui s’affiche avec leur contenu.

Les avatars utilisateur sont affichés (par défaut) en regard du contenu dans toutes les applications et sont extraits du système de profil d’identité utilisé dans votre implémentation. Ces avatars varient en taille, selon l’application dans laquelle ils sont affichés.

(Livefyre vous permet de désactiver les avatars si vous ne souhaitez pas les afficher dans vos applications.)

>[!NOTE]
>
>Les avatars sont affichés à 25p x 25p pour Chat et à 50p x 50p dans la plupart des autres applications.

## Stockage Avatar {#section_zbh_x1f_wy}

Les avatars sont chargés de manière asynchrone dans Livefyre. Lorsqu’un utilisateur se connecte pour la première fois à l’application ou modifie son fichier d’image d’avatar associé, son image de profil est ajoutée à une file d’attente de tâches. (Un avatar par défaut s’affiche temporairement lorsque l’utilisateur est téléchargé vers l’emplacement de stockage de l’avatar Livefyre.)

## Gravatars {#section_mqh_p1f_wy}

Livefyre soutient l'utilisation des Gravatars. Si un utilisateur n’a pas d’avatar personnalisé dans le cadre de son profil utilisateur, Livefyre recherche un Gravatar pour cet utilisateur. S’il n’existe aucun Gravatar, l’avatar par défaut est utilisé.


Applications qui utilisent cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaïque](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Critiques](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

