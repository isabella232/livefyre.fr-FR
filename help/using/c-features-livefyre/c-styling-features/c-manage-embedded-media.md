---
description: Définissez les sources à partir desquelles les utilisateurs peuvent publier des médias et ceux dont les publications multimédia seront interdites.
seo-description: Définissez les sources à partir desquelles les utilisateurs peuvent publier des médias et ceux dont les publications multimédia seront interdites.
seo-title: Gestion de médias incorporés
title: Gestion de médias incorporés
uuid: d 8621 be 1-dcfb -429 f -954 e-b 21 fdcf 02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Gestion de médias incorporés{#manage-embedded-media}

Définissez les sources à partir desquelles les utilisateurs peuvent publier des médias et ceux dont les publications multimédia seront interdites.

Par défaut, toutes les pièces jointes multimédia peuvent être incorporées dans des commentaires. Pour obtenir la liste complète des fournisseurs pris en charge, voir embed.ly/providers.

Livefyre utilise les protocoles Embed. ly et oembed standard pour incorporer des médias dans les flux d&#39;application et transmettra toutes les données multimédia fournies par la source.

Incorporer. ly transmet toutes les informations disponibles, y compris le titre, la description, la miniature et le code incorporé du support pour toute URL fournie. La disponibilité de ces éléments varie selon le fournisseur. Par exemple : Facebook ne renvoie pas de miniatures pour ses vidéos et transmet uniquement une vidéo incorporable. Cliquer sur Lire lance la vidéo (semblable au format d&#39;affichage de YouTube). Twitter transmet uniquement les images statiques et n&#39;envoie pas de vidéos. Par conséquent, les vidéos natives Twitter peuvent ne pas être lues depuis un flux Livefyre.

Vous pouvez empêcher l&#39;incorporation de certaines pièces jointes dans des commentaires lors de l&#39;incorporation du flux de commentaires. Vous pouvez également choisir de masquer toutes les extensions Incorporer. ly sur le réseau, le site et le niveau de conversation à l&#39;aide de Studio, en affichant uniquement les liens vers le média et non les médias entièrement incorporés.

Applications utilisant cette fonctionnalité :

* [Carte de fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

