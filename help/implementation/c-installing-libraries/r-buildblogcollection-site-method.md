---
description: Renvoie un objet Collection appelé en tant que type de blog. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection appelé en tant que type de blog. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.
seo-title: buildBlogCollection, méthode du site
solution: Experience Manager
title: buildBlogCollection, méthode du site
uuid: 6a5ec6b9-bc32-467a-abe6-a57c6defe067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildBlogCollection, méthode du site{#buildblogcollection-site-method}

Renvoie un objet Collection appelé en tant que type de blog. Exécutez create_or_update() depuis l'objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| title | Chaîne | Titre de la collection. |
| articleId | Chaîne | ID d’article unique que vous avez choisi d’identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

