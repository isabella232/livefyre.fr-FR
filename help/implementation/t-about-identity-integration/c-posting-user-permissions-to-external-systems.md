---
description: Livefyre utilise une interface PUSH pour envoyer des informations système externes sur les modifications apportées aux autorisations utilisateur.
title: Validation des autorisations d’utilisateur sur des systèmes externes (facultatif)
exl-id: 335c9ff2-e392-4310-aad2-7890c8e82eba
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 4%

---

# Validation des autorisations d’utilisateur sur des systèmes externes (facultatif){#posting-user-permissions-to-external-systems-optional}

Livefyre utilise une interface PUSH pour envoyer des informations système externes sur les modifications apportées aux autorisations utilisateur.

## Types d&#39;utilisateurs dans Livefyre Studio

| Type d’utilisateur | Description |
|--- |--- |
| propriétaire | Cet utilisateur est propriétaire et peut à la fois modérer le contenu et affecter de nouveaux modérateurs. |
| admin | Cet utilisateur est un modérateur et peut modérer le contenu. |
| membre | Cet utilisateur est placé sur la liste autorisée. Le contenu publié ne passe pas par des filtres de spam ou de profanation et ne nécessite pas d’approbation dans les flux prémodérés. |
| Aucune | Cet utilisateur est un utilisateur standard et ne dispose pas d’autorisations spéciales. |
| décapité | Cet utilisateur n&#39;a pas le droit de participer à une quelconque conversation. |

Pour publier des autorisations d’utilisateur sur des systèmes externes, vous devez enregistrer une URL qui reçoit des données d’autorisation en tant que requêtes POST.

Par exemple :

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Paramètre | Description |
|--- |--- |
| networkName | Votre Livefyre a fourni un nom de réseau. |
| token | Jeton système valide. |
| url | URL d’enregistrement. |

L’URL enregistrée doit accepter les POST avec les données suivantes comme type de contenu : application/x-www-form-urlencoded.

| Paramètre | Description |
|--- |--- |
| jid | JID de l’utilisateur dont l’affiliation a été modifiée. Un JID est une chaîne de la forme `user_id@network`. |
| affiliation | Nom des autorisations attribuées, qui doit être l’une des suivantes :  `{admin | member | none | outcast | owner}` |

Pour plus d&#39;informations sur la mise à jour des paramètres d&#39;affiliation utilisateur, consultez le [Guide de référence de l&#39;API d&#39;affiliation utilisateur Ajouté](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
