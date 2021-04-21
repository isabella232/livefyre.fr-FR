---
description: Renvoie un objet Collection appelé comme type de commentaires. Exécutez createOrUpdate() à partir de l’objet Collection pour terminer le processus de création.
title: buildCommentsCollection, méthode du site
exl-id: 9534c25a-fd1c-4a09-92e2-d196ac218ef3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# buildCommentsCollection, méthode du site{#buildcommentscollection-site-method}

Renvoie un objet Collection appelé comme type de commentaires. Exécutez createOrUpdate() à partir de l’objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| title | Chaîne | Titre de la collection. |
| articleId | Chaîne | ID d’article unique que vous avez choisi d’identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
