---
description: Comptez le nombre d’éléments sociaux traités.
seo-description: Comptez le nombre d’éléments sociaux traités.
seo-title: Compteur social
solution: Experience Manager
title: Compteur social
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Compteur social{#social-counter}

Comptez le nombre d’éléments sociaux traités. Pour obtenir la liste complète des points de fin disponibles, consultez la section Référence [de l’](https://api.livefyre.com/docs) API Livefyre.

L’API Compteur de réseau social renvoie le nombre de règles de traitement correspondantes dans une collection donnée pour des intervalles sur une période donnée.

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

* **** networkName :Votre Livefyre a fourni un nom réseau. Par exemple : Des *labos* `labs.fyre.co`.
* **** query : Hachage codé en base 64 sécurisé par l’URL de tous les sites, ID d’article, tuples de type règle pour lesquels les informations de décompte doivent être récupérées (pré-codées)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La requête est limitée à 10 sites, ID d’article, tuples de type règle. (L’exemple précédent contient 3 tuples.)

* **from**`(optional)` spécifie la période relative ou absolue à suivre pour le graphique ; from spécifie le début et prend par défaut la valeur 24 heures auparavant, si omis.
* **jusqu** ’à ce que `(optional)` spécifie la période relative ou absolue à représenter par le graphique ; until spécifie le début et l’heure actuelle (maintenant) par défaut, si omis.

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

## Heure absolue {#section_xqr_jgc_11b}

FORMAT : HH:MM_YYYMJJ

| Abréviation | Signification |
|---|---|
| HH | Heures (au format 24h/24) |
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

Pour obtenir des comptes à la dernière minute pour l’ID du site `123456` et de l’article `some-article-id` et le type de règle `2`, par exemple : `123456:some-article-id;2:`

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
