---
description: Renvoie un objet Collection instancié comme type d'évaluation. Exécutez
  create_ or_ update () à partir de l'objet Collection pour terminer le processus
  de création.
seo-description: Renvoie un objet Collection instancié comme type d'évaluation. Exécutez
  create_ or_ update () à partir de l'objet Collection pour terminer le processus
  de création.
seo-title: Méthode du site buildratingscollection
title: Méthode du site buildratingscollection
uuid: 5 eea 2 ba 3-48 e 1-4 cd 2-aa 73-ea 81788 af 1 df
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Méthode du site buildratingscollection{#buildratingscollection-site-method}

Renvoie un objet Collection instancié comme type d'évaluation. Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| titre | Chaîne | Titre de la collection. |
| Articleid | Chaîne | Identifiant d'article unique choisi pour identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## Exemple nodejs {#section_xkd_gds_rz}

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

