---
description: Renvoie un objet Collection instancié sous forme de type Classement. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection instancié sous forme de type Classement. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-title: buildRatingsCollection, méthode du site
title: buildRatingsCollection, méthode du site
uuid: 5eea2ba3-48e1-4cd2-aa73-ea81788af1df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildRatingsCollection, méthode du site{#buildratingscollection-site-method}

Renvoie un objet Collection instancié sous forme de type Classement. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| title | Chaîne | Titre de la collection. |
| articleId | Chaîne | ID d’article unique que vous avez choisi d’identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

