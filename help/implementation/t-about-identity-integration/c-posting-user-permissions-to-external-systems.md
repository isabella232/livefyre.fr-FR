---
description: Livefyre utilise une interface PUSH pour envoyer une information système
  externe sur les modifications apportées aux autorisations utilisateur.
seo-description: Livefyre utilise une interface PUSH pour envoyer une information
  système externe sur les modifications apportées aux autorisations utilisateur.
seo-title: Publication des permissions utilisateur sur systèmes externes (facultatif)
solution: Experience Manager
title: Publication des permissions utilisateur sur systèmes externes (facultatif)
uuid: 9 c 18 b 20 d -3 b 93-4666-b 7 de -1 ec 60318 cf 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Publication des permissions utilisateur sur systèmes externes (facultatif){#posting-user-permissions-to-external-systems-optional}

Livefyre utilise une interface PUSH pour envoyer une information système externe sur les modifications apportées aux autorisations utilisateur.

## Types d'utilisateurs dans Livefyre Studio

| Type d'utilisateur | Description |
|--- |--- |
| propriétaire | Cet utilisateur est un propriétaire et peut modérer le contenu et affecter de nouveaux modérateurs. |
| admin | Cet utilisateur est un modérateur et peut modérer le contenu. |
| membre | Cet utilisateur est autorisé. Le contenu publié ne transfère pas les messages indésirables ou de profilité et ne nécessite pas d'approbation dans les flux pré-modérés. |
| none | Cet utilisateur est un utilisateur standard et n'a pas d'autorisations spéciales. |
| outcast | Cet utilisateur a été interdit de participer à une conversation. |

Pour publier des permissions utilisateur sur des systèmes externes, vous devez enregistrer une URL qui reçoit des données d'autorisation sous forme de requêtes POST.

Par exemple :

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Paramètre | Description |
|--- |--- |
| Networkname | Votre nom de réseau fourni par Livefyre. |
| jeton | Jeton système valide. |
| url | URL à enregistrer. |

L'URL enregistrée doit accepter les POST avec les données suivantes comme type de contenu : application/x-www-form-urlencoded.

| Paramètre | Description |
|--- |--- |
| jid | JID de l'utilisateur dont l'affiliation est modifiée. Un JID est une chaîne du formulaire `user_id@network`. |
| affiliation | Nom des autorisations attribuées, qui doivent être l'une des suivantes : `{admin | member | none | outcast | owner}` |

Pour plus d'informations sur la mise à jour des paramètres d'affiliation utilisateur, voir [la référence de l'API d'association d'utilisateur](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
