---
description: Renvoie un objet Collection instancié sous la forme d’un type Comptage. Exécutez create_or_update() à partir de l'objet Collection pour terminer le processus de création.
title: buildCountingCollection, méthode du site
exl-id: 02186eff-1f2f-41e5-8232-033b646ef224
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# buildCountingCollection, méthode du site{#buildcountingcollection-site-method}

Renvoie un objet Collection instancié sous la forme d’un type Comptage. Exécutez create_or_update() à partir de l&#39;objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| title | Chaîne | Titre de la collection. |
| articleId | Chaîne | ID d’article unique que vous avez choisi d’identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```
