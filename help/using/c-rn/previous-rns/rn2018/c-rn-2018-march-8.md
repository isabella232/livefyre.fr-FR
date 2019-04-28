---
description: Notes de mise à jour pour la version du 8 mars 2018.
seo-description: Notes de mise à jour pour la version du 8 mars 2018.
seo-title: 8 mars 2018
solution: Experience Manager
title: 8 mars 2018
uuid: 4 ed 67147-0837-4 d 5 e -8 e 99-532 a 4278 bcce
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 8 mars 2018{#march}

Notes de mise à jour pour la version du 8 mars 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* ** Suppression d&#39;applications. ** Ajout de la possibilité de supprimer des applications dans Studio afin que les utilisateurs puissent mieux gérer la liste des applications. La suppression d&#39;une application la supprime du tableau, mais elle ne supprime pas l&#39;application de votre site. L&#39;application continue de recevoir le contenu d&#39;un flux s&#39;il est configuré pour le faire.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Sondages | Modification des sondages pour utiliser exclusivement HTTPS. Auparavant, les sondages étaient toujours autorisés à être utilisés avec HTTP. |
| Bogue | Studio | Correction d&#39;un problème en raison duquel la fenêtre modale affichait les annonces lorsque vous vous connectiez à Studio pour afficher trop grand sur les écrans à faible résolution. |

## Version UAT

| Type de publication | Composant | Note de version |
|--- |--- |--- |
| Amélioration | Film fixe | Mise à jour des fonctionnalités d&#39;accessibilité suivantes pour le film fixe : <br><ul><li>Flèches gauche/droite corrigées de &lt; div &gt; en &lt; bouton &gt; </li><li>L&#39;élément d&#39;image de prévisualisation a été modifié d&#39;un libellé ARIA moins descriptif, « Ouvrir la photo jointe », à une étiquette qui lit le nom de la plateforme et du texte de la publication.</li></ul> |
| Bogue | Mur multimédia | Correction d&#39;un problème dans le mur multimédia en raison duquel les balises n&#39;étaient pas cliquables lorsqu&#39;une publication Instagram était ajoutée à partir d&#39;une règle de diffusion en continu. |
| Amélioration | Mur multimédia | Amélioration de l&#39;accessibilité du mur multimédia comme suit : <br><ul><li>Les options d&#39;ouverture et de fermeture par l&#39;intermédiaire des commandes du clavier ne repassent plus au début de la page. La cible d&#39;action reste à la place sur l&#39;élément qui vient d&#39;être ciblé avant la fenêtre contextuelle modale.</li><li>Le bouton Charger plus peut être comprimé et déclenché à l&#39;aide de la touche Entrée du clavier.</li></ul> |
| Bogue | Rights Management | Correction d&#39;une erreur qui empêchait l&#39;affichage du modal de demande des droits après l&#39;octroi des droits d&#39;un fichier Instagram. |

