---
description: Notes de mise à jour de la version du 26 avril 2018.
seo-description: Notes de mise à jour de la version du 26 avril 2018.
seo-title: 26 avril 2018
solution: Experience Manager
title: 26 avril 2018
uuid: a84ebe5c-40d5-43b5-a300-3e041ab22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 4%

---


# 26 avril 2018{#april}

Notes de mise à jour de la version du 26 avril 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* Ajouté une nouvelle fonctionnalité qui permet aux clients de configurer un nombre spécifique de colonnes pour une paroi multimédia. Le nombre de colonnes que vous choisissez forcera le mur multimédia à inclure ce nombre de colonnes, quelle que soit la taille. Dans le cas contraire, le nombre de colonnes du mur multimédia est défini par défaut sur &quot;auto&quot;, où les colonnes s’ajustent à un nombre qui optimise le mur multimédia pour la taille de l’écran.
* Dans Media Wall Designer, il existe désormais une bascule qui permet de désactiver l’animation automatique du mur multimédia qui se produit lorsqu’une page comportant un mur multimédia se charge.
* Vous pouvez désormais choisir le seuil de confiance pour les balises actives dans les flux. La définition du score de précision (0-100) pour les balises permet de contrôler la précision des ressources que nous récupérons.
* Recommandations de modération Ajoutées. Livefyre analyse désormais chaque publication dans les commentaires Apps et prédit si vous allez la corrompre ou non en fonction de données historiques et de l&#39;apprentissage automatique. Ces recommandations s’affichent dans ModQ.
   * Les utilisateurs peuvent désactiver les recommandations de modération, qui permettent aux utilisateurs de filtrer ModQ selon le contenu que Livefyre pense que vous allez corrompre.
   * Ajoute la capacité de filtrer ModQ par la balise de recommandation de modération, Corbeille.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Rights Management | Correction d’un problème en raison duquel les demandes de droits ne fonctionnaient pas pour les ressources après les avoir trouvées dans une recherche sur les réseaux sociaux. |
| Amélioration | Flux | Mise à jour du mécanisme de diffusion en flux continu qui permet au contenu de diffuser en continu à partir de Facebook afin de se conformer à une modification principale créée par Facebook. |
| bogue | UGC Commerce | Correction d’un problème en raison duquel le bouton &quot;Acheter&quot; de la LTC ne s’affichait pas dans une application Mosaic ou Filmstrip ou dans un module de produits lorsque vous survoliez une carte avec un produit lorsque le bouton CTA était activé. |
| Amélioration | UGC Commerce | Correction d’un problème en raison duquel l’indicateur de commerce UGC était défini sur &quot;désactivé&quot; par défaut au lieu de &quot;activé&quot;. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Bibliothèque/Recherche | Correction d’un problème en raison duquel le téléchargement des vidéos n’était pas correct. |
| Amélioration | Studio | Ajoute la possibilité d’afficher les mots suggérés lors de la saisie dans les noms de balise. |

