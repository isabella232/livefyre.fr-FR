---
description: This method returns the URN for this Collection. Vous devez exécuter createOrUpdate() avant d’exécuter cette méthode.
seo-description: This method returns the URN for this Collection. Vous devez exécuter createOrUpdate() avant d’exécuter cette méthode.
seo-title: getUrn, méthode de collecte
solution: Experience Manager
title: getUrn, méthode de collecte
uuid: 2f4d7796-2ae5-4b74-a958-40825c6bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

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

