---
description: Définir les sources à partir desquelles les utilisateurs peuvent publier des médias et celles à partir desquelles les publications de médias seront interdites.
seo-description: Définir les sources à partir desquelles les utilisateurs peuvent publier des médias et celles à partir desquelles les publications de médias seront interdites.
seo-title: Gérer les supports incorporés
title: Gérer les supports incorporés
uuid: d8621be1-dcfb-429f-954e-b21fdcf02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Gérer les médias incorporés {#manage-embedded-media}

Définir les sources à partir desquelles les utilisateurs peuvent publier des médias et celles à partir desquelles les publications de médias seront interdites.

Par défaut, toutes les pièces jointes peuvent être incorporées dans des commentaires. Pour obtenir une liste complète des fournisseurs pris en charge, voir embed.ly/providers.

Livefyre utilise les protocoles Embed.ly et oEmbed standard pour incorporer les médias dans les flux d’applications et transmettra toutes les données de médias fournies par sa source.

Embed.ly transmet toutes les informations disponibles, y compris le titre, la description, la miniature et le code incorporé du média pour toute URL fournie. La disponibilité de ces éléments varie selon le fournisseur. Par exemple : Facebook ne renvoie pas de miniatures pour ses vidéos et transmet uniquement une vidéo incorporable. Cliquez sur Lecture pour début la vidéo (semblable au format d’affichage de YouTube). Twitter transmet uniquement des images statiques et n’envoie pas de vidéos. Par conséquent, il est possible que les vidéos natives Twitter ne soient pas lues dans un flux Livefyre.

Vous pouvez empêcher certaines pièces jointes d’être incorporées dans des commentaires lors de l’incorporation du flux de commentaires. Vous pouvez également choisir de masquer toutes les extensions Embed.ly au niveau du réseau, du site et de la conversation à l’aide de Studio, affichant uniquement les liens vers le média, et non les médias entièrement incorporés.

Applications qui utilisent cette fonctionnalité :

* [Carte des fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

