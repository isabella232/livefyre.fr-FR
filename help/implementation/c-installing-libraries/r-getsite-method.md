---
description: Renvoie un nouvel objet Site.
seo-description: Renvoie un nouvel objet Site.
seo-title: getSite Network, méthode
solution: Experience Manager
title: getSite Network, méthode
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# getSite Network Method{#getsite-network-method}

Renvoie un nouvel objet Site.
|Variable|Type|Description|
|— |— |— |
|siteId|String|ID fourni par Livefyre pour le site Web ou l&#39;application auquel appartient la collection. Par exemple : 303617.  |
|siteKey|String|Clé secrète fournie par Livefyre pour siteId.  |

## Exemple Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Exemple Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

