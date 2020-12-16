---
description: Renvoie un jeton chiffré authentifié par l’utilisateur pour le réseau à partir duquel il est appelé.
seo-description: Renvoie un jeton chiffré authentifié par l’utilisateur pour le réseau à partir duquel il est appelé.
seo-title: buildUserAuthToken, méthode réseau
solution: Experience Manager
title: buildUserAuthToken, méthode réseau
uuid: 8828d356-c3c6-46a6-91bf-83bd59e35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 6%

---


# buildUserAuthToken Network, méthode{#builduserauthtoken-network-method}

Renvoie un jeton chiffré authentifié par l’utilisateur pour le réseau à partir duquel il est appelé.

| Variable | Type | Description |
|--- |--- |--- |
| l’userID | Chaîne | ID utilisateur de l’utilisateur auquel appartient ce jeton. |
| displayName | Chaîne | Nom d’affichage de l’utilisateur. |
| expire | Double | Date à laquelle le jeton doit expirer en secondes. |

## Exemple Java {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Exemple Python {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Exemple Ruby {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
