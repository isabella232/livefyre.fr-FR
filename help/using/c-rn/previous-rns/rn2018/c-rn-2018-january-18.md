---
description: Notes de mise à jour de la version du 18 janvier 2018.
seo-description: Notes de mise à jour de la version du 18 janvier 2018.
seo-title: 18 janvier 2018
solution: Experience Manager
title: 18 janvier 2018
uuid: 8141f431-c154-4c8f-bbcd-b7c712fe5f7d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# January 18, 2018{#january}

Notes de mise à jour de la version du 18 janvier 2018.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Applications | Correction d’un bogue qui empêchait le rendu correct des avatars lors de l’utilisation d’un fichier jpeg. |
| bogue | ModQ | Correction d’un bogue pour les clients S1 afin d’autoriser le filtrage par collections dans ModQ. |
| bogue | Flux | Correction d’un bogue qui rompait une règle de flux lorsque le filtre de langue était défini sur "aucun". |
| bogue | Flux | Correction d’un bogue qui empêchait l’enregistrement des règles de flux YouTube. |
| bogue | Flux | Correction d’un bogue en raison duquel les utilisateurs pouvaient créer des entrées géographiques mal formatées dans les règles de flux et les enregistrer, ce qui entraînait l’échec du flux. Désormais, les utilisateurs ne peuvent plus enregistrer de balises géographiques mal formatées. |
| bogue | Studio | Correction d’un problème qui empêchait certains utilisateurs de se connecter à Livefyre. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Bibliothèque | Correction d’un bogue de sécurité. Tous les appels d’authentification sont désormais effectués à l’aide du protocole HTTPS au lieu de HTTP. |
| Amélioration | Balises intelligentes | Le contenu en flux continu est désormais automatiquement balisé intelligemment par Adobe Sensei lorsqu’il est enregistré dans un dossier ou publié dans une application. |
| bogue | Flux | Correction d’un problème en raison duquel les règles de flux Instagram ne reconnaissaient pas les caractères japonais. |
| Amélioration | Flux | Les clients peuvent désormais utiliser les opérateurs logiques ( ANY, ALL, NOT) pour créer des filtres de balises intelligentes détaillés dans les flux qui traitent un contenu beaucoup plus précis. Par exemple, si j'utilise le hashtag #himalyas, je peux choisir de n'afficher que les images qui incluent "des montagnes enneigées". |
| bogue | Studio | Correction d’un bogue qui affichait des caractères spéciaux dans les noms au format HTML. |

