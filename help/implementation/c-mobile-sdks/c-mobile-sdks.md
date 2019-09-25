---
description: Ajoutez Livefyre à vos applications mobiles natives.
seo-description: Ajoutez Livefyre à vos applications mobiles natives.
seo-title: SDK mobiles
solution: Experience Manager
title: SDK mobiles
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK mobiles{#mobile-sdks}

Ajoutez Livefyre à vos applications mobiles natives.

Plusieurs options sont disponibles pour les implémentations mobiles, selon l’étendue de la personnalisation que vous prévoyez d’effectuer :

* Applications Web mobiles
* SDK Livefyre Android ou iOS
* API HTTP

## Applications Web mobiles {#section_t2k_vpb_11b}

Les clients qui ouvrent une page Web sur un périphérique mobile obtiennent automatiquement un flux de contenu Livefyre optimisé pour les périphériques mobiles, y compris la mise en forme pour s’adapter à la taille d’écran réduite et aux modifications pour gérer les événements tactiles.

>[!NOTE]
>
>Lors de l’utilisation d’une application Livefyre dans une vue WebView Android, le paramètre Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) doit être défini sur true. Si localStorage n’est pas activé, Livefyre ne pourra pas connecter un utilisateur à l’application Livefyre.

Pour optimiser les fonctionnalités mobiles, Livefyre limite les commentaires, les blogs en direct et les applications de messagerie instantanée aux fonctionnalités suivantes :

* Publication
* Modifier     
* Marquer d’un indicateur
* J’aime
* Répondre
* Nombre d’écouteurs
* Nombre de commentaires
* Modération en attente en ligne
* Hovercards
* Principaux commentaires
* Threads chauds
* Commentaires de file d’attente

Dans les applications Web mobiles, le fait de cliquer sur le nom d’un auteur ouvre les informations relatives aux cartes mères dans une nouvelle page.

## Kit SDK Livefyre Android ou SDK iOS {#section_zdz_spb_11b}

Livefyre fournit également deux SDK mobiles : un SDK iOS et un SDK Android. Ces SDK sont des wrappers autour de nos points de fin HTTP, conçus pour fournir une méthode plus facile d’envoi et de réception des données. Aucune interface n’est fournie avec ces kits SDK, ce qui offre une plus grande souplesse quant à la manière dont le contenu est affiché et utilisé dans votre application mobile.

Les SDK Android et iOS prennent en charge les fonctionnalités suivantes pour les commentaires, les blogs en direct et les conversations :

| Fonctionnalités d’iOS : | Fonctionnalités d'Android : |
|--- |--- |
| <ul><li> Publication </li><li>Modifier      </li><li>Marquer d’un indicateur </li><li>J’aime </li><li>Répondre </li><li>Threads chauds</li></ul> | <ul><li>Publication </li><li>Modifier      </li><li>J’aime </li><li>Répondre </li><li>Threads chauds</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Les API HTTP sont le groupe de points de fin qui vous permet de créer des conversations et du contenu sur la plateforme Livefyre. Il alimente également tous les flux Livefyre prêts à l'emploi. Bien que cette solution nécessite davantage de temps de développement de la part de votre équipe d’ingénieurs, elle offre une plus grande flexibilité lors de l’utilisation de la suite de produits Livefyre et permet une intégration mobile native.

>[!IMPORTANT]
>
>**Ne créez pas** de jetons d’authentification utilisateur au sein du client mobile, car cela impliquerait que vous exposiez votre clé réseau secrète Livefyre dans une application non sécurisée. Pour une solution plus robuste et plus sécurisée, reportez-vous à la section Jetons d’authentification utilisateur.

