---
description: Informe Livefyre d’extraire les informations utilisateur d’une URL de synchronisation utilisateur précédemment définie. Renvoie une valeur de type Boolean.
title: syncUser Network, méthode
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# syncUser Network Method{#syncuser-network-method}

Informe Livefyre d’extraire les informations utilisateur d’une URL de synchronisation utilisateur précédemment définie. Renvoie une valeur de type Boolean.

| Variable | Type | Description |
|--- |--- |--- |
| l’userID | Chaîne | ID utilisateur à synchroniser avec Livefyre. Vous devez définir une URL de synchronisation utilisateur avec Livefyre avant d’appeler cette méthode. |

## Exemple Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Exemple de sortie :

```
true
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Exemple de sortie :

```
true
```

## Exemple PHP {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Exemple de sortie :

```
true
```

## Exemple Python {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Exemple de sortie :

```
True
```

## Exemple Ruby {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Exemple de sortie :

```
True
```
