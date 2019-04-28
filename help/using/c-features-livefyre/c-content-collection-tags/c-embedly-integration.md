---
description: Utilisez embed.ly pour afficher plusieurs formats multimédias directement dans l’application.
seo-description: Utilisez embed.ly pour afficher plusieurs formats multimédias directement dans l’application.
seo-title: Intégration Embedly
solution: Experience Manager
title: Intégration Embedly
uuid: 1 f 27 e 32 c-c 2 c 3-4 f 7 c -93 de-c 9 c 7 bf 783 d 6 a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Intégration Embedly{#embedly-integration}

Utilisez `embed.ly` pour afficher plusieurs formats multimédia directement dans l&#39;application.

Afin de mieux activer le contenu multimédia intégré à partir de diverses sources, notamment Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify et Tumblr, les applications Livefyre utilisent l&#39;outil Openrement en tant que fournisseur tiers pour étendre l&#39;URL. Si un utilisateur ou un modérateur comporte un lien pris en charge dans une publication, le support inclus dans le lien s&#39;étend lorsqu&#39;il est publié sur la collection.

Ainsi, les applications Livefyre ont accès aux plus de 250 options multimédias incorporées différentes prises en charge par Incorporer.

>[!NOTE]
>
>Livefyre n&#39;étend qu&#39;un sous-ensemble de la liste complète des fournisseurs d&#39;acquisition. Les images incorporées ne seront développées sur les pages HTTPS que si le fournisseur est Twitter, YouTube, Imgur, Vine, Wikipedia ou soundcloud. Pour toute question sur l&#39;extension des liens ou les sources, contactez votre gestionnaire de compte technique.

Cette page répertorie des exemples de types de supports incorporés courants et leurs schémas d&#39;URL acceptables. `Embed.ly` ajoute continuellement de nouvelles sources. Pour obtenir la liste complète des fournisseurs, rendez `https://embed.ly/embed/features/providers`-vous sur la page.

>[!NOTE]
>
>La mise en forme incorporée requiert un lien permalink complet. Les liens raccourcis ne fonctionneront pas.

Seul le contenu public peut être incorporé. Si vous tentez d&#39;incorporer un élément de contenu non public, le lien vers le contenu s&#39;affiche dans la publication de blog et une icône d&#39;espace réservé l&#39;accompagne. Lorsque vous cliquez dessus, le lien conduit le lecteur à un message d&#39;erreur du service dans lequel le contenu est hébergé, comme un message Facebook pour une photo d&#39;amis uniquement. Veuillez contacter votre gestionnaire de compte si vous constatez que le support n&#39;est pas développé comme prévu.

## Exemples d&#39;URL inclusives

| Type | Fournisseur | URL |
|--- |--- |--- |
| Cartes | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Remarque**: L&#39;URL doit commencer `http` par et non `https.` |
| Réseaux sociaux | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Vidéo | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Photos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | Twitpic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Service de transfert de contenu de Hootsuite) | `https://ow.ly/i/*` |
| Sondages | Gopollgo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | Soundcloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Applications utilisant cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Carte de fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Sondages](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Révisions](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Commentaires de sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Tendances](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Bouton Télécharger](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

