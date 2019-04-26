---
description: valeur nulle
seo-description: valeur nulle
seo-title: Événements Livefyre Analytics
solution: Experience Manager
title: Événements Livefyre Analytics
uuid: 4 eb 5 a 196-ca 33-40 f 8-a 96 d-ed 46469223 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Événements Livefyre Analytics {#livefyre-analytics-events}

## Définition d'objet d'événement {#section_dh1_yhn_pdb}

Le code suivant définit les champs de l'objet d'événement qui sont reçus par le gestionnaire d'analyses sur une page.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Evars et événements Analytics Livefyre {#section_u3k_tft_mcb}

Événements Livefyre suivants à associer aux événements personnalisés à utiliser dans les rapports à l'aide du Gestionnaire de Report Suites. Pour plus d'informations sur les suites de rapports dans Adobe Analytics, reportez-vous à [la section Gestionnaire de Report Suites](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html). Pour plus d'informations sur l'utilisation des événements Livefyre avec le Gestionnaire de Report Suites, voir [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Événements Livefyre Analytics

| Evénement | Description |
|---|---|
| Init | Lorsqu'une page contenant au moins une application Livefyre est chargée |
| Charger | Chaque fois qu'une application a été chargée sur une page, quelle que soit l'affichage utilisateur |
| Affichage | Lorsqu'une application a saisi la fenêtre d'affichage pour la première fois. |
| Publication | Chaque fois qu'un utilisateur publie un commentaire ou un élément de contenu, y compris ex : publication de niveau supérieur, réponses, révision, téléchargement de mur multimédia |
| Publié | Lorsqu'une publication a été approuvée. |
| Twitter_ Reply | Chaque fois qu'un utilisateur a répondu sur Twitter |
| Twitter_ Like | Où le contenu a été partagé à : Retweet |
| Livefyre_ Like | Chaque fois que la fonction livefyre like est utilisée dans une application |
| Livefyre_ Against | Chaque fois qu'un utilisateur n'aime pas un livefyre comme |
| Shareonpost | Chaque fois qu'un utilisateur publie le contenu et utilise le partage sur la fonction Publication |
| Sharebuttonclick | Chaque fois qu'un utilisateur clique sur le bouton Partager d'un commentaire |
| Sharetwitter | Lorsque l'utilisateur clique sur Partager sur Twitter |
| Sharefacebook | Lorsque l'utilisateur clique sur Partager sur Facebook |
| Shareurl | Lorsque Partager sur l'URL est sélectionné/copié. |
| Expandanswers | Lorsqu'un utilisateur clique sur le lien + ou Développer pour afficher toutes les réponses dans une publication globale |
| Collapsereplies | Lorsqu'un utilisateur clique sur le lien - ou Réduire pour afficher toutes les réponses dans une publication globale |
| Flagclick | Chaque fois qu'un utilisateur ouvre le Modal Modal |
| Flagspam | Lorsqu'un utilisateur signale le contenu comme indésirable |
| Flagapprove | Lorsqu'un utilisateur signale le contenu comme étant non compatible |
| Flagoffensive | Lorsqu'un utilisateur signale le contenu comme injurieux |
| Flagofftopic | Lorsqu'un utilisateur signale le contenu comme non actif |
| Flagcancel | Chaque fois qu'un utilisateur clique sur X ou « annuler » lors de l'envoi d'un indicateur |
| Followcollection | Chaque fois qu'une conversation est suivie (« Je suis intéressé » dans les révisions) |
| Unfollowcollection | Lorsqu'une conversation n'est pas suivie |
| Requestmore | Chaque fois qu'un utilisateur a chargé plus de contenu dans une application (doit être pour une vitesse élevée) |
| Modalview | Chaque fois qu'un utilisateur clique pour afficher le contenu dans un modal |
| Twitterretweetclick | Où le contenu a été partagé à : Retweet |
| Postbuttonclick | Lorsqu'un utilisateur clique sur la publication (« What is on your mind ?  ») bouton |
| Connexion | Chaque fois qu'un utilisateur est connecté |
| Déconnexion | Chaque fois qu'un utilisateur déconnecte |

Voici la liste des variables de conversion (evars) fournies par Livefyre.

## Variables de conversion - evars

| Evénement | Description |
|--- |--- |
| Identifiant réseau | ID réseau/Nom dans Livefyre |
| ID de l'application | URN de l'application |
| ID de contexte | ID de contenu dans Livefyre |
| Type d'application | Type d'application Livefyre. Options : <br><ul><li>Blog en direct  </li><li> Carte de fonctionnalités</li><li>Carrousel</li><li>Chat </li><li>Commentaires</li><li>Film fixe</li><li>Carte</li><li>Mosaic</li><li>Mur multimédia</li><li>Tendances</li><li>Bouton Télécharger</li></ul> |
| Type de contenu | Instagram, Twitter, Facebook, livefyre, YouTube, etc. |

## Plus d'informations {#section_b3d_4yl_pdb}

Pour plus d'informations sur les sujets abordés sur cette page, voir :

* [Report Suite managerdtm](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Règles](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)