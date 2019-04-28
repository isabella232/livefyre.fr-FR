---
description: Renvoie un nouvel objet Site.
seo-description: Renvoie un nouvel objet Site.
seo-title: Méthode de réseau getsite
solution: Experience Manager
title: Méthode de réseau getsite
uuid: 67 de 781 e -5240-4 be 5-9 e 93-c 614828 e 0 bb 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Méthode de réseau getsite{#getsite-network-method}

Renvoie un nouvel objet Site.
| Variable | Type | Description|
|— |— |— |
| Siteid | String | The Identifiant fourni pour le site Web ou l&#39;application auquel la collection appartient. Par exemple : 303617. |
| Sitekey | String | The Clé secrète fournie pour siteid. |

## Exemple Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Exemple nodejs {#section_xkd_gds_rz}

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

