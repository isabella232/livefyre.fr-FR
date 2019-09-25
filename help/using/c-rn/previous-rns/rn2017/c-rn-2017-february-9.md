---
description: Notes de mise à jour de la version du 9 février 2017.
seo-description: Notes de mise à jour de la version du 9 février 2017.
seo-title: 9 février 2017
title: 9 février 2017
uuid: cbbf10f3-d8ca-4c10-849e-fa7208f987be
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# February 9, 2017{#february}

Notes de mise à jour de la version du 9 février 2017.

## SocialSync pour Twitter {#section_nv4_yry_wy}

SocialSync pour Twitter fait partie de notre fonctionnalité principale depuis plusieurs années. Cependant, à mesure que notre produit s’est développé et s’est développé au fil du temps, SocialSync pour Twitter est devenu une fonctionnalité de moindre valeur actuellement utilisée par une très petite partie de notre base de clients. Afin d’améliorer l’expérience globale de Livefyre pour nos clients et de concentrer les ressources de développement dans les domaines les plus rentables, nous mettrons fin à la fonctionnalité SocialSync pour Twitter le 24 février. SocialSync pour Facebook ne sera pas affecté par cette mise à jour. Si vous avez des questions ou des préoccupations au sujet de cette mise à jour, contactez votre CSM Livefyre.

## Version de production {#section_r24_1m2_wy}

| Type de problème | Composant | Note de mise à jour |
|--- |--- |--- |
| bogue | Media Wall | Correction d’un bogue en raison duquel les vidéos Facebook pouvaient être lues correctement. |
| bogue | ModQ | Correction d’un bogue qui empêchait l’affichage des objets de courrier électronique dans le contenu du flux de courrier électronique. |
| bogue | Mosaïque | Ajout de la prise en charge de l’accessibilité à Mosaic pour permettre aux utilisateurs de changer d’onglet entre les cartes de contenu. |
| bogue | Critiques | Correction d’un bogue qui empêchait l’affichage approprié des modifications d’évaluation. |
| bogue | Recherche sociale | Correction d’un bogue en raison duquel le bouton Afficher plus était coupé dans les résultats de la recherche par liste Twitter. |
| Amélioration | Storify 2 | Amélioration de Storify 2 pour la prise en charge de la recherche de contenu Gratuit en copie. Copywrite Free recherche des images gratuites sur Flickr, Noun Project, Kuler, Pixabay et Unsplash. |
| bogue | Flux | Correction d’un bogue qui empêchait l’enregistrement des règles de flux Tumblr. |
| bogue | Flux | Correction d’un bogue qui générait des identifiants de générateur incorrects dans la collection JSON pour les flux RSS. |
| Amélioration | Flux | Ajustement du paramètre de l’option "Comptes vérifiés uniquement" pour être désactivé par défaut. |
| Amélioration | Flux | Ajout d’une nouvelle fonctionnalité permettant d’autoriser la liste blanche des catégories de contenu (par le biais d’une règle de diffusion en continu) et de contourner la modération. |
| bogue | Flux | Correction d’un bogue en raison duquel les paramètres "Prémodéré" et "Prémodéré média" étaient transférés vers une règle de diffusion en continu nouvellement créée. |

## Version UAT {#section_dyx_yl2_wy}

| Type de problème | Composant | Note de mise à jour |
|--- |--- |--- |
| bogue | Applications de conversation | Amélioration des applications de conversation pour qu’elles établissent toujours un lien vers les profils utilisateur, même sans intégration complète de l’authentification. |
| bogue | Mosaïque | Correction d’un bogue en raison duquel toutes les images Twitter étaient désormais diffusées via HTTPS. |
| bogue | Recherche sociale | Correction d’un bogue en raison duquel la coche verte "enregistrée" n’apparaissait pas lors de l’enregistrement de fichiers dans Recherche sociale et de l’affichage de fichiers dans la bibliothèque. |
| bogue | Recherche sociale | Correction d’un bogue qui empêchait le fonctionnement correct de l’option "Cacher les images explicites". |
| Amélioration | Storify 2 | Amélioration de Storify 2 pour la prise en charge des liens permalinks lors de l’ouverture d’un module modal (auparavant, l’application faisait défiler l’écran jusqu’à l’emplacement de publication sur la page). Dans Storify 2, nous avons ajouté une configuration pour basculer entre le comportement de liaison de permalink de défilement et modale. Le comportement du permalink modal sera le comportement par défaut. |
| Amélioration | Storify 2 | Amélioration de l’intégration Storify 2 de Google AMP pour produire un fichier CSS plus petit. |
| bogue | Flux | Amélioration du contenu (images et vidéos) des règles de diffusion en continu par courrier électronique pour qu’il soit disponible via HTTPS. |
| bogue | Flux | Ajout d’une étiquette pour la valeur du rayon de mille dans les cartes dans les règles de flux Twitter. |
| bogue | Flux | Correction d’un bogue lié aux règles de flux continu de page Facebook et Facebook afin d’extraire correctement les publications avec plusieurs pièces jointes de médias. |
| bogue | Studio | Correction d’un bogue en raison duquel plusieurs &amp;’s n’étaient pas ajoutés à l’URL lors de l’utilisation de filtres dans Studio. |
| bogue | Studio | Correction d’un bogue qui empêchait la désactivation de certaines cases à cocher dans les filtres Studio. |

