---
description: Renvoie un objet Collection appelé de type Chat. Exécutez create_or_update() à partir de l'objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection appelé de type Chat. Exécutez create_or_update() à partir de l'objet Collection pour terminer le processus de création.
seo-title: buildChatCollection, méthode du site
solution: Experience Manager
title: buildChatCollection, méthode du site
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# buildChatCollection, méthode du site{#buildchatcollection-site-method}

Renvoie un objet Collection appelé de type Chat. Exécutez create_or_update() à partir de l&#39;objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| title | Chaîne | Titre de la collection. |
| articleId | Chaîne | ID d’article unique que vous avez choisi d’identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Exemple Python {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
