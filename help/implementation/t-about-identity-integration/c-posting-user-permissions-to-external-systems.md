---
description: Livefyre utilise une interface PUSH pour envoyer des informations système externes sur les modifications apportées aux autorisations utilisateur.
seo-description: Livefyre utilise une interface PUSH pour envoyer des informations système externes sur les modifications apportées aux autorisations utilisateur.
seo-title: Publication des autorisations utilisateur sur des systèmes externes (facultatif)
solution: Experience Manager
title: Publication des autorisations utilisateur sur des systèmes externes (facultatif)
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Publication des autorisations utilisateur sur des systèmes externes (facultatif){#posting-user-permissions-to-external-systems-optional}

Livefyre utilise une interface PUSH pour envoyer des informations système externes sur les modifications apportées aux autorisations utilisateur.

## Types d'utilisateurs dans Livefyre Studio

| Type d’utilisateur | Description |
|--- |--- |
| propriétaire | Cet utilisateur est propriétaire et peut modérer le contenu et affecter de nouveaux modérateurs. |
| admin | Cet utilisateur est un modérateur et peut modérer le contenu. |
| membre | Cet utilisateur est autorisé. Le contenu publié ne passe pas par les filtres de spam ou de profanation et ne nécessite pas d’approbation dans les flux prémodérés. |
| Aucune | Cet utilisateur est un utilisateur standard et ne dispose d’aucune autorisation spéciale. |
| outcast | Cet utilisateur n'a pas le droit de participer aux conversations. |

Pour publier des autorisations d’utilisateur sur des systèmes externes, vous devez enregistrer une URL qui reçoit des données d’autorisation en tant que requêtes POST.

Par exemple :

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Paramètre | Description |
|--- |--- |
| networkName | Votre Livefyre a fourni un nom réseau. |
| token | Jeton système valide. |
| url | URL à enregistrer. |

L’URL enregistrée doit accepter les POST avec les données suivantes comme type de contenu : application/x-www-form-urlencoded.

| Paramètre | Description |
|--- |--- |
| jid | JID de l’utilisateur dont l’affiliation a été modifiée. Un JID est une chaîne du formulaire `user_id@network`. |
| affiliation | Nom des autorisations attribuées, qui doit être l’une des suivantes :  `{admin | member | none | outcast | owner}` |

Pour plus d’informations sur la mise à jour des paramètres d’affiliation utilisateur, voir le Guide de référence [sur l’API](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)Ajouter une affiliation utilisateur.
