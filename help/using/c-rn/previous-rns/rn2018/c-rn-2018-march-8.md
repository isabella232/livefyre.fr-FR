---
description: Notes de mise à jour de la version du 8 mars 2018.
seo-description: Notes de mise à jour de la version du 8 mars 2018.
seo-title: 8 mars 2018
solution: Experience Manager
title: 8 mars 2018
uuid: 4ed67147-0837-4d5e-8e99-532a4278bcce
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 5%

---


# 8 mars 2018{#march}

Notes de mise à jour de la version du 8 mars 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* **Suppression des applications. **Ajouté la possibilité de supprimer des applications dans Studio afin que les utilisateurs puissent mieux gérer la liste de l’application. La suppression d’une application la supprime du tableau, mais elle ne la supprime pas de votre site. L’application continuera à recevoir du contenu d’un flux s’il est configuré pour le faire.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Sondages | Modification des sondages pour utiliser le protocole HTTPS exclusivement. Auparavant, les sondages étaient toujours autorisés à être utilisés avec HTTP. |
| bogue | Studio | Correction d’un problème en raison duquel la fenêtre modale affichait des annonces lorsque vous vous connectiez à Studio pour s’afficher trop grand sur les écrans basse résolution. |

## Version UAT

| Type de problème | Composant | Note de mise à jour |
|--- |--- |--- |
| Amélioration | Filmstrip | Mise à jour des fonctionnalités d’accessibilité suivantes pour Filmstrip : <br><ul><li>Flèches gauche/droite corrigées de &lt;div> à &lt;button> </li><li>L’élément d’image de la prévisualisation a été remplacé par un libellé ARIA moins descriptif de, &quot;Ouvrir la photo jointe&quot;, en un libellé qui lit le nom de la plateforme et le texte de la publication.</li></ul> |
| bogue | Mur multimédia | Correction d’un problème dans le mur multimédia en raison duquel les balises ne pouvaient pas être cliquées lorsqu’une publication Instagram était ajoutée à partir d’une règle de diffusion en continu. |
| Amélioration | Mur multimédia | Amélioration de l’accessibilité du mur multimédia des manières suivantes : <br><ul><li>L’ouverture et la fermeture de modules au moyen des commandes du clavier ne décalent plus la mise au point vers le haut de la page. La cible d’action reste concentrée sur l’élément qui a été le dernier avant la fenêtre contextuelle modale.</li><li>Le bouton Charger plus peut être enfoncé et déclenché à l’aide de la touche Entrée du clavier.</li></ul> |
| bogue | Rights Management | Correction d’une erreur en raison de laquelle vous ne pouviez pas voir le module de demande de droits après l’octroi de droits pour un fichier Instagram. |

