---
description: Découvrez comment surveiller et stocker le contenu généré par l’utilisateur circulant sur le système Livefyre.
seo-description: Découvrez comment surveiller et stocker le contenu généré par l’utilisateur circulant sur le système Livefyre.
seo-title: Flux d’Activité
solution: Experience Manager
title: Flux d’Activité
uuid: f40deec1-58ab-41c9-aac4-d2d8c9192bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# Flux d&#39;Activité {#activity-stream}

Découvrez comment surveiller et stocker le contenu généré par l’utilisateur circulant sur le système Livefyre.

Utilisez l’API de diffusion en continu d’Activités pour utiliser les données générées par l’utilisateur qui transitent par le système Livefyre sur votre réseau ou votre site. Par exemple : utilisez les données de cette API pour mettre à jour vos indices de recherche en fonction des évaluations ou pour gérer les badges des utilisateurs dans un système tiers en fonction de leur activité.

API de flux d&#39;Activité :

Pour une liste complète des points de terminaison disponibles, consultez la section Référence API Livefyre.

## Ressources {#section_aql_n4l_b1b}

Il existe deux points de terminaison, un pour l’environnement d’évaluation et un autre pour la production.

### Evaluation

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Production

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Paramètres

* **resource:** ** stringURL de l&#39;objet pour lequel vous demandez des données d&#39;activité.

* **since:** ** integerEntier 64 bits représentant l’identifiant du dernier événement reçu. Indiquez &quot;0&quot; si vous n’avez aucune donnée antérieure.

## Chaînes URN {#section_skl_q4l_b1b}

Exemples :

* **urn:livefyre:** `example.fyre.co` Flux d’activité pour  `example.fyre.co`.
* **urn:livefyre:** `example.fyre.co:site=54321` Flux d’activité pour le site 54321 sous le  `example.fyre.co` réseau.

## Stratégies de jeton {#section_nwh_c5j_11b}

L’API de flux d’Activité utilise un jeton de garde OAuth pour l’authentification. Les jetons de garde font partie de la spécification OAuth 2.0 et sont officiellement décrits [ici](https://tools.ietf.org/html/rfc6750#section-1.2).

Un jeton contient plusieurs éléments :

* Qui a créé le jeton.
* Qui a reçu un jeton.
* Heure à laquelle il n’est plus valide.
* Ce sur quoi nous travaillons.
* Liste des autorisations qui ont été accordées.

### Étapes

Voici les étapes de création d&#39;un jeton OAuth Bearer :

* Créez un mappage/dictionnaire contenant l’émetteur, l’audience, l’objet, l’expiration et la portée.
* Utilisez la bibliothèque JWT, avec votre secret, pour coder un jeton JWT.
* Ajouter &quot;Authentication: Bearer&quot; à votre requête HTTP.

L&#39;exemple de code ci-dessous illustre les étapes ci-dessus en Python :

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

Lorsque les clés de jeton porteur sont définies comme suit :

* **iss** *(Issuer)* Entité habilitée à générer des jetons. Il peut s&#39;agir de Livefyre, d&#39;un site ou d&#39;un réseau. (Pour qu’une note soit en retard à l’école, c’est votre parent.)
* **aud** *(Audience)* Personne pour laquelle ce jeton a été généré. Si vous créez vous-même le jeton, il s’agit du site ou du réseau.
* **sub** *(Objet)* Objet pour lequel des autorisations doivent être accordées. Par exemple, si vous opérez sur une collection, l’objet doit être l’identifiant de la collection. (Dans la note de l’exemple de l’école, c’est vous.)
* **exp** *(Expiration)* Moment auquel le jeton n’est plus valide.
* **scope** *(Scope)* Il s&#39;agit d&#39;une liste des autorisations accordées sur le sujet. &quot;Late for school&quot; en est un exemple. Le nom d&#39;une API est un autre exemple.

## Exemple {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## Réponse {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

Réponse contenant de nouvelles données depuis la dernière requête :

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Notes {#section_hj3_crj_11b}

* Un appel réussi à l&#39;API retournera un code d&#39;état HTTP 200. Tous les autres codes d’état doivent être considérés comme des erreurs.
* Si la valeur n’est pas nulle, utilisez la valeur de `data.meta.cursor.next` comme paramètre `since` de votre requête suivante.
* Si la valeur de `data.meta.cursor.next` est nulle, cela signifie qu’il n’y a pas de nouvelles données à consommer. Vous devez demander de nouveau plus tard avec la même valeur `since` pour savoir si de nouvelles données sont arrivées.
* En règle générale, vous devez immédiatement demander plus de données si la valeur `data.meta.cursor.next` n’est pas nulle.
* Cette API est disponible en production pour environ deux heures de données récentes.
* Configurez vos processus pour qu’ils interrogent fréquemment ce point de terminaison sur cronjob afin d’éviter les données manquantes. Un intervalle de cinq minutes doit être parfaitement adapté à la plupart des mises en oeuvre.
