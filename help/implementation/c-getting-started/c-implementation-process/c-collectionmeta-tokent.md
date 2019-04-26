---
description: Créez un jeton unique sur votre serveur qui identifie chaque collection
  que vous créez.
seo-description: Créez un jeton unique sur votre serveur qui identifie chaque collection
  que vous créez.
seo-title: Collectionmeta Token
solution: Experience Manager
title: Collectionmeta Token
uuid: d 5 db 0 b 0 f -2807-4392-874 a -94 ac 3 c 1 e 7550
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Collectionmeta Token{#collectionmeta-token}

Créez un jeton unique sur votre serveur qui identifie chaque collection que vous créez.

Livefyre attribue un identifiant unique à chaque collection que vous créez. Livefyre attribue un titre, une URL et d'autres paramètres, notamment :

## Paramètres de jeton collectionmeta

| Paramètre | Type | Description |
|--- |--- |--- |
| Networkname | Chaîne (facultatif) | Le nom du réseau Livefyre (disponible depuis {! UICONTROL Studio > Paramètres > Paramètres d'intégration > Informations d'identification]). Cela est facultatif lorsque vous utilisez la bibliothèque pour créer un jeton collectionmeta. |
| Networkkey | Chaîne (facultatif) | Clé secrète du réseau spécifique (disponible depuis Studio > Paramètres > Paramètres d'intégration > Informations d'identification). Cela est facultatif lorsque vous utilisez la bibliothèque pour créer un jeton collectionmeta. |
| Siteid | Chaîne (facultatif) | ID du site (accessible depuis [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Facultatif lors de l'utilisation de la bibliothèque pour créer un jeton collectionmeta. |
| Sitekey | Chaîne (facultatif) | La clé secrète du site (disponible depuis {! UICONTROL Studio > Paramètres > Paramètres d'intégration > Informations d'identification]). |
| Articleid | Chaîne (facultatif) | Identifiant unique de la collection. |
| titre | Chaîne (facultatif) | Titre que vous souhaitez appliquer à la collection. Habituellement, cela correspond au titre de la page qui affiche l'application. <br>Par exemple : « L'intégration est tellement fun !  » » <br>Remarque : La longueur maximale du titre est de 255 caractères. Le champ title ne prend pas en charge les entités HTML. Veuillez coder des caractères spéciaux à l'aide de UTF -8. |
| url | Chaîne (facultatif) | URL absolue canonique que vous souhaitez joindre à cette collection. Cette URL est utilisée pour générer des liens renvoyant à l'application depuis le contenu partagé sur Facebook et Twitter, les notifications par courrier électronique et Livefyre Studio. <br>Remarque : Si vous testez localement, utilisez un domaine d'URL de base valide (par exemple : valide : `https://customer.com`; non valide : `https://localhost:5995`). |
| balises | Chaîne (facultatif) | Liste de mots-clés ou d'expressions séparés par des virgules. Rechercher des collections par balises à l'aide de Studio. </br>Remarque : Les balises ne peuvent pas contenir d'espaces. Utilisez des traits de soulignement si vous souhaitez qu'un espace apparaisse dans l'interface utilisateur. |
| extensions | JSON (facultatif) | Ensemble de paramètres au format JSON à transmettre à la collection. |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## Nodejs {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE] {importance = « high »}
>
>Livefyre reçoit le jeton collectionmeta que vous créez et détermine l'unicité en combinant siteid (Livefyre fourni) et articleid (client spécifié).

