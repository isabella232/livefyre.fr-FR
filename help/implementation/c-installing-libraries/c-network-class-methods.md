---
description: Créez un objet Network.
title: Méthodes de classe réseau
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 14%

---

# Méthodes de classe réseau{#network-class-methods}

Créez un objet Network.

Une fois que vous avez créé un objet réseau, le reste de la page suppose que votre session contient un objet réseau instancié.

## Objet réseau

| Paramètre | Type | Description |
|---|---|---|
| *`network`* | Chaîne | Votre réseau Livefyre. Par exemple: “`labs.fyre.co`”. |
| *`networkKey`* | Chaîne | La clé secrète fournie par Livefyre pour le réseau. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
