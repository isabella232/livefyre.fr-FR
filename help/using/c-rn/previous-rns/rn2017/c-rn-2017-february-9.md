---
description: Notes de mise à jour de la version du 9 février 2017.
title: 9 février 2017
exl-id: 155f8a43-17e5-40b2-ada0-32691f8a34e5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 5%

---

# 9 février 2017{#february}

Notes de mise à jour de la version du 9 février 2017.

## SocialSync pour Twitter {#section_nv4_yry_wy}

SocialSync pour Twitter fait partie de nos fonctionnalités de base depuis plusieurs années. Cependant, à mesure que notre produit s’est développé et s’est développé au fil du temps, SocialSync pour Twitter est devenu une fonctionnalité de moindre valeur qui est actuellement utilisée par une très petite partie de notre clientèle. Afin d’améliorer l’expérience globale de Livefyre pour nos clients et de concentrer les ressources de développement dans les domaines les plus rentables, nous supprimerons la fonctionnalité SocialSync pour Twitter le 24 février. SocialSync pour Facebook ne sera pas affecté par cette mise à jour. Si vous avez des questions ou des inquiétudes au sujet de cette mise à jour, contactez votre responsable Livefyre.

## Version de production {#section_r24_1m2_wy}

| Type de problème | Composant | Note de mise à jour |
|--- |--- |--- |
| bogue | Mur multimédia | Correction d’un bogue en raison duquel les vidéos Facebook pouvaient être lues correctement. |
| bogue | ModQ | Correction d’un bogue qui empêchait l’affichage des objets de courrier électronique dans le contenu du flux de courrier électronique. |
| bogue | Mosaïque | Ajout de la prise en charge de l’accessibilité à Mosaic pour permettre aux utilisateurs de changer de tabulation entre les cartes de contenu. |
| bogue | Critiques | Correction d’un bogue en raison duquel les modifications d’évaluation n’apparaissaient pas correctement. |
| bogue | Recherche sociale | Correction d’un bogue en raison duquel le bouton Afficher plus était coupé dans les résultats de la recherche de Liste Twitter. |
| Amélioration | Storify 2 | Amélioration de Storify 2 pour la prise en charge de la recherche de contenu Gratuit en copie. Copywrite Free recherche des images gratuites sur Flickr, Noun Project, Kuler, Pixabay et Unsplash. |
| bogue | Flux | Correction d’un bogue qui empêchait l’enregistrement des règles de flux Tumblr. |
| bogue | Flux | Correction d’un bogue en raison duquel des ID de générateur incorrects étaient générés dans la collection JSON pour les flux RSS. |
| Amélioration | Flux | Correction de la définition de l’option &quot;Comptes vérifiés uniquement&quot; à désactiver par défaut. |
| Amélioration | Flux | Ajouté une nouvelle fonctionnalité permettant de placer sur la liste autorisée les catégories de contenu (par le biais d’une règle de diffusion en continu) et de contourner la modération. |
| bogue | Flux | Correction d’un bogue en raison duquel les paramètres &quot;Prémodéré&quot; et &quot;Prémodéré média&quot; étaient reportés à une nouvelle règle de diffusion en continu. |

## Version UAT {#section_dyx_yl2_wy}

| Type de problème | Composant | Note de mise à jour |
|--- |--- |--- |
| bogue | Applications de conversation | Amélioration des applications de conversation pour qu’elles se connectent toujours aux profils utilisateur, même sans intégration complète de l’authentification. |
| bogue | Mosaïque | Correction d’un bogue en raison duquel toutes les images Twitter étaient désormais accessibles via HTTPS. |
| bogue | Recherche sociale | Correction d’un bogue en raison duquel la coche verte &quot;enregistrée&quot; n’apparaissait pas lors de l’enregistrement de fichiers dans Recherche sociale et de l’affichage de fichiers dans la bibliothèque. |
| bogue | Recherche sociale | Correction d’un bogue en raison duquel l’option &quot;Masquer les images explicites&quot; ne fonctionnait pas correctement. |
| Amélioration | Storify 2 | Amélioration de la fonctionnalité Storify 2 pour la prise en charge des liens permules l’ouverture d’un module modal (auparavant, l’application faisait défiler l’écran jusqu’à l’emplacement de publication sur la page). Dans Storify 2’s Designer, nous avons ajouté une configuration permettant de basculer entre le comportement de liaison de permalink Modal et Scroll. Le comportement par défaut sera celui du lien permalink modal. |
| Amélioration | Storify 2 | Amélioration de l’intégration Storify 2 de Google AMP pour produire un fichier CSS plus petit. |
| bogue | Flux | Amélioration du contenu (images et vidéos) des règles de diffusion en continu des courriels pour qu’il soit disponible via HTTPS. |
| bogue | Flux | Ajouté une étiquette pour la valeur du rayon de mille dans les cartes dans les règles de flux Twitter. |
| bogue | Flux | Correction d’un bogue lié aux règles de gestion dynamique des pages Facebook et Facebook afin d’extraire correctement les publications avec plusieurs pièces jointes. |
| bogue | Studio | Correction d’un bogue en raison duquel plusieurs &amp;’s n’étaient pas ajoutés à l’URL lors de l’utilisation de filtres dans Studio. |
| bogue | Studio | Correction d’un bogue en raison duquel certaines cases à cocher des filtres Studio ne pouvaient pas être désactivées. |
