---
description: Comptez le nombre d'éléments sociaux organisés.
seo-description: Comptez le nombre d'éléments sociaux organisés.
seo-title: Compteur social
solution: Experience Manager
title: Compteur social
uuid: fa 9 aa 1 a 8-6 a 04-4 bc 1-9 bfe-e 42 c 1250 fd 48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Compteur social{#social-counter}

Comptez le nombre d'éléments sociaux organisés. Pour obtenir la liste complète des points de fin disponibles, consultez la section [Référence](https://api.livefyre.com/docs) de l'API Livefyre.

L'API de compteur Social renvoie le nombre de règles de traitement correspondantes dans une collection donnée pour les intervalles sur une période donnée.

>[!NOTE]
>
>Cette API est disponible uniquement pour les hashtags Twitter.

API de compteur social :

* Ressource
* Types de règle
* Réponse

## Ressource {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **Networkname :** Votre nom de réseau fourni par Livefyre. Par exemple : *labs* in `labs.fyre.co`.
* **query :** Hachage encodé en base 64 de tout le site, ID d'article, tuple de type règle pour lequel les informations du nombre doivent être récupérées (pré-codées)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La requête est limitée à 10 site, ID d'article, tuples de type règle. (L'exemple précédent contient 3 tuples.)

* **from** `(optional)` specifies the relative or absolute time period to graph ; from specifies the start and defaults to 24 hours if omitted.
* **jusqu'à** `(optional)` ce que la période absolue ou absolue soit définie sur graphique ; jusqu'à ce que le début et la valeur par défaut correspondent à l'heure actuelle (maintenant), s'ils sont omis.

### Heure relative

| Abréviation | Unité |
|---|---|
| s | Secondes |
| min | Minutes |
| h | Heures |
| d | Jours |
| w | Semaines |
| mon | 30 jours (mois) |
| y | 365 jours (année) |

Exemple :

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Heure absolue {#section_xqr_jgc_11b}

FORMAT : HH : MM_ AAAAMMJJ

| Abréviation | Signification |
|---|---|
| HH | Heures (format d'horloge 24 h) |
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

Pour obtenir le décompte sur la dernière minute pour l'ID de site `123456` et d'article `some-article-id` et le type de règle `2`, par exemple : `123456:some-article-id;2:`

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
