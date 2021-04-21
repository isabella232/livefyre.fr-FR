---
description: Automatisation du processus à l’aide des API de fonctions
title: API de fonctionnalités
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# API de fonctionnalités{#feature-apis}

Automatisation du processus à l’aide des API de fonctions

Utilisez les API de fonctionnalités pour automatiser le processus selon lequel le contenu est proposé. Par exemple, lors de la création d’un blog en direct ou d’une application de commentaires, incluez tout le contenu publié par un modérateur sélectionné pour diriger la conversation et assurer la cohérence au sein du flux.

Offres Livefyre à la fois des API Fonctionnalités et Unfeature.

## Fonctionnalité {#section_jpw_nqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; Entrez le jeton utilisateur pour le modérateur sélectionné.

**Données de publication**

```
{value: <number>} 
```

La valeur sera utilisée pour trier le contenu incitatif, de la plus grande à la plus petite (10 apparaîtra avant 1 dans la liste de contenu incitatif). Par défaut, cette valeur est **now** dans l’époque, de sorte que les commentaires présentés sont généralement triés du plus récent au plus ancien.

**Exemple de réponse**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Le champ de données n&#39;est pas encore utilisé.

## Désactiver {#section_knh_mqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Saisissez le jeton utilisateur pour le modérateur sélectionné.

**Exemple de réponse**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Le champ de données n&#39;est pas encore utilisé.
