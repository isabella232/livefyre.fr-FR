---
description: Notes de mise à jour de la version du 15 février 2018.
seo-description: Notes de mise à jour de la version du 15 février 2018.
seo-title: 15 février 2018
solution: Experience Manager
title: 15 février 2018
uuid: ee46f088-9fb7-49e2-a42c-e0d4b2f24a32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 5%

---


# 15 février 2018{#february}

Notes de mise à jour de la version du 15 février 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* **Balises dynamiques.**

   Livefyre utilise la technologie de reconnaissance d’images Adobe Sensei pour baliser automatiquement les images que vous enregistrez dans la bibliothèque.
Avec les balises actives, vous pouvez gagner un temps considérable en recherchant et en modérant le contenu. Avec les balises actives, vous pouvez :

   * Rechercher dans les images enregistrées un contenu précis basé sur le contenu de l’image, plutôt que sur du texte uniquement
   * Collecte de contenu dans des flux basés sur des termes de recherche précis qui analysent l’image, plutôt que sur du texte uniquement

   Pour plus d’informations sur les balises actives, voir [Balises dynamiques](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Messages internes au produit.** Désormais, lorsque vous vous connectez à Livefyre Studio, une fenêtre d’annonces s’affiche pour afficher les mises à jour des nouvelles fonctionnalités.
* **UGC pour Carousel.** Vous pouvez désormais utiliser toutes les fonctions d’UGC Commerce dans l’application Livefyre Carousel. Vous pouvez créer un bouton d’appel à l’action et connecter votre catalogue de produits à l’application afin de créer une expérience d’achat à partir de Carousel.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Problème | ModQ | Correction d’un problème en raison duquel les publications Instagram marquées comme approuvées ou détruites réentraient dans la file d’attente. |
| Amélioration | Rights Management | Amélioration Ajoutée afin d’afficher un avertissement lors de l’utilisation de comptes Instagram expirés lors de l’exécution de demandes de droits. |
| Problème | Tendances | Correction d’un problème en raison duquel l’application Trends permettait parfois le protocole HTTP plutôt que HTTPS. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | Applications | Ajoute la possibilité de supprimer des applications de Livefyre. |
| Problème | Sondages | Modification des sondages pour utiliser le protocole HTTPS exclusivement. Auparavant, les sondages étaient toujours autorisés à être utilisés avec HTTP. |
| Problème | UGC | Correction d’un problème en raison duquel l’UGC dans une application de visualisation ne filtrait pas par ID de produit comme prévu. |

