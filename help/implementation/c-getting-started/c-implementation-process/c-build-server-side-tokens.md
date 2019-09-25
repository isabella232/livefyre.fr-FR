---
description: Guide de création de jetons CollectionMeta et Auth.
seo-description: Guide de création de jetons CollectionMeta et Auth.
seo-title: Créer des jetons côté serveur
solution: Experience Manager
title: Créer des jetons côté serveur
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Créer des jetons côté serveur{#build-server-side-tokens}

Guide de création de jetons CollectionMeta et Auth.

La création des jetons utilisés par Livefyre pour valider les requêtes vous garantit que vous seul pouvez mettre à jour votre réseau Livefyre.

## CollectionMeta Token

Découvrez comment créer un jeton pour créer et afficher des conversations existantes.

## Jeton d’authentification

Découvrez comment créer un jeton pour authentifier les utilisateurs, étape nécessaire du processus d’intégration si vous n’utilisez pas Janrain Capture pour la gestion des utilisateurs.

## Jeton d’authentification utilisateur {#section_l5l_hwt_bbb}

Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.

Pour créer le jeton, utilisez votre bibliothèque de langues préférée pour transmettre les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| networkName | Chaîne *requise* | Nom du réseau Livefyre (fourni par Livefyre). |
| networkKey | Chaîne *requise* | Clé secrète de ce réseau spécifique (fournie par Livefyre). |
| l’userID | Chaîne *requise* | L’ID de l’utilisateur se connectant tel qu’il est stocké dans votre système de gestion des utilisateurs (seuls les caractères alphanumériques, de tiret, de trait de soulignement et de point sont autorisés) : `[a-zA-Z0-9_-.]`). **** Remarque : L’ID utilisateur doit être unique. |
| expire | Entier *requis* | Date d’expiration du jeton (en secondes). **** Remarque : Cette valeur peut également être transmise sous forme de virgule flottante. Le jeton Web JSON produit stockera cette valeur dans l’époque UNIX. |
| displayName | Chaîne *requise* | Texte permettant d’identifier cet utilisateur dans l’interface utilisateur et dans les commentaires. (Nombre maximal de caractères : 50.) |

