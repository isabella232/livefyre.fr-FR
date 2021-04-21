---
description: Cette méthode renvoie l’URL pour cette collection. Vous devez exécuter createOrUpdate() avant d’exécuter cette méthode.
title: getUrn, méthode de collecte
exl-id: bea04805-8f02-4c06-9a1a-6b057de831ab
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# getUrn, méthode de collecte{#geturn-collection-method}

Cette méthode renvoie l’URL pour cette collection. Vous devez exécuter createOrUpdate() avant d’exécuter cette méthode.

## Exemple Java {#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
collection.getUrn(); 
```

Exemple de sortie :

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection.urn() 
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection.urn
```

Exemple de sortie :

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```
