---
description: Renvoie un jeton chiffré authentifié par l’utilisateur pour le réseau à partir duquel il est appelé.
title: buildUserAuthToken, méthode réseau
exl-id: dcc61c4b-90d9-42a0-9f46-73a843a4ad78
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 8%

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
