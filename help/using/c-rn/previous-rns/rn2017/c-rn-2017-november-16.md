---
description: Notes de mise à jour de la version du 16 novembre 2017.
seo-description: Notes de mise à jour de la version du 16 novembre 2017.
seo-title: 16 novembre 2017
solution: Experience Manager
title: 16 novembre 2017
uuid: e7d09640-d2c1-4d23-8fa6-ecc90d0b2daa
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 16 novembre 2017{#november}

Notes de mise à jour de la version du 16 novembre 2017.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | AEM, bibliothèque | Correction d’un bogue en raison duquel aucun résultat n’était renvoyé lors de l’utilisation de la recherche Balise et Évaluation dans la bibliothèque. |
| bogue | Applications | Correction d’un problème en raison duquel la balise de fonction ne s’affichait pas sur une application à carte unique. |
| bogue | Carrousel | Correction d’un problème en raison duquel Carousel n’apparaissait pas dans Designer. |
| bogue | Commentaires | Correction du nombre de commentaires inexacts dans les applications de commentaires. |
| Amélioration | Feature Card | Toutes les fonctionnalités commerciales de l’application de carte de fonctionnalités sont activées. |
| Amélioration | Filmstrip | Nous avons ajouté des options de redimensionnement pour le film fixe afin que l’utilisateur puisse mieux contrôler l’aspect des images dans l’application. |
| bogue | Threads chauds | Correction des messages d’erreur des threads chauds pour les rendre plus sécurisés. |
| Amélioration | Bibliothèque | Les clients peuvent supprimer les balises actives appliquées par notre système AI. Une fois supprimées, elles ne verront plus ces balises dans les résultats de la recherche. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel une image ne s’affichait pas correctement après l’avoir ajoutée à la bibliothèque à partir d’une recherche sur les réseaux sociaux. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel la création de dossiers était lente. |
| bogue | Bibliothèque | Les utilisateurs peuvent désormais publier des fichiers .mov dans Collections. |
| bogue | Bibliothèque | Les images comportant des caractères spéciaux dans le titre ne seraient pas téléchargées dans la bibliothèque, ce problème a été corrigé. |
| Amélioration | Bibliothèque | Nous avons mis à jour notre algorithme de classement de "pertinence" lorsqu’un utilisateur recherche des balises actives. Ainsi, lorsqu’un utilisateur bascule le tri de "pertinence" dans la recherche de bibliothèque, le nouvel algorithme de classement est appliqué. Ce nouvel algorithme de classement prend en compte les scores de précision des balises intelligentes, le nombre d’étoiles attribuées par l’utilisateur et l’âge du document. L’objectif est de rendre la recherche de balises plus précise pour l’utilisateur. |
| Amélioration | Bibliothèque | Lorsqu’un client enregistre un fichier dans la bibliothèque, Livefyre utilise la technologie d’apprentissage automatique Adobe Sensei pour ajouter des balises qui décrivent automatiquement ce qui se trouve dans l’image du fichier. Cela permet à l’utilisateur de rechercher ces balises dans le système. |
| Amélioration | Bibliothèque | Lorsqu’un client enregistre un fichier basé sur une image dans la bibliothèque, Livefyre le balisera automatiquement à l’aide de la technologie Adobe AI, en extrayant des fonctionnalités, des catégories et des propriétés esthétiques du système. Cela permet à l’utilisateur de rechercher dans la bibliothèque en fonction de ce qui se trouve à l’intérieur des images, et pas seulement du texte. |
| bogue | Identité Livefyre | Les avatars ne se chargeaient pas correctement pour l'implémentation de Microsoft de l'identité LF, ceci a été corrigé. |
| bogue | ModQ | Correction d’un problème en raison duquel la prémodération des flux et la méthode ModQ n’affichaient pas correctement tout le contenu. |
| Amélioration | Paramètres | Les clients peuvent désormais consulter notre politique de confidentialité et les conditions de service d’Adobe dans un pied de page dans Paramètres. |
| Amélioration | Flux | Correction d’un bogue de prémodération des règles de flux basées sur le courrier électronique. |
| Amélioration | Flux | Ajout de la capacité de filtrer le contenu du flux par langue. |
| Amélioration | Utilisateurs | Ajout de la capacité d’utiliser des fichiers .png pour les avatars utilisateur. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | App Manager | Correction d’un problème lié à la recherche des balises d’application dans App Manager. |
| bogue | Bibliothèque | Correction d’un problème qui empêchait l’ajout d’étoiles pour plusieurs éléments de contenu à la fois dans la bibliothèque de fichiers. |
| bogue | Studio | Correction d’un problème qui empêchait certains utilisateurs de se connecter à Livefyre. |

