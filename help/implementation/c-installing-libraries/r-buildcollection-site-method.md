---
description: valeur nulle
seo-description: valeur nulle
seo-title: Méthode du site buildcollection
solution: Experience Manager
title: Méthode du site buildcollection
uuid: 52 abc 42 a -9506-4492-b 219-f 2 e 05 eb 79 c 5 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Méthode du site buildcollection{#buildcollection-site-method}

| Variable | Type | Description |
|--- |--- |--- |
| type | Collectiontype | Type de la collection. |
| titre | Chaîne | Titre de la collection. |
| Articleid | Chaîne | Identifiant d&#39;article unique choisi pour identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Exemple nodejs {#section_xkd_gds_rz}

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
