---
description: Automatisation du processus à l’aide des API de fonctionnalités
seo-description: Automatisation du processus à l’aide des API de fonctionnalités
seo-title: API de fonctionnalités
title: API de fonctionnalités
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# API de fonctionnalités{#feature-apis}

Automatisation du processus à l’aide des API de fonctionnalités

Utilisez les API de fonctionnalités pour automatiser le processus selon lequel le contenu est proposé. Par exemple, lors de la création d’un blog en direct ou d’une application de commentaires, mettez en vedette tout le contenu publié par un modérateur sélectionné afin de diriger la conversation et d’assurer la cohérence au sein du flux.

Livefyre propose des API Fonctionnalités et Unfeature.

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

La valeur sera utilisée pour trier le contenu incitatif, du plus grand au plus petit (10 apparaîtra avant 1 dans la liste de contenu incitatif). Par défaut, cette valeur est **maintenant** dans l’époque. Les commentaires présentés sont donc généralement triés du plus récent au plus ancien.

**Exemple de réponse**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Le champ de données n’est pas encore utilisé.

## Annuler {#section_knh_mqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Entrez le jeton utilisateur pour le modérateur sélectionné.

**Exemple de réponse**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Le champ de données n’est pas encore utilisé.

