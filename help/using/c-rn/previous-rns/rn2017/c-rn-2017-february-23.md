---
description: Notes de mise à jour de la version du 23 février 2017.
seo-description: Notes de mise à jour de la version du 23 février 2017.
seo-title: 23 février 2017
title: 23 février 2017
uuid: 9b08acf4-15e9-43b7-8abc-c0d720b156e6
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# February 23, 2017{#february}

Notes de mise à jour de la version du 23 février 2017.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | SDK Android | Réorganisation du SDK Android afin de garantir que les répertoires d’implémentation d’exemple et de référence sont plus clairement identifiables par leur emplacement. |
| Amélioration | SDK Android | SDK Android modifié pour prendre désormais en charge une version minimale du SDK de 14 (moins de 16). |
| bogue | Applications de conversation | Amélioration des applications de conversation pour qu’elles établissent toujours un lien vers les profils utilisateur, même sans intégration complète de l’authentification. |
| bogue | Mosaïque | Correction d’un bogue en raison duquel toutes les images Twitter étaient désormais diffusées via HTTPS. |
| Amélioration | Recherche et flux | Ajout de la capacité de rechercher par les emplacements Instagram (enregistrements) dans les règles de recherche Instagram de bibliothèque et de flux Instagram. |
| bogue | Paramètres | Correction d’un bogue qui empêchait l’enregistrement des comptes sociaux Twitter. |
| bogue | Recherche sociale | Correction d’un bogue qui empêchait le fonctionnement correct de l’option "Cacher les images explicites". |
| Amélioration | Storify 2 | Amélioration de Storify 2 pour la prise en charge des liens permalinks lors de l’ouverture d’un module modal (auparavant, l’application faisait défiler l’écran jusqu’à l’emplacement de publication sur la page). Dans Storify 2’s Designer, nous avons ajouté une configuration permettant de basculer entre le comportement de liaison de permalink de type défilement et Modal. Le comportement du permalink modal sera le comportement par défaut. |
| Amélioration | Storify 2 | Amélioration de l’intégration Storify 2 de Google AMP pour produire un fichier CSS plus petit. |
| Amélioration | Flux | Correction d’un bogue lié aux règles Facebook qui entraînait l’extraction du contenu avec des métadonnées incomplètes. |
| bogue | Flux | Amélioration du contenu (images et vidéos) des règles de diffusion en continu par courrier électronique pour qu’il soit disponible via HTTPS. |
| bogue | Flux | Ajout d’une étiquette pour la valeur du rayon de mille dans les cartes dans les règles de flux Twitter. |
| bogue | Flux | Correction d’un bogue lié aux règles de flux continu de page Facebook et Facebook afin d’extraire correctement les publications avec plusieurs pièces jointes de médias. |
| Amélioration | Flux | Ajout d’une nouvelle fonctionnalité permettant aux utilisateurs de choisir d’appliquer ou de désactiver les règles SAFE par règle de flux. |
| Amélioration | Studio | Correction d’un bogue en raison duquel le contenu n’était pas publié ou enregistré correctement s’il existait déjà. |
| bogue | Studio | Correction d’un bogue en raison duquel plusieurs &amp;’s n’étaient pas ajoutés à l’URL lors de l’utilisation de filtres dans Studio. |
| bogue | Studio | Correction d’un bogue qui empêchait la désactivation de certaines cases à cocher dans les filtres Studio. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Applications | Correction d’un bogue pour afficher le contenu dans les modèles de médias avec les proportions correctes. |
| bogue | Media Wall | Correction d’un bogue qui empêchait le rendu des murs multimédia si des caractères étrangers étaient inclus. |
| bogue | Outils | Correction d’un bogue en raison duquel les pages se chargeaient incorrectement lors de la pagination dans les résultats de recherche avec l’option "Cacher les images explicites" activée. |
| Amélioration | Studio | Augmentation du temps de session avant l'expiration des sessions de connexion de l'utilisateur Studio. Une fois qu'une session Studio expire, l'utilisateur est redirigé pour se reconnecter. |
| bogue | Studio | Correction d’un bogue qui empêchait parfois les utilisateurs d’enregistrer les informations d’identification Instagram. |
| bogue | Studio | Correction d’un bogue qui empêchait l’enregistrement correct de la balise de fonction lorsqu’elle était appliquée. |

