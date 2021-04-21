---
description: Utilisez embed.ly pour afficher plusieurs formats multimédias directement dans l’application.
title: Intégration Embedly
exl-id: 859fe306-367e-4207-b9f7-c730ba0cd24d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 10%

---

# Intégration Embedly {#embedly-integration}

Utilisez `embed.ly` pour afficher plusieurs formats multimédias, directement dans l’application.

Pour mieux activer le contenu multimédia incorporé à partir de diverses sources, notamment Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify et Tumblr, les applications Livefyre utilisent Embetly comme fournisseur tiers pour l’extension d’URL. Si un utilisateur ou un modérateur inclut un lien pris en charge dans une publication, le média inclus dans le lien se développera lorsqu’il sera publié dans la collection.

Les applications Livefyre ont ainsi accès à plus de 250 options de médias incorporés différentes prises en charge par Embetly.

>[!NOTE]
>
>Livefyre ne développe qu&#39;un sous-ensemble de la liste complète du fournisseur Embetly. Les images incorporées s’étendent sur les pages HTTPS uniquement si le fournisseur est Twitter, YouTube, Imgur, Vine, Wikipedia ou SoundCloud. Veuillez contacter votre gestionnaire de compte technique pour toute question supplémentaire sur l&#39;extension des liens ou les sources.

Cette page liste des exemples de certains types de supports incorporés courants et leurs modèles d’URL acceptables. `Embed.ly` ajoute continuellement de nouvelles sources. Pour une liste complète des fournisseurs, veuillez aller à `https://embed.ly/embed/features/providers`.

>[!NOTE]
>
>La mise en forme Embetly nécessite un lien permalin complet. Les liens raccourcis ne fonctionneront pas.

Seul le contenu visible publiquement peut être incorporé. Si vous tentez d’incorporer un élément de contenu qui n’est pas public, le lien vers le contenu s’affiche dans la publication de blog et une icône d’espace réservé s’affiche avec cette publication. Lorsque vous cliquez dessus, le lien conduit le lecteur à un message d’erreur du service où le contenu est hébergé, tel qu’un message Facebook pour une photo réservée aux amis. Contactez votre gestionnaire de compte si vous constatez que le média n&#39;est pas développé comme prévu.

## Exemples d’URL d’expression

| Type | Fournisseur | URL |
|--- |--- |--- |
| Mappages | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Remarque** : L’URL doit commencer par  `http` et non par  `https.` |
| Réseaux sociaux | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Vidéo | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Photos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Service de téléchargement de contenu d’Hootsuite) | `https://ow.ly/i/*` |
| Sondages | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Dropler | `https://d.pr/i/*` |
| Audio | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotifier | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Applications qui utilisent cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Carte des fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaïque](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Sondages](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Critiques](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Suivi des tendances](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Bouton Télécharger](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
