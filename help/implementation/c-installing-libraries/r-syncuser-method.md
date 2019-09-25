---
description: Informe Livefyre d’extraire les informations utilisateur d’une URL de synchronisation utilisateur précédemment définie. Renvoie une valeur de type Boolean.
seo-description: Informe Livefyre d’extraire les informations utilisateur d’une URL de synchronisation utilisateur précédemment définie. Renvoie une valeur de type Boolean.
seo-title: syncUser Network, méthode
solution: Experience Manager
title: syncUser Network, méthode
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# syncUser Network, méthode{#syncuser-network-method}

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
