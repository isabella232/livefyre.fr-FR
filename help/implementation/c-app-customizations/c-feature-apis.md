---
description: Automatisation du processus à l'aide des API de fonctionnalités
seo-description: Automatisation du processus à l'aide des API de fonctionnalités
seo-title: API de fonctionnalités
title: API de fonctionnalités
uuid: eac 3 a 156-0 b 60-4 ffa -8 b 6 f-e 451 eb 03 da 77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# API de fonctionnalités{#feature-apis}

Automatisation du processus à l&#39;aide des API de fonctionnalités

Utilisez les API Fonctionnalités pour automatiser le processus de sélection du contenu. Par exemple, lors de la création d&#39;un blog ou d&#39;une application de commentaire en direct, faites correspondre tout le contenu publié par un modérateur sélectionné pour conduire la conversation et établir une cohérence dans le flux.

Livefyre propose à la fois des API de fonctionnalité et d&#39;annulation de fonctionnalités.

## Fonction {#section_jpw_nqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

Saisissez le jeton d&#39;utilisateur pour le modérateur sélectionné.

**Données de publication**

```
{value: <number>} 
```

La valeur sera utilisée pour trier le contenu incitatif, la plus grande au plus petit (10 apparaîtra avant 1 dans la liste du contenu incitatif). Cette valeur correspond par défaut à **la** date considérée. Les commentaires incitatifs sont donc généralement triés le plus récent à la plus ancienne.

**Exemple de réponse**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Le champ de données n&#39;est pas encore utilisé.

## Unfeature {#section_knh_mqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Saisissez le jeton d&#39;utilisateur pour le modérateur sélectionné.

**Exemple de réponse**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Le champ de données n&#39;est pas encore utilisé.

