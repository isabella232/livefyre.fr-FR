---
description: Notes de mise à jour pour la version du 23 février 2017.
seo-description: Notes de mise à jour pour la version du 23 février 2017.
seo-title: 23 février 2017
title: 23 février 2017
uuid: 9 b 08 acf 4-15 e 9-43 b 7-8 abc-c 0 d 720 b 156 e 6
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 23 février 2017{#february}

Notes de mise à jour pour la version du 23 février 2017.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Amélioration | SDK Android | Réorganisation du SDK Android pour vérifier que les répertoires d'implémentation de référence et de référence sont plus clairement identifiables par leur emplacement. |
| Amélioration | SDK Android | Android SDK modified to now support a minimum SDK version of 14 (down from 16). |
| Bogue | Applications de conversation | Amélioration des applications de conversation afin de toujours lier les profils utilisateur, même sans une intégration authentique complète. |
| Bogue | Mosaic | Correction d'un bogue qui diffusait désormais toutes les images Twitter via HTTPS. |
| Amélioration | Recherche et flux | Ajout de la capacité d'effectuer une recherche par Places Instagram (archivage) dans la bibliothèque Instagram et les règles de flux Instagram. |
| Bogue | Paramètres | Correction d'un bogue qui empêchait l'enregistrement des comptes Twitter de Twitter. |
| Bogue | Recherche sociale | Correction d'un bogue qui empêchait le fonctionnement correct de l'option « Masquer les images explicites ». |
| Amélioration | Storify 2 | Amélioration de Storify 2 pour prendre en charge les permalines ouvrant un modale (auparavant, l'application défilait jusqu'à l'emplacement de publication sur la page). Dans Designer de Storify 2, nous avons ajouté une configuration permettant de basculer entre le comportement de permalink Scroll et Modal. Le comportement du permalink modal est le comportement par défaut. |
| Amélioration | Storify 2 | Amélioration de l'intégration Google AMP de Storify 2 pour produire un fichier CSS plus petit. |
| Amélioration | Flux | Correction d'un bogue concernant les règles Facebook qui entraînaient l'extraction de contenu avec des métadonnées incomplètes. |
| Bogue | Flux | Amélioration du contenu (images et vidéos) des règles de diffusion en continu d'adresses électroniques pour être disponibles via HTTPS. |
| Bogue | Flux | Ajout d'un libellé pour la valeur Rayon du mile dans les zones dans les règles de flux Twitter. |
| Bogue | Flux | Correction d'un bogue concernant les règles de vapeur de page Facebook et Facebook afin d'extraire les publications avec plusieurs pièces jointes multimédias appropriées. |
| Amélioration | Flux | Ajout d'une nouvelle fonctionnalité permettant aux utilisateurs de choisir d'appliquer ou de désactiver des règles SAFE par règle de diffusion en continu. |
| Amélioration | Studio | Correction d'un bogue qui entraînait la publication ou l'enregistrement incorrect du contenu s'il existait déjà. |
| Bogue | Studio | Correction d'un bogue en raison duquel plusieurs & s n'étaient pas ajoutés à l'URL lors de l'utilisation des filtres dans Studio. |
| Bogue | Studio | Correction d'un bogue qui empêchait certaines cases à cocher des filtres Studio d'être désactivées. |

## Version UAT

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Applications | Correction d'un bogue qui affichait le contenu des modals médias avec les proportions appropriées. |
| Bogue | Mur multimédia | Correction d'un bogue en raison duquel les murs de médias n'étaient pas rendus si des caractères étrangers spécifiques étaient inclus. |
| Bogue | Rechercher | Correction d'un bogue en raison duquel les pages se chargeaient incorrectement lors de la pagination dans les résultats de recherche avec l'activation de « Masquer les images explicites ». |
| Amélioration | Studio | Augmentation du délai de session avant expiration des sessions de connexion au studio Studio. Une fois qu'une session Studio expire, l'utilisateur est redirigé pour se reconnecter. |
| Bogue | Studio | Correction d'un bogue qui empêchait parfois les utilisateurs d'enregistrer les informations d'identification Instagram. |
| Bogue | Studio | Correction d'un bogue qui empêchait l'enregistrement correct de la « balise de fonctionnalité » lorsqu'elle était appliquée. |

