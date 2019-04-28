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

## Définition d&#39;objet d&#39;événement {#section_dh1_yhn_pdb}

Le code suivant définit les champs de l&#39;objet d&#39;événement qui sont reçus par le gestionnaire d&#39;analyses sur une page.

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

Événements Livefyre suivants à associer aux événements personnalisés à utiliser dans les rapports à l&#39;aide du Gestionnaire de Report Suites. Pour plus d&#39;informations sur les suites de rapports dans Adobe Analytics, reportez-vous à [la section Gestionnaire de Report Suites](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html). Pour plus d&#39;informations sur l&#39;utilisation des événements Livefyre avec le Gestionnaire de Report Suites, voir [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Événements Livefyre Analytics

| Evénement | Description |
|---|---|
| Init | Lorsqu&#39;une page contenant au moins une application Livefyre est chargée |
| Charger | Chaque fois qu&#39;une application a été chargée sur une page, quelle que soit l&#39;affichage utilisateur |
| Affichage | Lorsqu&#39;une application a saisi la fenêtre d&#39;affichage pour la première fois. |
| Publication | Chaque fois qu&#39;un utilisateur publie un commentaire ou un élément de contenu, y compris ex : publication de niveau supérieur, réponses, révision, téléchargement de mur multimédia |
| Publié | Lorsqu&#39;une publication a été approuvée. |
| Twitter_ Reply | Chaque fois qu&#39;un utilisateur a répondu sur Twitter |
| Twitter_ Like | Où le contenu a été partagé à : Retweet |
| Livefyre_ Like | Chaque fois que la fonction livefyre like est utilisée dans une application |
| Livefyre_ Against | Chaque fois qu&#39;un utilisateur n&#39;aime pas un livefyre comme |
| Shareonpost | Chaque fois qu&#39;un utilisateur publie le contenu et utilise le partage sur la fonction Publication |
| Sharebuttonclick | Chaque fois qu&#39;un utilisateur clique sur le bouton Partager d&#39;un commentaire |
| Sharetwitter | Lorsque l&#39;utilisateur clique sur Partager sur Twitter |
| Sharefacebook | Lorsque l&#39;utilisateur clique sur Partager sur Facebook |
| Shareurl | Lorsque Partager sur l&#39;URL est sélectionné/copié. |
| Expandanswers | Lorsqu&#39;un utilisateur clique sur le lien + ou Développer pour afficher toutes les réponses dans une publication globale |
| Collapsereplies | Lorsqu&#39;un utilisateur clique sur le lien - ou Réduire pour afficher toutes les réponses dans une publication globale |
| Flagclick | Chaque fois qu&#39;un utilisateur ouvre le Modal Modal |
| Flagspam | Lorsqu&#39;un utilisateur signale le contenu comme indésirable |
| Flagapprove | Lorsqu&#39;un utilisateur signale le contenu comme étant non compatible |
| Flagoffensive | Lorsqu&#39;un utilisateur signale le contenu comme injurieux |
| Flagofftopic | Lorsqu&#39;un utilisateur signale le contenu comme non actif |
| Flagcancel | Chaque fois qu&#39;un utilisateur clique sur X ou « annuler » lors de l&#39;envoi d&#39;un indicateur |
| Followcollection | Chaque fois qu&#39;une conversation est suivie (« Je suis intéressé » dans les révisions) |
| Unfollowcollection | Lorsqu&#39;une conversation n&#39;est pas suivie |
| Requestmore | Chaque fois qu&#39;un utilisateur a chargé plus de contenu dans une application (doit être pour une vitesse élevée) |
| Modalview | Chaque fois qu&#39;un utilisateur clique pour afficher le contenu dans un modal |
| Twitterretweetclick | Où le contenu a été partagé à : Retweet |
| Postbuttonclick | Lorsqu&#39;un utilisateur clique sur la publication (« What is on your mind ?  ») bouton |
| Connexion | Chaque fois qu&#39;un utilisateur est connecté |
| Déconnexion | Chaque fois qu&#39;un utilisateur déconnecte |

Voici la liste des variables de conversion (evars) fournies par Livefyre.

## Variables de conversion - evars

| Evénement | Description |
|--- |--- |
| Identifiant réseau | ID réseau/Nom dans Livefyre |
| ID de l&#39;application | URN de l&#39;application |
| ID de contexte | ID de contenu dans Livefyre |
| Type d&#39;application | Type d&#39;application Livefyre. Options : <br><ul><li>Blog en direct  </li><li> Carte de fonctionnalités</li><li>Carrousel</li><li>Chat </li><li>Commentaires</li><li>Film fixe</li><li>Carte</li><li>Mosaic</li><li>Mur multimédia</li><li>Tendances</li><li>Bouton Télécharger</li></ul> |
| Type de contenu | Instagram, Twitter, Facebook, livefyre, YouTube, etc. |

## Plus d&#39;informations {#section_b3d_4yl_pdb}

Pour plus d&#39;informations sur les sujets abordés sur cette page, voir :

* [Report Suite managerdtm](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Règles](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)