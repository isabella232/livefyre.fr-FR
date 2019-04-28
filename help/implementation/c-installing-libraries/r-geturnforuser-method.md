---
description: Cette méthode renvoie l'URN pour l'utilisateur de ce réseau.
seo-description: Cette méthode renvoie l'URN pour l'utilisateur de ce réseau.
seo-title: Méthode réseau geturnforuser
solution: Experience Manager
title: Méthode réseau geturnforuser
uuid: b 70 b 8 b 0 f -2 b 3 a -4 a 1 d -90 d 0-93 a 97 a 137 ad 4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Méthode réseau geturnforuser{#geturnforuser-network-method}

Cette méthode renvoie l&#39;URN pour l&#39;utilisateur de ce réseau.

| Variable | Type | Description |
|--- |--- |--- |
| Userid | Chaîne | ID utilisateur à utiliser dans l&#39;URN. |

## Exemple Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemple nodejs {#section_xkd_gds_rz}

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
