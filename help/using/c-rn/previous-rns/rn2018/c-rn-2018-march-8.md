---
description: Notes de mise à jour pour la version du 8 mars 2018.
seo-description: Notes de mise à jour pour la version du 8 mars 2018.
seo-title: 8 mars 2018
solution: Experience Manager
title: 8 mars 2018
uuid: 4 ed 67147-0837-4 d 5 e -8 e 99-532 a 4278 bcce
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 8 mars 2018{#march}

Notes de mise à jour pour la version du 8 mars 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* ** Suppression d'applications. ** Ajout de la possibilité de supprimer des applications dans Studio afin que les utilisateurs puissent mieux gérer la liste des applications. La suppression d'une application la supprime du tableau, mais elle ne supprime pas l'application de votre site. L'application continue de recevoir le contenu d'un flux s'il est configuré pour le faire.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Sondages | Modification des sondages pour utiliser exclusivement HTTPS. Auparavant, les sondages étaient toujours autorisés à être utilisés avec HTTP. |
| Bogue | Studio | Correction d'un problème en raison duquel la fenêtre modale affichait les annonces lorsque vous vous connectiez à Studio pour afficher trop grand sur les écrans à faible résolution. |

## Version UAT

| Type de publication | Composant | Note de version |
|--- |--- |--- |
| Amélioration | Film fixe | Mise à jour des fonctionnalités d'accessibilité suivantes pour le film fixe : <br><ul><li>Flèches gauche/droite corrigées de < div > en < bouton > </li><li>L'élément d'image de prévisualisation a été modifié d'un libellé ARIA moins descriptif, « Ouvrir la photo jointe », à une étiquette qui lit le nom de la plateforme et du texte de la publication.</li></ul> |
| Bogue | Mur multimédia | Correction d'un problème dans le mur multimédia en raison duquel les balises n'étaient pas cliquables lorsqu'une publication Instagram était ajoutée à partir d'une règle de diffusion en continu. |
| Amélioration | Mur multimédia | Amélioration de l'accessibilité du mur multimédia comme suit : <br><ul><li>Les options d'ouverture et de fermeture par l'intermédiaire des commandes du clavier ne repassent plus au début de la page. La cible d'action reste à la place sur l'élément qui vient d'être ciblé avant la fenêtre contextuelle modale.</li><li>Le bouton Charger plus peut être comprimé et déclenché à l'aide de la touche Entrée du clavier.</li></ul> |
| Bogue | Rights Management | Correction d'une erreur qui empêchait l'affichage du modal de demande des droits après l'octroi des droits d'un fichier Instagram. |

