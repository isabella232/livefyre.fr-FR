---
description: Découvrez comment surveiller et stocker le contenu généré par l'utilisateur dans le système Livefyre.
seo-description: Découvrez comment surveiller et stocker le contenu généré par l'utilisateur dans le système Livefyre.
seo-title: Flux d'activités
solution: Experience Manager
title: Flux d'activités
uuid: f 40 deec 1-58 ab -41 c 9-aac 4-d 2 d 8 c 9192 bb 9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Flux d&#39;activités {#activity-stream}

Découvrez comment surveiller et stocker le contenu généré par l&#39;utilisateur dans le système Livefyre.

Utilisez l&#39;API de diffusion en continu d&#39;activité pour utiliser les données générées par l&#39;utilisateur dans le système Livefyre de votre réseau ou site. Par exemple : utilisez les données de cette API pour mettre à jour vos indices de recherche en fonction des évaluations ou pour gérer les badges d&#39;utilisateurs dans un système tiers basé sur leur activité.

API de diffusion en continu d&#39;activité :

Pour obtenir la liste complète des points de fin disponibles, consultez la section Référence de l&#39;API Livefyre.

## Ressources {#section_aql_n4l_b1b}

Il existe deux points de fin : un pour l&#39;environnement d&#39;évaluation et un pour production.

### Évaluation

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Production

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Paramètres

* **ressource :***string* A URN de l&#39;objet pour lequel vous demandez des données d&#39;activité.

* **depuis :***integer* Entier 64 bits représentant l&#39;ID du dernier événement reçu. Indiquez « 0 » si vous n&#39;avez pas de données antérieures.

## Chaînes URN {#section_skl_q4l_b1b}

Exemples :

* **urn : livefyre :**`example.fyre.co` Le flux d&#39;activité pour `example.fyre.co`.
* **urn : livefyre :**`example.fyre.co:site=54321` Flux d&#39;activités du site 54321 sous le `example.fyre.co` réseau.

## Stratégies jeton {#section_nwh_c5j_11b}

L&#39;API de diffusion en continu d&#39;activité utilise un jeton porteur oauth pour l&#39;authentification. Les jetons du porteur font partie de la spécification oauth 2.0 et décrit officiellement [ici](https://tools.ietf.org/html/rfc6750#section-1.2).

Un jeton contient plusieurs éléments :

* Qui a créé le jeton.
* Qui a reçu un jeton.
* Heure à laquelle elle n&#39;est plus valide.
* Ce que nous utilisons.
* Liste des autorisations qui ont été accordées.

### Etapes

Les étapes de création d&#39;un jeton porteur oauth incluent :

* Créez un mappage/dictionnaire contenant l&#39;émetteur, l&#39;audience, le sujet, l&#39;expiration et la portée.
* Utilisez la bibliothèque JWT, avec votre secret, pour coder un jeton JWT.
* Ajouter une authentification : Porteur de votre requête HTTP.

L&#39;exemple de code ci-dessous illustre les étapes ci-dessus de Python :

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

Où les clés de jeton du porteur sont définies comme suit :

* **iss** *(émetteur)* Entité avec l&#39;autorisation de générer des jetons. Il peut s&#39;agir de Livefyre, d&#39;un site ou d&#39;un réseau. (Pour qu&#39;une note soit en retard à l&#39;école, c&#39;est votre parent.)
* **aud** *(Audience)* Personne pour laquelle ce jeton a été généré. Si vous créez le jeton vous-même, il s&#39;agit du site ou du réseau.
* **sub** *(Objet)* Objet pour lequel les autorisations doivent être accordées. Si vous utilisez, par exemple, une collection, l&#39;objet doit être l&#39;identifiant de la collection. (Dans la note de l&#39;exemple scolaire, c&#39;est vous.)
* **exp** *(expiration)* Un point auquel le jeton n&#39;est plus valide.
* **scope** *(Scope)* Il s&#39;agit d&#39;une liste des autorisations accordées à l&#39;objet. « Tardivement pour l&#39;école » est un exemple. Le nom d&#39;une API est un autre exemple.

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

Réponse avec de nouvelles données depuis la dernière requête :

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

## Remarques {#section_hj3_crj_11b}

* Un appel réussi à l&#39;API retournera un code d&#39;état HTTP 200. Tous les autres codes d&#39;état doivent être considérés comme des erreurs.
* Si non nul, utilisez la valeur d&#39; `data.meta.cursor.next` en tant `since` que paramètre de la requête suivante.
* Si la valeur d&#39; `data.meta.cursor.next` est null, cela signifie qu&#39;il n&#39;y a aucune nouvelle donnée à consommer. Vous devez rédemander ultérieurement avec la même `since` valeur pour savoir si de nouvelles données sont arrivées.
* En pratique, vous devez demander immédiatement davantage de données si `data.meta.cursor.next` la valeur n&#39;est pas nulle.
* Environ deux heures de données récentes sont disponibles via cette API en production.
* Vous devez configurer vos processus pour interroger fréquemment ce point de fin sur cronjob afin d&#39;éviter les données manquantes. Un intervalle de cinq minutes doit être parfaitement adapté pour la plupart des implémentations.
