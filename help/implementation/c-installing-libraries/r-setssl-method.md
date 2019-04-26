---
description: Définit SSL pour que les appels d'API soient activés ou désactivés.
seo-description: Définit SSL pour que les appels d'API soient activés ou désactivés.
seo-title: Méthode réseau setssl
solution: Experience Manager
title: Méthode réseau setssl
uuid: 8 d 989 e 63-c 859-456 a -99 ca -8 d 87933913 ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Méthode réseau setssl{#setssl-network-method}

Définit SSL pour que les appels d'API soient activés ou désactivés.

| Variable | Type | Description |
|--- |--- |--- |
| ssl | Booléen | La valeur par défaut est true. si vous souhaitez que SSL soit activé, false dans le cas contraire. <br><ul><li>True - SSL activé </li><li>False - SSL désactivé</li></ul> |

## Exemple Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Exemple nodejs {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Exemple Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Exemple Ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
