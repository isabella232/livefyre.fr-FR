---
description: Notes de mise à jour de la version du 18 janvier 2018.
title: 18 janvier 2018
exl-id: aaf49dc9-64eb-4354-8bcb-04039fa25f10
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 7%

---

# 18 janvier 2018{#january}

Notes de mise à jour de la version du 18 janvier 2018.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Applications | Correction d’un bogue qui empêchait le rendu correct des avatars lors de l’utilisation d’un fichier jpeg. |
| bogue | ModQ | Correction d’un bogue pour les clients S1 qui autorisait le filtrage par collections dans ModQ. |
| bogue | Flux | Correction d’un bogue en raison duquel une règle de flux était rompue lorsque le filtre de langue était défini sur &quot;aucun&quot;. |
| bogue | Flux | Correction d’un bogue qui empêchait l’enregistrement des règles de flux Youtube. |
| bogue | Flux | Correction d’un bogue en raison duquel les utilisateurs pouvaient créer des entrées géographiques mal formatées dans les règles de flux et les enregistrer, ce qui provoquait l’échec du flux. Désormais, les utilisateurs ne peuvent plus enregistrer de balises géographiques mal formatées. |
| bogue | Studio | Correction d’un problème qui empêchait certains utilisateurs de se connecter à Livefyre. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Bibliothèque | Correction d’un bogue de sécurité. Tous les appels d’authentification sont désormais effectués à l’aide du protocole HTTPS au lieu du protocole HTTP. |
| Amélioration | Balises actives | Le contenu en flux continu est désormais automatiquement balisé par Adobe Sensei lorsqu’il est enregistré dans un dossier ou publié dans une application. |
| bogue | Flux | Correction d’un problème en raison duquel les règles de flux Instagram ne reconnaissaient pas les caractères japonais. |
| Amélioration | Flux | Les clients peuvent désormais utiliser les opérateurs logiques ( ANY, ALL, NOT) pour créer des filtres détaillés de balises intelligentes dans des flux qui gèrent un contenu beaucoup plus précis. Par exemple, si j&#39;utilise le hashtag #himalyas, je peux choisir de ne montrer que des images qui incluent &quot;des montagnes enneigées&quot;. |
| bogue | Studio | Correction d’un bogue qui affichait des caractères spéciaux dans les noms au format HTML. |
