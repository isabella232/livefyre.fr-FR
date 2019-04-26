---
description: Ajoutez Livefyre à vos applications mobiles natives.
seo-description: Ajoutez Livefyre à vos applications mobiles natives.
seo-title: SDK mobiles
solution: Experience Manager
title: SDK mobiles
uuid: 84 c 7 ca 1 c -3401-492 a-bfa 5-62 b 996947 a 44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK mobiles{#mobile-sdks}

Ajoutez Livefyre à vos applications mobiles natives.

Plusieurs options sont disponibles pour les implémentations mobiles, selon l'étendue de personnalisation que vous prévoyez d'effectuer :

* Applications Web mobiles
* SDK Livefyre Android ou ios
* API HTTP

## Applications Web mobiles {#section_t2k_vpb_11b}

Les clients qui ouvrent une page Web sur un périphérique mobile obtiennent automatiquement un flux de contenu Livefyre optimisé pour les périphériques mobiles, y compris la mise en forme pour ajuster la taille d'écran réduite et les modifications pour gérer les événements tactiles.

>[!NOTE]
>
>Lorsque vous utilisez une application Livefyre dans un webview Android, le paramètre [Websettings. setdomstorageenabled de Android](https://developer.android.com/reference/android/webkit/WebSettings.html) doit être défini sur true. Si localstorage n'est pas activé, Livefyre ne pourra pas enregistrer un utilisateur dans l'application Livefyre.

Pour optimiser le mobile, Livefyre limite les fonctionnalités Commentaires, Blog en direct et Application de Chat à inclure :

* Publication
* Modifier
* Indicateur
* Aimer
* Répondre
* Nombre d'écouteurs
* Nombre de commentaires
* Modération en attente en attente
* Hovercards
* Principaux commentaires
* Threads logiciels
* Commentaires sur la file d'attente

Dans les applications Web mobiles, cliquez sur le nom d'un auteur pour ouvrir les informations sur la carte dans une nouvelle page.

## SDK Livefyre Android ou SDK ios {#section_zdz_spb_11b}

Livefyre fournit également deux kits SDK mobiles : un SDK ios et un SDK Android. Ces SDK sont des wrappers autour de nos endpoints de terminaison HTTP, conçus pour fournir une méthode plus facile d'envoi et de réception de données. Aucune interface n'est fournie avec ces kits SDK, ce qui offre une plus grande flexibilité quant à l'affichage et à l'utilisation du contenu dans votre application mobile.

Les SDK Android et ios prennent en charge les fonctionnalités suivantes pour les commentaires, le blog en direct et la messagerie instantanée :

| Fonctionnalités ios : | Fonctionnalités Android : |
|--- |--- |
| <ul><li> Publication </li><li>Modifier </li><li>Indicateur </li><li>Aimer </li><li>Répondre </li><li>Threads logiciels</li></ul> | <ul><li>Publication </li><li>Modifier </li><li>Aimer </li><li>Répondre </li><li>Threads logiciels</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Les API HTTP sont le groupe de points de fin qui vous permettent de créer des conversations et du contenu sur la plate-forme Livefyre. Il alimente également tous les flux de données Livefyre. Bien que cette solution nécessite davantage de temps de développement par rapport à votre équipe d'ingénieurs, elle offre une plus grande flexibilité lors de l'utilisation de la suite de produits Livefyre et permet l'intégration native des applications mobiles.

>[!IMPORTANT]
>
>**Ne** créez pas de jetons d'authentification utilisateur dans le client mobile, car cela implique d'exposer votre clé réseau secrète Livefyre au sein d'une application non sécurisée. Pour une solution plus fiable et sécurisée, reportez-vous à la section Jetons d'authentification utilisateur.

