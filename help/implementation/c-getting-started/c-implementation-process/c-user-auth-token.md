---
description: Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.
seo-description: Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.
seo-title: Jeton d’authentification utilisateur
solution: Experience Manager
title: Jeton d’authentification utilisateur
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Jeton d’authentification utilisateur{#user-auth-token}

Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.

Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.

Pour créer le jeton, utilisez votre bibliothèque de langues préférée pour transmettre les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| networkName | Chaîne *requise* | Nom du réseau Livefyre (fourni par Livefyre). |
| networkKey | Chaîne *requise* | Clé secrète de ce réseau spécifique (fournie par Livefyre). |
| l’userID | Chaîne *requise* | L’ID de l’utilisateur se connectant tel qu’il est stocké dans votre système de gestion des utilisateurs (seuls les caractères alphanumériques, de tiret, de trait de soulignement et de point sont autorisés) : [a-zA-Z0-9_-.]). **** Remarque : L’ID utilisateur doit être unique. |
| expire | Entier *requis* | Date d’expiration du jeton (en secondes). **** Remarque : Cette valeur peut également être transmise sous forme de virgule flottante. Le jeton Web JSON produit stockera cette valeur dans l’époque UNIX. |
| displayName | Chaîne *requise* | Texte permettant d’identifier cet utilisateur dans l’interface utilisateur et dans les commentaires. (Nombre maximal de caractères : 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>Les clés de réseau ne sont pas partagées pour les comptes de démosite Livefyre. Vous recevrez une clé réseau une fois que Livefyre aura mis en service un environnement pour vous. Cette clé doit être gardée privée.

