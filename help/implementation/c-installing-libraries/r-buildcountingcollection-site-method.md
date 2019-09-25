---
description: Renvoie un objet Collection instancié sous forme de type Comptage. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection instancié sous forme de type Comptage. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-title: buildCountingCollection, méthode du site
title: buildCountingCollection, méthode du site
uuid: e293d66a-0025-4230-997e-295ce4625713
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCountingCollection, méthode du site{#buildcountingcollection-site-method}

Renvoie un objet Collection instancié sous forme de type Comptage. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.

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

