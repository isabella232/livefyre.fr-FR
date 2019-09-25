---
description: Renvoie un objet Collection instancié sous forme de type Comments. Exécutez createOrUpdate() à partir de l’objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection instancié sous forme de type Comments. Exécutez createOrUpdate() à partir de l’objet Collection pour terminer le processus de création.
seo-title: buildCommentsCollection, méthode du site
solution: Experience Manager
title: buildCommentsCollection, méthode du site
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCommentsCollection, méthode du site{#buildcommentscollection-site-method}

Renvoie un objet Collection instancié sous forme de type Comments. Exécutez createOrUpdate() à partir de l’objet Collection pour terminer le processus de création.

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
