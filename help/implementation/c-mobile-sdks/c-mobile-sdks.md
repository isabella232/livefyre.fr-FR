---
description: Ajoutez Livefyre à vos applications mobiles natives.
seo-description: Ajoutez Livefyre à vos applications mobiles natives.
seo-title: SDK mobiles
solution: Experience Manager
title: SDK mobiles
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 5%

---


# SDK mobiles{#mobile-sdks}

Ajoutez Livefyre à vos applications mobiles natives.

Plusieurs options sont disponibles pour les implémentations mobiles, selon l’étendue de la personnalisation que vous prévoyez d’effectuer :

* Applications Web mobiles
* SDK Livefyre Android ou iOS
* API HTTP

## Applications Web mobiles {#section_t2k_vpb_11b}

Les clients qui ouvrent une page Web sur un périphérique mobile obtiennent automatiquement un flux de contenu Livefyre optimisé pour les périphériques mobiles, y compris la mise en forme pour s’adapter à la taille d’écran réduite et les modifications pour gérer les événements tactiles.

>[!NOTE]
>
>Lors de l’utilisation d’une application Livefyre dans un WebView Android, le paramètre Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) doit être défini sur true. Si localStorage n’est pas activé, Livefyre ne pourra pas ouvrir de session d’utilisateur dans l’application Livefyre.

Pour optimiser l&#39;application mobile, Livefyre limite les fonctionnalités Commentaires, Blogs en direct et Application de messagerie instantanée aux fonctionnalités suivantes :

* Publication
* Modifier     
* Marquer d’un indicateur
* J’aime
* Répondre
* Nombre d’écouteurs
* Nombre de commentaires
* Modération en attente intégrée
* Hovercards
* Principaux commentaires
* Threads chauds
* Commentaires de la file d&#39;attente

Dans les applications Web mobiles, un clic sur le nom d’un auteur ouvre les informations relatives aux cartes d’identité dans une nouvelle page.

## SDK Livefyre Android ou SDK iOS {#section_zdz_spb_11b}

Livefyre fournit également deux SDK mobiles : un SDK iOS et un SDK Android. Ces SDK sont des wrappers autour de nos points de terminaison HTTP, conçus pour fournir une méthode plus facile d’envoi et de réception des données. Aucune interface n’est fournie avec ces kits SDK, ce qui permet une plus grande flexibilité quant à la manière dont le contenu est affiché et utilisé dans votre application mobile.

Les SDK Android et iOS prennent en charge les fonctionnalités suivantes pour les commentaires, les blogs en direct et les conversations :

| Fonctionnalités d’iOS : | Fonctionnalités Android : |
|--- |--- |
| <ul><li> Publication </li><li>Modifier      </li><li>Marquer d’un indicateur </li><li>J’aime </li><li>Répondre </li><li>Threads chauds</li></ul> | <ul><li>Publication </li><li>Modifier      </li><li>J’aime </li><li>Répondre </li><li>Threads chauds</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Les API HTTP sont le groupe de points de terminaison qui vous permet de créer des conversations et du contenu sur la plate-forme Livefyre. Il alimente également tous les flux Livefyre prêts à l&#39;emploi. Bien que cette solution nécessite davantage de temps de développement de la part de votre équipe d&#39;ingénieurs, elle offre une plus grande flexibilité lors de l&#39;utilisation de la suite de produits Livefyre et permet l&#39;intégration mobile native.

>[!IMPORTANT]
>
>**Ne** créez pas de jetons d’authentification utilisateur au sein du client mobile, car cela impliquerait d’exposer votre clé réseau secrète Livefyre dans une application non sécurisée. Pour une solution plus robuste et plus sécurisée, reportez-vous à la section Jetons d’authentification utilisateur.

