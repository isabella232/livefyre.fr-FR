---
description: Notes de mise à jour de la version du 1er novembre 2018.
seo-description: Notes de mise à jour de la version du 1er novembre 2018.
seo-title: 1er novembre 2018
solution: Experience Manager
title: 1er novembre 2018
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# November 1, 2018{#november}

Notes de mise à jour de la version du 1er novembre 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les nouvelles fonctionnalités suivantes ont été publiées dans la version de production de cette version :

* Balises dynamiques vidéo

   Tirez parti de la technologie de pointe de la vision informatique, optimisée par Adobe Sensei, pour baliser automatiquement le contenu vidéo lorsque vous l’enregistrez dans la bibliothèque. Les balises intelligentes vous aident à gérer l’UGC de manière plus efficace, mais également à créer des règles de traitement (flux) très précises qui collectent le contenu en fonction de ce qui se trouve dans la vidéo, et pas seulement du texte, ce qui vous évite d’avoir beaucoup d’efforts pour modérer le contenu indésirable.

   Détails des fonctionnalités :

   * Les balises actives sont automatiquement ajoutées aux vidéos issues de la recherche sur les réseaux sociaux, aux flux et aux fichiers vidéo téléchargés dans la bibliothèque. Affichage des balises dans les détails de la ressource pour une vidéo individuelle
   * Balises vidéo aux formats .MP4, .MOV et AVI
   * Balises vidéo jusqu’à 60 secondes ou 50 Mo
   * Deux catégories de balises actives s’appliquent aux vidéos : caractéristiques (animaux, objets, lieux, etc.) et actions (course, marche, chant, etc.)
   For more information see [Smart Tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Limite du taux Instagram

   Instagram a modifié le nombre de demandes que toute entreprise utilisant l'API Instagram, y compris Livefyre, peut faire de 5 000 demandes par heure par jeton à 200 demandes par heure par jeton. On parle alors de limitation de *taux*. Pour plus d’informations, voir Limitation des taux [Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* Fichiers audio dans la bibliothèque

   Vous pouvez désormais exécuter les fonctions suivantes sur les fichiers audio à partir du panneau de la bibliothèque :

   * Outils
   * Aperçu
   * Importer
   * Filtrage par fichiers audio
   * Faire glisser des fichiers dans le concepteur

## Problèmes {#section_ehw_ndt_wcb}

Aucun nouveau problème n’a été résolu dans la version de production de cette version. Voir [la section ci-dessus](#c_rn/section_syx_mdt_wcb).

## Version UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Les problèmes des tableaux suivants ont été résolus dans la version UAT de cette version.

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | RGPD | Toutes les données attribuées aux anciens clients dans Analytics seront supprimées. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel une vidéo téléchargée dans la bibliothèque, puis affichée dans les détails de la ressource, ne s’affichait pas correctement. |
| bogue | Mosaïque | Correction d’un problème en raison duquel une mosaïque affichait le dernier élément de contenu d’un carrousel Instagram sous forme de miniature, au lieu d’une carte. |
| bogue | Recherche sociale | Correction d’un problème en raison duquel la recherche sociale sur Instagram ne fonctionnait pas comme prévu. |

