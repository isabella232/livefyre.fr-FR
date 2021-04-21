---
description: Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.
title: Jeton d’authentification utilisateur
exl-id: 564144dd-6db4-447b-80ac-b743ecac833d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---

# Jeton d’authentification de l’utilisateur {#user-auth-token}

Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.

Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.

Pour créer le jeton, utilisez votre bibliothèque de langues préférée pour transmettre les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| networkName | Chaîne *requise* | Nom du réseau Livefyre (fourni par Livefyre). |
| networkKey | Chaîne *requise* | La clé secrète de ce réseau spécifique (fournie par Livefyre). |
| l’userID | Chaîne *requise* | ID de l’utilisateur se connectant tel qu’il est stocké dans votre système de gestion des utilisateurs (seuls les caractères alphanumériques, les tirets, les traits de soulignement et les points sont autorisés) : [a-zA-Z0-9_-.]). **Remarque :** l’ID utilisateur doit être unique. |
| expire | Entier *requis* | Date à laquelle le jeton doit expirer à partir de maintenant (en secondes). **Remarque :** Cette valeur peut également être transmise sous la forme d’un nombre flottant. Le jeton Web JSON produit stockera cette valeur dans l’époque UNIX. |
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
>Les clés réseau ne sont pas partagées pour les comptes de démosite Livefyre. Vous recevrez une clé réseau une fois que Livefyre aura mis en service un environnement pour vous. Cette clé doit être gardée privée.
