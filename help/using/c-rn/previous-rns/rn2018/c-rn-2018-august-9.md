---
description: Notes de mise à jour de la version du 9 août 2018.
seo-description: Notes de mise à jour de la version du 9 août 2018.
seo-title: 9 août 2018
solution: Experience Manager
title: 9 août 2018
uuid: c59ae5ec-9d26-41c4-9a98-cb95c89ee26a
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 9 août 2018{#august}

Notes de mise à jour de la version du 9 août 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

**** Balises dynamiques vidéo : Les utilisateurs peuvent désormais voir les balises actives pour les vidéos de moins de 50 Mo.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Contenu de l’application | Correction d’un problème qui empêchait les administrateurs et les gestionnaires de contenu de modifier le contenu dans l’application Contenu. |
| Amélioration | Applications | Les réseaux sociaux ont apporté des modifications à la confidentialité, ce qui signifie que les mentions sociales ne seront plus prises en charge pour Facebook ou Twitter. |
| Amélioration | Applications | Les réseaux sociaux ont apporté des changements à la vie privée. La fonction "Publier vers" qui publie automatiquement le contenu sur les réseaux sociaux (Facebook, LinkedIn, Twitter) a été supprimée. |
| Amélioration | RGPD | Suppression de la bascule du mode Détails de la page des détails de la requête sous Paramètres &gt; Confidentialité. Vous pouvez toujours accéder au basculement du mode Détails en ajoutant /dbg à la fin de l'URL. |
| bogue | Intégration : AEM | Correction d’un problème en raison duquel les applications Livefyre par glisser-déposer dans AEM semblaient créer plusieurs applications. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel un fichier n’était pas enregistré correctement dans la bibliothèque. |
| bogue | Identité Livefyre | Correction d’un problème d’identité LF qui provoquait des erreurs 403 lors de la connexion. |
| bogue | Recherche sociale | Correction d’un problème en raison duquel les utilisateurs ne parvenaient pas à rechercher des publications Facebook publiques à l’aide de l’option URL dans Recherche sociale. |
| Amélioration | Social Sync | Les réseaux sociaux ont apporté des modifications à la confidentialité qui signifient que Social Sync ne sera plus pris en charge pour Facebook. |
| Amélioration | Flux | Désormais, lorsque vous supprimez une application, vous supprimez tous les flux associés à cette application. |
| Amélioration | Studio | Les clients ont désormais la possibilité d’émettre des événements Livefyre à Adobe Analytics individuellement plutôt que par lots. |
| Amélioration | Studio | Les fenêtres modales qui s’affichent dans les applications de conversation pour les réseaux sociaux sont désormais des fenêtres modales du réseau social au lieu d’Adobe Experience Manager Livefyre ou d’autres fenêtres modales de marque. |

## Version UAT

Les problèmes des tableaux suivants ont été résolus dans la version UAT.

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | RGPD | Correction d’un problème en raison duquel les messages d’exclusion ne s’affichaient pas pour certaines vidéos Instagram. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel une carte avec des droits accordés affichait manuellement un état de demande de droits incorrect. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel un fichier ne pouvait pas être enregistré dans un dossier. |
| bogue | Bibliothèque/Recherche | Restauration de la capacité de rechercher des URL à partir d’Instagram dans Social Search. |
| bogue | ModQ | Correction d’un problème en raison duquel le menu Plus d’informations dans ModQ ne s’affichait pas comme prévu. |
| bogue | Rights Management | Correction d’un problème en raison duquel le tri dans ModQ devait se trouver dans une position fixe lorsque la page défilait. |
| bogue | Flux | Correction d’un problème d’affichage des flux sur l’environnement d’évaluation. |
| Amélioration | Flux | Ajout d’un commutateur Safe For Work (SFW) et Not Safe For Work (NSFW) aux flux. |
| Amélioration | Studio | Ajout de la fonctionnalité de balises actives au contenu téléchargé dans la bibliothèque Livefyre Studio via FileStack (fonctionnalité de téléchargement dans tous les fichiers). |

