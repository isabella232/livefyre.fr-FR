---
description: Livefyre utilise une interface PUSH pour envoyer une information système externe sur les modifications apportées aux autorisations utilisateur.
seo-description: Livefyre utilise une interface PUSH pour envoyer une information système externe sur les modifications apportées aux autorisations utilisateur.
seo-title: Publication des permissions utilisateur sur systèmes externes (facultatif)
solution: Experience Manager
title: Publication des permissions utilisateur sur systèmes externes (facultatif)
uuid: 9 c 18 b 20 d -3 b 93-4666-b 7 de -1 ec 60318 cf 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Publication des permissions utilisateur sur systèmes externes (facultatif){#posting-user-permissions-to-external-systems-optional}

Livefyre utilise une interface PUSH pour envoyer une information système externe sur les modifications apportées aux autorisations utilisateur.

## Types d&#39;utilisateurs dans Livefyre Studio

| Type d&#39;utilisateur | Description |
|--- |--- |
| propriétaire | Cet utilisateur est un propriétaire et peut modérer le contenu et affecter de nouveaux modérateurs. |
| admin | Cet utilisateur est un modérateur et peut modérer le contenu. |
| membre | Cet utilisateur est autorisé. Le contenu publié ne transfère pas les messages indésirables ou de profilité et ne nécessite pas d&#39;approbation dans les flux pré-modérés. |
| none | Cet utilisateur est un utilisateur standard et n&#39;a pas d&#39;autorisations spéciales. |
| outcast | Cet utilisateur a été interdit de participer à une conversation. |

Pour publier des permissions utilisateur sur des systèmes externes, vous devez enregistrer une URL qui reçoit des données d&#39;autorisation sous forme de requêtes POST.

Par exemple :

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Paramètre | Description |
|--- |--- |
| Networkname | Votre nom de réseau fourni par Livefyre. |
| jeton | Jeton système valide. |
| url | URL à enregistrer. |

L&#39;URL enregistrée doit accepter les POST avec les données suivantes comme type de contenu : application/x-www-form-urlencoded.

| Paramètre | Description |
|--- |--- |
| jid | JID de l&#39;utilisateur dont l&#39;affiliation est modifiée. Un JID est une chaîne du formulaire `user_id@network`. |
| affiliation | Nom des autorisations attribuées, qui doivent être l&#39;une des suivantes : `{admin | member | none | outcast | owner}` |

Pour plus d&#39;informations sur la mise à jour des paramètres d&#39;affiliation utilisateur, voir [la référence de l&#39;API d&#39;association d&#39;utilisateur](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
