---
description: Notes de mise à jour de la version du 16 novembre 2017.
title: 16 novembre 2017
exl-id: 167b8c7d-f2fb-4735-9681-d349646ec3eb
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 8%

---

# 16 novembre 2017{#november}

Notes de mise à jour de la version du 16 novembre 2017.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | AEM, bibliothèque | Correction d’un bogue en raison duquel aucun résultat n’était renvoyé lors de l’utilisation de la recherche de balises et de notations dans la bibliothèque. |
| bogue | Applications | Correction d’un problème en raison duquel la balise de fonction ne s’affichait pas sur une seule application de carte. |
| bogue | Carrousel | Correction d’un problème en raison duquel le carrousel n’apparaissait pas dans Designer. |
| bogue | Commentaires | Correction du nombre inexact de commentaires dans les applications de commentaires. |
| Amélioration | Carte des fonctionnalités | Toutes les fonctionnalités commerciales de l’application de carte de fonctions sont activées. |
| Amélioration | Filmstrip | Nous avons ajouté des options de redimensionnement pour Filmstrip afin que l’utilisateur puisse mieux contrôler l’aspect des images dans l’application. |
| bogue | Threads chauds | Correction des messages d’erreur provenant des threads dynamiques pour les rendre plus sécurisés. |
| Amélioration | Bibliothèque | Les clients peuvent supprimer les balises actives appliquées par notre système AI. Une fois supprimées, elles ne voient plus ces balises dans les résultats de la recherche. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel une image ne s’affichait pas correctement après l’avoir ajoutée à la bibliothèque à partir d’une recherche sur les réseaux sociaux. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel la création de dossiers était lente. |
| bogue | Bibliothèque | Les utilisateurs peuvent désormais publier des fichiers .mov dans Collections. |
| bogue | Bibliothèque | Les images dont le titre contient des caractères spéciaux ne sont pas téléchargées dans la bibliothèque, ce problème a été corrigé. |
| Amélioration | Bibliothèque | Nous avons mis à jour notre algorithme de classement &quot;pertinence&quot; lorsqu’un utilisateur recherche des balises actives. Ainsi, lorsqu’un utilisateur bascule le tri &quot;pertinence&quot; dans la recherche de bibliothèque, le nouvel algorithme de classement est activé. Ce nouvel algorithme de classement prend en compte, les scores de précision des balises actives, le nombre d’étoiles attribuées par utilisateur et l’âge du document. L’objectif est de rendre l’expérience de recherche de balises plus précise pour l’utilisateur. |
| Amélioration | Bibliothèque | Lorsqu’un client enregistre un fichier dans la bibliothèque, Livefyre utilise la technologie d’apprentissage automatique Adobe Sensei pour ajouter des balises qui décrivent automatiquement ce qui se trouve dans l’image du fichier. Cela permet à l’utilisateur de rechercher ces balises dans le système. |
| Amélioration | Bibliothèque | Lorsqu&#39;un client enregistre un fichier basé sur une image dans la bibliothèque, Livefyre le balisera automatiquement à l&#39;aide de la technologie de l&#39;IA Adobe, en extrayant des fonctions, des catégories et des propriétés esthétiques du système. L’utilisateur peut ainsi effectuer des recherches dans la bibliothèque en fonction de ce qui se trouve à l’intérieur des images, et non seulement du texte. |
| bogue | Identité Livefyre | Les avatars ne se chargeaient pas correctement pour l&#39;implémentation de Microsoft de l&#39;identité LF, ceci a été corrigé. |
| bogue | ModQ | Correction d’un problème en raison duquel la prémodération des flux et ModQ n’affichaient pas correctement tout le contenu. |
| Amélioration | Paramètres | Les clients peuvent maintenant consulter notre politique de confidentialité et les conditions d’Adobe dans un pied de page dans Paramètres. |
| Amélioration | Flux | Correction d’un bogue de prémodération des règles de flux basées sur le courrier électronique. |
| Amélioration | Flux | Ajoute la capacité de filtrer le contenu du flux par langue. |
| Amélioration | Utilisateurs | Ajoute la possibilité d’utiliser des fichiers .png pour les avatars utilisateur. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | App Manager | Correction d’un problème lié à la recherche de balises d’application dans App Manager. |
| bogue | Bibliothèque | Correction d’un problème qui empêchait l’ajout d’étoiles pour plusieurs éléments de contenu à la fois dans la bibliothèque de fichiers. |
| bogue | Studio | Correction d’un problème qui empêchait certains utilisateurs de se connecter à Livefyre. |
