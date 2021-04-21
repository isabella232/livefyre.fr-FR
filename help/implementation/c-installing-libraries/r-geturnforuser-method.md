---
description: Cette méthode renvoie l'URL de l'utilisateur de ce réseau.
title: getUrnForUser, méthode réseau
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# getUrnForUser Network, méthode{#geturnforuser-network-method}

Cette méthode renvoie l&#39;URL de l&#39;utilisateur de ce réseau.

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
