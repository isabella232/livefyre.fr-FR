---
description: Créez un jeton unique sur votre serveur qui identifie chaque collection que vous créez.
seo-description: Créez un jeton unique sur votre serveur qui identifie chaque collection que vous créez.
seo-title: CollectionMeta Token
solution: Experience Manager
title: CollectionMeta Token
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: 6978f0f36b5698c9c599c1828edea67703423397
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 2%

---


# CollectionMeta Token{#collectionmeta-token}

Créez un jeton unique sur votre serveur qui identifie chaque collection que vous créez.

Livefyre attribue un identifiant unique à chaque collection que vous créez. Livefyre attribue un titre, une URL et d’autres paramètres, notamment :

## Paramètres de collectionMeta Token

| Paramètre | Type | Description |
|--- |--- |--- |
| networkName | Chaîne (facultatif) | Nom du réseau Livefyre (disponible à partir de [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials] ). Cette option est facultative lorsque vous utilisez la bibliothèque pour créer un jeton collectionMeta. |
| networkKey | Chaîne (facultatif) | Clé secrète du réseau spécifique (disponible depuis Studio > Paramètres > Paramètres d’intégration > Informations d’identification). Cette option est facultative lorsque vous utilisez la bibliothèque pour créer un jeton collectionMeta. |
| siteId | Chaîne (facultatif) | ID du site (disponible auprès de [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Facultatif lors de l’utilisation de la bibliothèque pour créer un jeton collectionMeta. |
| siteKey | Chaîne (facultatif) | Clé secrète du site (disponible sur [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). |
| articleId | Chaîne (facultatif) | Identifiant unique de la collection. |
| title | Chaîne (facultatif) | Titre que vous souhaitez appliquer à la collection. En général, cela correspond au titre de la page qui affiche l’application. <br>Par exemple : &quot;L&#39;intégration est tellement amusante !&quot; <br>Remarque :  La longueur maximale des caractères pour le titre est de 255 caractères. Le champ de titre ne prend pas en charge les entités HTML. Veuillez coder des caractères spéciaux au format UTF-8. |
| url | Chaîne (facultatif) | URL absolue canonique que vous souhaitez joindre à cette collection. Cette URL sera utilisée pour générer des liens vers l’application à partir du contenu partagé sur Facebook et Twitter, des notifications par courrier électronique et Livefyre Studio. <br>Remarque :  Si le test est effectué localement, utilisez un domaine d’URL de base valide (par exemple : valide : `https://customer.com`; non valide : `https://localhost:5995`). |
| balises | Chaîne (facultatif) | Liste de mots-clés ou d’expressions séparés par des virgules. Recherchez Collections par balises à l’aide de Studio.  </br>Remarque :  Les balises ne peuvent pas contenir d’espaces. Utilisez des traits de soulignement si vous souhaitez qu’un espace s’affiche dans l’interface utilisateur. |
| extensions | JSON (facultatif) | Ensemble de paramètres au format JSON à transmettre à la collection. |

## Java {#section_orz_m4n_sz}

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

## NodeJS {#section_kpk_44n_sz}

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

>[!NOTE]
>
>Livefyre reçoit le jeton collectionMeta que vous créez et détermine son unicité en combinant siteId (Livefyre fourni) et articleId (client spécifié).
