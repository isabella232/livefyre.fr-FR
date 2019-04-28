---
description: Notes de mise à jour pour la version du 9 février 2017.
seo-description: Notes de mise à jour pour la version du 9 février 2017.
seo-title: 9 février 2017
title: 9 février 2017
uuid: cbbf 10 f 3-d 8 ca -4 c 10-849 e-fa 7208 f 987 be
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 9 février 2017{#february}

Notes de mise à jour pour la version du 9 février 2017.

## Socialsync pour Twitter {#section_nv4_yry_wy}

Socialsync pour Twitter fait partie de notre fonctionnalité principale pendant plusieurs années. Cependant, à mesure que notre produit a développé et augmenté au fil du temps, socialsync pour Twitter est devenu une fonctionnalité à faible valeur ajoutée actuellement utilisée par une petite partie de notre base de clients. Pour améliorer l&#39;expérience globale de Livefyre pour nos clients et concentrer les ressources de développement dans des domaines de meilleure valeur, nous interrompons la synchronisation de socialsync pour Twitter le 24 février. Socialsync pour Facebook ne sera pas affecté par cette mise à jour. Pour toute question ou toute question concernant cette mise à jour, veuillez contacter votre CSM Livefyre.

## Version de production {#section_r24_1m2_wy}

| Type de publication | Composant | Note de version |
|--- |--- |--- |
| Bogue | Mur multimédia | Correction d&#39;un bogue qui permet aux vidéos Facebook de se lire correctement. |
| Bogue | Modq | Correction d&#39;un bogue qui empêchait l&#39;affichage des rubriques par courriel dans le contenu du flux électronique. |
| Bogue | Mosaic | Ajout de la prise en charge d&#39;accessibilité supplémentaire à Mosaic pour permettre aux utilisateurs de changer de tabulation entre les cartes de contenu. |
| Bogue | Révisions | Correction d&#39;un bogue qui empêchait l&#39;affichage correct des modifications de notation. |
| Bogue | Recherche sociale | Correction d&#39;un bogue en raison duquel le bouton Afficher plus était coupé sur les résultats de la recherche de liste Twitter. |
| Amélioration | Storify 2 | Amélioration de Storify 2 pour prendre en charge la recherche de contenu gratuit. Copyright Free searches across Flickr, Noun Project, Kuler, Pixabay and Unsplash for copyright free image. |
| Bogue | Flux | Correction d&#39;un bogue qui empêchait l&#39;enregistrement des règles de flux Tumblr. |
| Bogue | Flux | Correction d&#39;un bogue qui générait des ID Generator incorrects dans la collection JSON pour les flux RSS. |
| Amélioration | Flux | Ajout d&#39;un ajustement au paramètre de l&#39;option « Comptes vérifiés uniquement » pour être désactivé par défaut. |
| Amélioration | Flux | Ajout d&#39;une nouvelle fonctionnalité permettant d&#39;autoriser des catégories de contenu (par le biais d&#39;une règle de diffusion en continu) et de contourner la modération. |
| Bogue | Flux | Correction d&#39;un bogue en raison duquel les paramètres « Prémodéré » et « Prémodéré multimédia » continuaient à s&#39;appliquer à une règle de flux nouvellement créée. |

## Version UAT {#section_dyx_yl2_wy}

| Type de publication | Composant | Note de version |
|--- |--- |--- |
| Bogue | Applications de conversation | Amélioration des applications de conversation afin de toujours lier les profils utilisateur, même sans une intégration authentique complète. |
| Bogue | Mosaic | Correction d&#39;un bogue qui diffusait désormais toutes les images Twitter via HTTPS. |
| Bogue | Recherche sociale | Correction d&#39;un bogue en raison duquel la coche verte « enregistrée » n&#39;apparaissait pas lors de l&#39;enregistrement des fichiers dans la recherche sociale et l&#39;affichage des fichiers dans la bibliothèque. |
| Bogue | Recherche sociale | Correction d&#39;un bogue qui empêchait le fonctionnement correct de l&#39;option « Masquer les images explicites ». |
| Amélioration | Storify 2 | Amélioration de Storify 2 pour prendre en charge les permalines ouvrant un modale (auparavant, l&#39;application défilait jusqu&#39;à l&#39;emplacement de publication sur la page). Dans Designer de Storify 2, nous avons ajouté une configuration permettant de basculer entre le comportement de permalink Scroll et Modal. Le comportement du permalink modal est le comportement par défaut. |
| Amélioration | Storify 2 | Amélioration de l&#39;intégration Google AMP de Storify 2 pour produire un fichier CSS plus petit. |
| Bogue | Flux | Amélioration du contenu (images et vidéos) des règles de diffusion en continu d&#39;adresses électroniques pour être disponibles via HTTPS. |
| Bogue | Flux | Ajout d&#39;un libellé pour la valeur Rayon du mile dans les zones dans les règles de flux Twitter. |
| Bogue | Flux | Correction d&#39;un bogue concernant les règles de vapeur de page Facebook et Facebook afin d&#39;extraire les publications avec plusieurs pièces jointes multimédias appropriées. |
| Bogue | Studio | Correction d&#39;un bogue en raison duquel plusieurs &amp; s n&#39;étaient pas ajoutés à l&#39;URL lors de l&#39;utilisation des filtres dans Studio. |
| Bogue | Studio | Correction d&#39;un bogue qui empêchait certaines cases à cocher des filtres Studio d&#39;être désactivées. |

