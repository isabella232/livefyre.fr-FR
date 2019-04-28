---
description: Renvoie un objet Collection instancié comme type de blog. Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection instancié comme type de blog. Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus de création.
seo-title: Méthode du site buildblogcollection
solution: Experience Manager
title: Méthode du site buildblogcollection
uuid: 6 a 5 ec 6 b 9-bc 32-467 a-abe 6-a 57 c 6 defe 067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Méthode du site buildblogcollection{#buildblogcollection-site-method}

Renvoie un objet Collection instancié comme type de blog. Exécutez create_ or_ update () à partir de l&#39;objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| titre | Chaîne | Titre de la collection. |
| Articleid | Chaîne | Identifiant d&#39;article unique choisi pour identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Exemple nodejs {#section_xkd_gds_rz}

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

