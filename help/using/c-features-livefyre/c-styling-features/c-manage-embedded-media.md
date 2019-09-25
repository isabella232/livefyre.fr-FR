---
description: Définissez les sources à partir desquelles les utilisateurs peuvent publier des médias et celles à partir desquelles les publications de médias seront interdites.
seo-description: Définissez les sources à partir desquelles les utilisateurs peuvent publier des médias et celles à partir desquelles les publications de médias seront interdites.
seo-title: Gestion des médias incorporés
title: Gestion des médias incorporés
uuid: d8621be1-dcfb-429f-954e-b21fdcf02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Gestion des médias incorporés{#manage-embedded-media}

Définissez les sources à partir desquelles les utilisateurs peuvent publier des médias et celles à partir desquelles les publications de médias seront interdites.

Par défaut, toutes les pièces jointes peuvent être incorporées dans des commentaires. Pour obtenir la liste complète des fournisseurs pris en charge, voir embed.ly/providers.

Livefyre utilise Embed.ly et les protocoles oEmbed standard pour incorporer des médias dans les flux d’application et transmettra toutes les données de média fournies par sa source.

Embed.ly transmet toutes les informations disponibles, y compris le titre, la description, la miniature et le code incorporé du média pour toute URL fournie. La disponibilité de ces éléments varie selon le fournisseur. Par exemple : Facebook ne renvoie pas de miniatures pour ses vidéos et transmet uniquement une vidéo intégrable. Cliquez sur Lecture pour lancer la vidéo (comme le format d’affichage de YouTube). Twitter transmet uniquement des images statiques et n’envoie pas de vidéos. Par conséquent, il est possible que les vidéos natives Twitter ne soient pas lues dans un flux Livefyre.

Vous pouvez empêcher l’incorporation de certaines pièces jointes dans des commentaires lors de l’incorporation du flux de commentaires. Vous pouvez également choisir de masquer toutes les extensions Embed.ly au niveau du réseau, du site et de la conversation à l’aide de Studio, affichant uniquement les liens vers le média et non les médias entièrement intégrés.

Applications qui utilisent cette fonctionnalité :

* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

