---
description: Renvoie un objet Collection instancié comme type de message annexe. Exécutez
  create_ or_ update () à partir de l'objet Collection pour terminer le processus
  de création.
seo-description: Renvoie un objet Collection instancié comme type de message annexe.
  Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus
  de création.
seo-title: Méthode du site buildsitenotescollection
solution: Experience Manager
title: Méthode du site buildsitenotescollection
uuid: 2 bfbc 032-4 c 0 c -48 d 2-8 ce 6-02460 b 38 bd 6 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Méthode du site buildsitenotescollection{#buildsitenotescollection-site-method}

Renvoie un objet Collection instancié comme type de message annexe. Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| titre | Chaîne | Titre de la collection. |
| Articleid | Chaîne | Identifiant d'article unique choisi pour identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Exemple nodejs {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
