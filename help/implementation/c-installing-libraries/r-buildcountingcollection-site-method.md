---
description: Renvoie un objet Collection instancié comme type de comptage. Exécutez
  create_ or_ update () à partir de l'objet Collection pour terminer le processus
  de création.
seo-description: Renvoie un objet Collection instancié comme type de comptage. Exécutez
  create_ or_ update () à partir de l'objet Collection pour terminer le processus
  de création.
seo-title: Méthode du site buildcountingcollection
title: Méthode du site buildcountingcollection
uuid: e 293 d 66 a -0025-4230-997 e -295 ce 4625713
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Méthode du site buildcountingcollection{#buildcountingcollection-site-method}

Renvoie un objet Collection instancié comme type de comptage. Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| titre | Chaîne | Titre de la collection. |
| Articleid | Chaîne | Identifiant d'article unique choisi pour identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## Exemple nodejs {#section_xkd_gds_rz}

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

