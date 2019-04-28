---
description: Notes de mise à jour de la version du 18 janvier 2018.
seo-description: Notes de mise à jour de la version du 18 janvier 2018.
seo-title: 18 janvier 2018
solution: Experience Manager
title: 18 janvier 2018
uuid: 8141 f 431-c 154-4 c 8 f-bbcd-b 7 c 712 fe 5 f 7 d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 18 janvier 2018{#january}

Notes de mise à jour de la version du 18 janvier 2018.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Applications | Correction d&#39;un bogue qui empêchait le rendu correct des Avatars lors de l&#39;utilisation d&#39;un fichier JPEG. |
| Bogue | Modq | Correction d&#39;un bogue pour les clients S 1 afin de permettre le filtrage par collections dans le modq. |
| Bogue | Flux | Correction d&#39;un bogue qui rompt une règle de diffusion en continu lorsque le filtre de langue était défini sur « Aucun ».  » » |
| Bogue | Flux | Correction d&#39;un bogue qui empêchait l&#39;enregistrement des règles de flux Youtube. |
| Bogue | Flux | Correction d&#39;un bogue en raison duquel les utilisateurs pouvaient créer des entrées géographiques incorrectes dans les règles de diffusion en continu et les enregistrer, ce qui provoquait l&#39;échec du flux. Désormais, les utilisateurs ne peuvent plus enregistrer de balises géographiques mal formatées. |
| Bogue | Studio | Correction d&#39;un problème qui empêchait certains utilisateurs de se connecter à Livefyre. |

## Version UAT

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Bibliothèque | Correctif de sécurité. Tous les appels d&#39;authentification sont désormais effectués via le protocole HTTPS au lieu du protocole HTTP. |
| Amélioration | Balises dynamiques | Le contenu en flux continu est désormais automatiquement balisé par Adobe Sensei, car il est enregistré dans un dossier ou publié dans une application. |
| Bogue | Flux | Correction d&#39;un problème en raison duquel les règles de flux Instagram ne reconnaissaient pas les caractères japonais. |
| Amélioration | Flux | Les clients peuvent désormais utiliser les opérateurs logiques (ANY, ALL, NOT) pour créer des filtres de balises intelligente détaillés dans les flux qui traitent un contenu bien plus précis. Par exemple, si j&#39;utilise le hashtag # himalyas, je peux choisir de n&#39;afficher que les images incluant « montagnes ». |
| Bogue | Studio | Correction d&#39;un bogue qui affichait des caractères spéciaux dans les noms au format HTML. |

