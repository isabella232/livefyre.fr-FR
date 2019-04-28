---
description: Cette section décrit comment générer l'objet JSON userauth qui crée le jeton d'authentification utilisateur requis pour enregistrer les utilisateurs dans vos applications.
seo-description: Cette section décrit comment générer l'objet JSON userauth qui crée le jeton d'authentification utilisateur requis pour enregistrer les utilisateurs dans vos applications.
seo-title: Jeton authentique utilisateur
solution: Experience Manager
title: Jeton authentique utilisateur
uuid: 6483 debd -453 c -4780-b 19 c -1 d 8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Jeton authentique utilisateur{#user-auth-token}

Cette section décrit comment générer l&#39;objet JSON userauth qui crée le jeton d&#39;authentification utilisateur requis pour enregistrer les utilisateurs dans vos applications.

Cette section décrit comment générer l&#39;objet JSON userauth qui crée le jeton d&#39;authentification utilisateur requis pour enregistrer les utilisateurs dans vos applications.

Pour créer le jeton, utilisez votre bibliothèque de langue préférée pour transmettre les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| Networkname | Chaîne *requise* | nom du réseau Livefyre (fourni par Livefyre). |
| Networkkey | Chaîne *requise* | Clé secrète de ce réseau spécifique (fourni par Livefyre). |
| Userid | Chaîne *requise* | L&#39;ID de l&#39;utilisateur connecté est stocké dans le système de gestion des utilisateurs (seuls les caractères alphanumériques, les tirets, les tirets bas et les points sont autorisés) : [a-zA-Z 0-9_-.]). **Remarque :** L&#39;ID utilisateur doit être unique. |
| expire | Entier *requis* | Date à laquelle le jeton doit expirer à partir de maintenant (en secondes). **Remarque :** Cette valeur peut également être transmise sous forme de virgule flottante. Le jeton Web JSON produit stockera cette valeur dans l&#39;heure UNIX époque. |
| Displayname | Chaîne *requise* | Texte permettant d&#39;identifier cet utilisateur dans l&#39;interface utilisateur et dans les commentaires. (Nombre maximal de caractères : 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## Nodejs {#section_c42_mjz_1cb}

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
>Les clés réseau ne sont pas partagées pour les comptes de site démographique Livefyre. Vous recevrez une clé réseau une fois que Livefyre a configuré un environnement pour vous. Cette clé doit rester privée.

