---
description: Définit SSL pour que les appels d’API soient activés ou désactivés.
seo-description: Définit SSL pour que les appels d’API soient activés ou désactivés.
seo-title: setSSL Network, méthode
solution: Experience Manager
title: setSSL Network, méthode
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---


# setSSL Network Method{#setssl-network-method}

Définit SSL pour que les appels d’API soient activés ou désactivés.

| Variable | Type | Description |
|--- |--- |--- |
| ssl | Booléen | La valeur par défaut est true. si vous souhaitez activer SSL, false dans le cas contraire. <br><ul><li>True - SSL activé </li><li>False - SSL désactivé</li></ul> |

## Exemple Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

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
