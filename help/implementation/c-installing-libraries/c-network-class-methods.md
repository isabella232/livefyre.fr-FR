---
description: Créez un objet réseau.
seo-description: Créez un objet réseau.
seo-title: Méthodes de classe réseau
solution: Experience Manager
title: Méthodes de classe réseau
uuid: 4130 beda-dd 09-49 ae-aafb-f 6 b 956 e 30 b 51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Méthodes de classe réseau{#network-class-methods}

Créez un objet réseau.

Lorsque vous créez un objet réseau, le reste de la page suppose que vous avez un objet réseau instancié dans votre session.

## Objet réseau

| Paramètre | Type | Description |
|---|---|---|
| *`network`* | Chaîne | Votre réseau Livefyre. Par exemple : « `labs.fyre.co` ». |
| *`networkKey`* | Chaîne | Clé secrète fournie pour le réseau. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## Nodejs {#section_nyk_dzs_kbb}

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
