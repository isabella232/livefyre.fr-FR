---
title: buildCollection, méthode du site
description: buildCollection, méthode du site
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 15%

---

# Méthode de site buildCollection{#buildcollection-site-method}

| Variable | Type | Description |
|--- |--- |--- |
| type | CollectionType | Type de la collection. |
| title | Chaîne | Titre de la collection. |
| articleId | Chaîne | ID d’article unique que vous avez choisi d’identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
