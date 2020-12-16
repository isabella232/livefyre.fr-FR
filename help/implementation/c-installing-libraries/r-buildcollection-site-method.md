---
description: valeur nulle
seo-description: valeur nulle
seo-title: buildCollection, méthode du site
solution: Experience Manager
title: buildCollection, méthode du site
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 17%

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
