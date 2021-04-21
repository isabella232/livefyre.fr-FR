---
description: Informe Livefyre de mettre à jour l’URL de synchronisation utilisateur du réseau avec celle fournie. Renvoie une valeur de type Boolean.
title: setUserSyncUrl, méthode réseau
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# setUserSyncUrl, méthode réseau{#setusersyncurl-network-method}

Informe Livefyre de mettre à jour l’URL de synchronisation utilisateur du réseau avec celle fournie. Renvoie une valeur de type Boolean.

| Variable | Type | Description |
|--- |--- |--- |
| urlTemplate | Chaîne | URL d’enregistrement auprès de Livefyre pour la synchronisation des identifiants d’utilisateur. Nécessite que &quot;`{id}`&quot; fasse partie de la chaîne URL fournie. |

## Exemple Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exemple de sortie :

```
true
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exemple de sortie :

```
true
```

## Exemple PHP {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Exemple de sortie :

```
true
```

## Exemple Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exemple de sortie :

```
True
```

## Exemple Ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exemple de sortie :

```
True
```
