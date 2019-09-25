---
description: Informe Livefyre de mettre à jour l’URL de synchronisation utilisateur du réseau vers celle fournie. Renvoie une valeur de type Boolean.
seo-description: Informe Livefyre de mettre à jour l’URL de synchronisation utilisateur du réseau vers celle fournie. Renvoie une valeur de type Boolean.
seo-title: setUserSyncUrl, méthode réseau
solution: Experience Manager
title: setUserSyncUrl, méthode réseau
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncUrl, méthode réseau{#setusersyncurl-network-method}

Informe Livefyre de mettre à jour l’URL de synchronisation utilisateur du réseau vers celle fournie. Renvoie une valeur de type Boolean.

| Variable | Type | Description |
|--- |--- |--- |
| urlTemplate | Chaîne | URL d’enregistrement auprès de Livefyre pour la synchronisation des ID utilisateur. "`{id}`" doit faire partie de la chaîne URL fournie. |

## Exemple Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exemple de sortie :

```
true
```

## Exemple NodeJS {#section_xkd_gds_rz}

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
