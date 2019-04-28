---
description: Notes de mise à jour de la version du 26 avril 2018.
seo-description: Notes de mise à jour de la version du 26 avril 2018.
seo-title: 26 avril 2018
solution: Experience Manager
title: 26 avril 2018
uuid: a 84 ebe 5 c -40 d 5-43 b 5-a 300-3 e 041 ab 22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 26 avril 2018{#april}

Notes de mise à jour de la version du 26 avril 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* Ajout d&#39;une nouvelle fonctionnalité permettant aux clients de configurer un nombre spécifique de colonnes pour un mur multimédia. Le nombre de colonnes que vous choisissez force le mur multimédia à se placer dans ce nombre de colonnes, quelle que soit la taille. Dans le cas contraire, le nombre de colonnes Mur multimédia est défini par défaut sur « auto » lorsque les colonnes s&#39;ajustent à un nombre qui optimise le mur multimédia pour la taille de l&#39;écran.
* Dans le mur de médias, il existe désormais un basculement permettant de désactiver l&#39;animation automatique du mur multimédia qui survient lorsqu&#39;une page comportant un mur multimédia se charge.
* Vous pouvez désormais choisir le seuil de confiance pour les balises dynamiques dans les flux. La définition du score de précision (0-100) pour les balises permet de contrôler l&#39;exactitude des ressources que nous récupérons.
* Ajout des recommandations de modération. Livefyre analyse désormais chaque publication dans les commentaires et prévoit que vous la pouviez la corbeille ou non en fonction des données historiques et de l&#39;apprentissage automatique. Ces recommandations s&#39;affichent dans modq.
   * Les utilisateurs peuvent désactiver les recommandations de modération, ce qui permet aux utilisateurs de filtrer modq par le contenu Livefyre que vous souhaitez corbeille.
   * Ajout de la capacité de filtrer modq par la balise de recommandation de modération, Corbeille.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Rights Management | Correction d&#39;un problème en raison duquel les demandes de droits ne fonctionnaient pas pour les Ressources après leur recherche dans une recherche sociale. |
| Amélioration | Flux | Mise à jour du mécanisme de diffusion en flux continu qui permet aux contenus de s&#39;étoffer de Facebook pour se conformer à une modification dorsale créée par Facebook. |
| Bogue | Commerce UGC | Correction d&#39;un problème en raison duquel le bouton « Shop » de l&#39;App ne s&#39;affichait pas dans une application de mosaïque ou de film fixe ou dans une application modale lors du survol d&#39;une carte avec un produit lorsque le bouton CTA était activé. |
| Amélioration | Commerce UGC | Correction d&#39;un problème en raison duquel l&#39;indicateur commercial UGC était défini sur « off » par défaut, plutôt que sur « on.  » » |

## Version UAT

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Bibliothèque/Recherche | Correction d&#39;un problème en raison duquel les vidéos ne se chargeaient pas correctement. |
| Amélioration | Studio | Ajout de la capacité de voir les mots suggérés lors de la saisie dans les noms de balise. |

