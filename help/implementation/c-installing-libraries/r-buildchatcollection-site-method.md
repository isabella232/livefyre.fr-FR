---
description: Renvoie un objet Collection instancié comme type de conversation. Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus de création.
seo-description: Renvoie un objet Collection instancié comme type de conversation. Exécutez create_ or_ update () à partir de l'objet Collection pour terminer le processus de création.
seo-title: Méthode du site buildchatcollection
solution: Experience Manager
title: Méthode du site buildchatcollection
uuid: 39 ee 32 d 0-29 c 9-47 a 8-a 458-a 3 cf 7 a 96 db 30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# Méthode du site buildchatcollection{#buildchatcollection-site-method}

Renvoie un objet Collection instancié comme type de conversation. Exécutez create_ or_ update () à partir de l&#39;objet Collection pour terminer le processus de création.

| Variable | Type | Description |
|--- |--- |--- |
| titre | Chaîne | Titre de la collection. |
| Articleid | Chaîne | Identifiant d&#39;article unique choisi pour identifier une collection sur votre site. |
| url | Chaîne | URL absolue canonique pour cette collection. |

## Exemple Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Exemple nodejs {#section_xkd_gds_rz}

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
