---
description: Renvoie un objet Collection appelé comme type de révision. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection appelé comme type de révision. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-title: buildReviewsCollection, méthode du site
solution: Experience Manager
title: buildReviewsCollection, méthode du site
uuid: 88af4c68-57de-4ae9-9394-550c94ede48f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildReviewsCollection, méthode du site{#buildreviewscollection-site-method}

Renvoie un objet Collection appelé comme type de révision. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| title | Chaîne | Titre de la collection. |
| articleId | Chaîne | ID d’article unique que vous avez choisi d’identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |


## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

