---
description: Définit SSL pour que les appels d’API soient activés ou désactivés.
title: setSSL Network, méthode
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

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
