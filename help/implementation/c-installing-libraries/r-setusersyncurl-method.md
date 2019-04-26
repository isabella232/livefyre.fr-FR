---
description: Informe Livefyre de la mise à jour de l'URL de synchronisation des utilisateurs
  du réseau vers celle fournie. Renvoie une valeur booléenne.
seo-description: Informe Livefyre de la mise à jour de l'URL de synchronisation des
  utilisateurs du réseau vers celle fournie. Renvoie une valeur booléenne.
seo-title: Setusersyncurl Network Method
solution: Experience Manager
title: Setusersyncurl Network Method
uuid: cd 067 e 90-a 2 da -4 e 3 d -8 e 60-7 eabfd 86 fc 7 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Setusersyncurl Network Method{#setusersyncurl-network-method}

Informe Livefyre de la mise à jour de l'URL de synchronisation des utilisateurs du réseau vers celle fournie. Renvoie une valeur booléenne.

| Variable | Type | Description |
|--- |--- |--- |
| Urltemplate | Chaîne | URL de l'enregistrement avec Livefyre pour synchroniser l'utilisateur - ID. Nécessite « `{id}` » pour faire partie de la chaîne URL fournie. |

## Exemple Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exemple de sortie :

```
true
```

## Exemple nodejs {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exemple de sortie :

```
true
```

## Exemple PHP {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Exemple de sortie :

```
true
```

## Exemple Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exemple de sortie :

```
True
```

## Exemple Ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exemple de sortie :

```
True
```
