---
description: Comptez le nombre d’éléments sociaux traités.
title: Compteur social
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 10%

---

# Compteur social{#social-counter}

Comptez le nombre d’éléments sociaux traités. Pour obtenir la liste complète des points de terminaison disponibles, consultez la section Livefyre [Référence API](https://api.livefyre.com/docs).

L’API Compteur de réseau social renvoie des comptes pour les règles de traitement correspondantes dans une collection donnée pour des intervalles sur une période donnée.

>[!NOTE]
>
>Cette API est disponible uniquement pour les hashtags Twitter.

API de compteur de réseau social :

* Ressource
* Types de règle
* Réponse

## Ressource {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName : nom réseau fourni par** votre Livefyre. Par exemple : *labs* dans `labs.fyre.co`.
* **requête :** hachage codé url-safe base64 de l’ensemble du site, identifiant de l’article, tuples de type règle pour lesquels les informations de décompte doivent être récupérées (pré-codées)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La requête est limitée à 10 sites, ID d’article, tuples de type règle. (L’exemple précédent contient 3 tuples.)

* **** `(optional)` froment spécifie la période relative ou absolue à tracer ; from indique le début et prend par défaut la valeur il y a 24 heures, s’il est omis.
* **** `(optional)` untilindique la période relative ou absolue à tracer ; until indique le début et l’heure actuelle (maintenant), par défaut, s’il est omis.

### Temps relatif

| Abréviation | Unité |
|---|---|
| s | Secondes |
| min | Minutes |
| h | Heures |
| d | jours |
| w | semaines |
| mon | 30 jours (mois) |
| y | 365 jours (année) |

Exemple :

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Temps absolu {#section_xqr_jgc_11b}

FORMAT : HH:MM_AAAAMMJJ

| Abréviation | Signification |
|---|---|
| HH | Heures (au format d&#39;horloge de 24h) |
| MM | Minutes |
| AAAA | Année à 4 chiffres |
| MM | Mois |
| DD | Jour |

Exemple :

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Types de règle {#section_v53_xqb_11b}

| Valeur | Type |
|---|---|
| 2 | Twitter |

Exemple :

Pour obtenir des comptes à la dernière minute pour le site `123456` et l’ID d’article `some-article-id` et le type de règle `2`, par exemple : `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

Exemple de réponse :

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
