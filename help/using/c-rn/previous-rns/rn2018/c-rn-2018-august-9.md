---
description: Notes de mise à jour pour la version du 9 août 2018.
seo-description: Notes de mise à jour pour la version du 9 août 2018.
seo-title: 9 août 2018
solution: Experience Manager
title: 9 août 2018
uuid: c 59 ae 5 ec -9 d 26-41 c 4-9 a 98-cb 95 c 89 ee 26 a
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 9 août 2018{#august}

Notes de mise à jour pour la version du 9 août 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

**Balises dynamiques vidéo :** Les utilisateurs peuvent désormais afficher des balises dynamiques pour les vidéos de moins de 50 Mo.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Contenu de l'application | Correction d'un problème qui empêchait les administrateurs et les gestionnaires de contenu de modifier le contenu dans le contenu de l'application. |
| Amélioration | Applications | Les réseaux sociaux ont apporté des modifications à la confidentialité que les mentions de réseau social ne seront plus prises en charge pour Facebook ou Twitter. |
| Amélioration | Applications | Les réseaux sociaux ont modifié la confidentialité. La fonctionnalité « Publier vers » qui publie automatiquement le contenu sur les réseaux sociaux (Facebook, linkedin, Twitter) a été supprimée. |
| Amélioration | GDPR | Suppression du basculement pour le mode Détails de la page Détails de la demande sous Paramètres > Confidentialité. Vous pouvez toujours accéder au mode Détails en ajoutant /dbg à la fin de l'URL. |
| Bogue | Intégration : AEM | Correction d'un problème en raison duquel le glisser-déposer des applications Livefyre dans AEM s'affichait pour créer plusieurs applications. |
| Bogue | Bibliothèque | Correction d'un problème en raison duquel un fichier n'était pas enregistré correctement dans la bibliothèque. |
| Bogue | Identité Livefyre | Correction d'un problème lié à l'identité SI qui provoquait des erreurs 403 lors de la connexion. |
| Bogue | Recherche sociale | Correction d'un problème en raison duquel les utilisateurs ne pouvaient pas rechercher de publications Facebook publiques à l'aide de l'option URL de la recherche sociale. |
| Amélioration | Synchronisation sociale | Les réseaux sociaux ont apporté des modifications à la confidentialité qui signifient que la synchronisation sociale ne sera plus prise en charge pour Facebook. |
| Amélioration | Flux | Désormais, lorsque vous supprimez une application, vous supprimez tous les flux associés à cette application. |
| Amélioration | Studio | Les clients ont désormais la possibilité de transmettre des événements Livefyre à Adobe Analytics individuellement par rapport aux lots. |
| Amélioration | Studio | Les fenêtres modales qui s'affichent dans les applications de conversation pour les réseaux sociaux seront désormais des fenêtres modales à partir du réseau social au lieu d'Adobe Experience Manager Livefyre ou d'autres fenêtres modales de marque. |

## Version UAT

Les problèmes des tableaux suivants ont été résolus dans la version de la version UAT.

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | GDPR | Correction d'un problème en raison duquel les messages d'exclusion ne s'affichaient pas pour certaines vidéos Instagram. |
| Bogue | Bibliothèque | Correction d'un problème en raison duquel une carte avec droits accordés affichait manuellement un état incorrect de demande de droits. |
| Bogue | Bibliothèque | Correction d'un problème en raison duquel un fichier n'était pas enregistré dans un dossier. |
| Bogue | Bibliothèque/Recherche | Possibilité de rechercher des URL à partir d'Instagram dans la recherche sociale. |
| Bogue | Modq | Correction d'un problème en raison duquel le menu Plus d'informations dans modq ne s'affichait pas comme prévu. |
| Bogue | Rights Management | Correction d'un problème en raison duquel le tri dans modq devait se trouver à une position fixe lorsque la page défilait. |
| Bogue | Flux | Correction d'un problème d'affichage des flux dans l'environnement d'évaluation. |
| Amélioration | Flux | Ajout d'un basculement sécurisé pour Work for Work (SFW) et Non sécurisé au travail (NSFW) en flux continu. |
| Amélioration | Studio | Ajout de la fonctionnalité de balises intelligente au contenu transféré vers la bibliothèque Livefyre Studio via filestack (fonctionnalité de transfert dans Tous les actifs). |

