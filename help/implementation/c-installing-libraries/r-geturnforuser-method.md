---
description: Cette méthode renvoie l’URL de l’utilisateur de ce réseau.
seo-description: Cette méthode renvoie l’URL de l’utilisateur de ce réseau.
seo-title: getUrnForUser Network, méthode
solution: Experience Manager
title: getUrnForUser Network, méthode
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getUrnForUser Network, méthode{#geturnforuser-network-method}

Cette méthode renvoie l’URL de l’utilisateur de ce réseau.

| Variable | Type | Description |
|--- |--- |--- |
| l’userID | Chaîne | ID utilisateur à utiliser dans l’URL. |

## Exemple Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemple Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemple Ruby {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
