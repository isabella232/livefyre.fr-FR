---
description: Renvoie un jeton Livefyre valide chiffré qui peut être utilisé pour interagir avec d’autres API Livefyre pour le réseau à partir duquel il est appelé.
seo-description: Renvoie un jeton Livefyre valide chiffré qui peut être utilisé pour interagir avec d’autres API Livefyre pour le réseau à partir duquel il est appelé.
seo-title: buildLivefyreToken, méthode réseau
solution: Experience Manager
title: buildLivefyreToken, méthode réseau
uuid: 7c72a05f-669b-4df3-8117-aa4af2f7a179
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildLivefyreToken, méthode réseau{#buildlivefyretoken-network-method}

Renvoie un jeton Livefyre valide chiffré qui peut être utilisé pour interagir avec d’autres API Livefyre pour le réseau à partir duquel il est appelé.

Renvoie un jeton Livefyre valide chiffré qui peut être utilisé pour interagir avec d’autres API Livefyre pour le réseau à partir duquel il est appelé.

Par défaut, ce jeton expire dans les 24 heures suivant sa création.

## Exemple Java {#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
network.buildLivefyreToken(); 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Exemple PHP {#section_ghf_gds_rz}

```
network.buildLivefyreToken(); 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Exemple Python {#section_dwg_gds_rz}

```
network.build_livefyre_token() 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Exemple Ruby {#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

Exemple de sortie :

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

