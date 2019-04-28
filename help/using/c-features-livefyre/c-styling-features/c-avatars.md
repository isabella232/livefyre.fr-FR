---
description: Permet aux utilisateurs de personnaliser l'image qui s'affiche avec leur contenu.
seo-description: Permet aux utilisateurs de personnaliser l'image qui s'affiche avec leur contenu.
seo-title: Avatars
title: Avatars
uuid: bf 20 f 3 bc -3 dcc -4 e 16-a 629-3380 d 1 a 7 a 3 f 2
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Avatars{#avatars}

Permet aux utilisateurs de personnaliser l&#39;image qui s&#39;affiche avec leur contenu.

Les avatars utilisateur sont affichés (par défaut) en regard du contenu dans toutes les applications et extraits du système de profils d&#39;identité utilisé dans votre implémentation. Ces avatars varient selon l&#39;application dans laquelle ils sont affichés.

(Livefyre vous permet de désactiver Avatars si vous ne souhaitez pas les afficher dans vos applications.)

>[!NOTE]
>
>Les avatars s&#39;affichent à 25 p 25 p 25 p pour Chat et 50 p x 50 p dans la plupart des autres applications.

## Stockage d&#39;avatar {#section_zbh_x1f_wy}

Les avatars sont chargés de manière asynchrone dans Livefyre. Lorsqu&#39;un utilisateur se connecte pour la première fois à l&#39;application ou modifie le fichier d&#39;image d&#39;avatar associé, son image de profil est ajoutée à une file d&#39;attente de tâche. (Un avatar par défaut s&#39;affiche temporairement pendant que votre utilisateur est téléchargé vers l&#39;emplacement de stockage de Avefyre Avatar.)

## Gravatars {#section_mqh_p1f_wy}

Livefyre prend en charge l&#39;utilisation de Gravatars. Si un utilisateur ne dispose pas d&#39;un avatar personnalisé dans le cadre de son profil utilisateur, Livefyre recherche un gravatar pour cet utilisateur. S&#39;il n&#39;existe aucune gravatar, l&#39;avatar par défaut est utilisé.

Si les commentaires ont été incorporés à l&#39;aide du module externe Livefyre wordpress, la gravure de l&#39;utilisateur est utilisée si les conditions suivantes sont remplies :

* La gravure a été activée dans le panneau d&#39;administration wordpress et
* l&#39;utilisateur dispose d&#39;un compte Gravatar et
* un avatar personnalisé n&#39;est pas fourni.

Pour plus d&#39;informations, reportez-vous à la documentation wordpress Gravatar.



Applications utilisant cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Carte de fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Révisions](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

