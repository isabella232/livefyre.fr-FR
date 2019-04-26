---
description: Notes de mise à jour pour la version du 15 février 2018.
seo-description: Notes de mise à jour pour la version du 15 février 2018.
seo-title: 15 février 2018
solution: Experience Manager
title: 15 février 2018
uuid: ee 46 f 088-9 fb 7-49 e 2-a 42 c-e 0 d 4 b 2 f 24 a 32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 15 février 2018{#february}

Notes de mise à jour pour la version du 15 février 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* **Balises dynamiques.**

   Livefyre utilise la technologie de reconnaissance d'image Adobe Sensei pour baliser automatiquement les images que vous enregistrez dans la bibliothèque.
Avec les balises dynamiques, vous pouvez enregistrer une quantité importante de temps de recherche et de modération du contenu. Avec les balises dynamiques, vous pouvez effectuer les opérations suivantes :

   * Recherche des images enregistrées pour un contenu précis basé sur le contenu de l'image, plutôt que sur le texte uniquement
   * Collecte de contenu dans des flux en fonction de termes de recherche précis qui analyse l'image, plutôt que le texte uniquement
   Pour plus d'informations sur les balises dynamiques, voir [Balises dynamiques](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Messages intégrés.** Lorsque vous vous connectez à Livefyre Studio, une fenêtre d'annonces s'affiche pour afficher les mises à jour sur les nouvelles fonctionnalités.
* **UGC pour Carousel.** Vous pouvez désormais utiliser toutes les fonctions du Commerce UGC dans l'application Livefyre Carousel. Vous pouvez créer un bouton Appel à l'action et connecter votre catalogue de produits à l'application afin de créer une expérience shoppable à partir du Carrousel.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Problème | Modq | Correction d'un problème en raison duquel les publications Instagram marquées comme approuvées ou endommagées entraient à nouveau dans la file d'attente. |
| Amélioration | Rights Management | Ajout d'une amélioration permettant d'afficher un avertissement lorsque vous tentez d'utiliser des comptes Instagram expirés lors de la création de requêtes de droits. |
| Problème | Tendances | Correction d'un problème en raison duquel l'application de tendances autorisait toujours HTTP à parfois, plutôt que HTTPS. |

## Version UAT

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Amélioration | Applications | Ajout de la possibilité de supprimer des applications de Livefyre. |
| Problème | Sondages | Modification des sondages pour utiliser exclusivement HTTPS. Auparavant, les sondages étaient toujours autorisés à être utilisés avec HTTP. |
| Problème | UGC | Correction d'un problème en raison duquel l'UGC dans une application de visualisation n'était pas filtré par - ID du produit comme prévu. |

