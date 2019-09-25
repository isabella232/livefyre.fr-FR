---
description: valeur nulle
seo-description: valeur nulle
seo-title: Événements Livefyre Analytics
solution: Experience Manager
title: Événements Livefyre Analytics
uuid: 4eb5a196-ca33-40f8-a96d-ed46469223de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Événements Livefyre Analytics {#livefyre-analytics-events}

## Définition d’objet d’événement {#section_dh1_yhn_pdb}

Le code suivant définit les champs de l’objet d’événement qui sont reçus par le gestionnaire d’analyses sur une page.

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

## Evénements et eVars Livefyre Analytics {#section_u3k_tft_mcb}

Les événements Livefyre suivants à mapper aux événements personnalisés à utiliser dans les rapports à l’aide du Gestionnaire de Report Suites. Pour plus d’informations sur les suites de rapports dans Adobe Analytics, voir Gestionnaire [de suites de](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)rapports. Pour plus d’informations sur l’utilisation des événements Livefyre avec le Gestionnaire de Report Suites, voir [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Événements Livefyre Analytics

| Événement | Description |
|---|---|
| Init | Lorsqu’une page contenant au moins une application Livefyre est chargée |
| Load | Chaque fois qu’une application était chargée sur une page, quelle que soit la vue de l’utilisateur |
| Affichage | Lorsqu’une application est entrée dans la fenêtre d’affichage pour la première fois. |
| Publication | Chaque fois qu’un utilisateur publie un commentaire ou un élément de contenu, notamment : publication de niveau supérieur, réponses, commentaires, téléchargements de mur multimédia |
| Publié | Quand une publication a réussi. |
| Twitter_Reply | Chaque fois qu’un utilisateur répond sur Twitter |
| Twitter_Like | Où le contenu a été partagé dans : Retweet |
| Livefyre_Like | Chaque fois que la fonction "J’aime" est utilisée dans une application |
| Livefyre_Contrairement | Chaque fois qu’un utilisateur n’aime pas une vie comme |
| ShareOnPost | Chaque fois qu’un utilisateur publie du contenu et utilise la fonction de partage sur publication |
| ShareButtonClick | Chaque fois qu’un utilisateur clique sur le bouton de partage d’un commentaire |
| ShareTwitter | Lorsque vous cliquez sur Partager sur Twitter |
| ShareFacebook | Lorsque vous cliquez sur Partager sur Facebook |
| ShareURL | Lorsque la zone de texte Partager sur l’URL est sélectionnée/copiée. |
| DévelopperRéponses | Lorsqu’un utilisateur clique sur le lien + ou Développer pour afficher toutes les réponses dans une publication de niveau supérieur |
| RéduireRéponses | Lorsqu’un utilisateur clique sur le lien - ou Réduire pour afficher toutes les réponses dans une publication de niveau supérieur |
| FlagClick | Chaque fois qu’un utilisateur ouvre le modèle d’indicateur |
| FlagSpam | Lorsqu’un utilisateur marque le contenu comme indésirable |
| DrapeauEn désaccord | Lorsqu’un utilisateur marque le contenu comme en désaccord |
| FlagOffensive | Lorsqu’un utilisateur marque le contenu comme offensant |
| FlagOffTopic | Lorsqu’un utilisateur marque le contenu comme une rubrique hors sujet |
| FlagCancel | Chaque fois qu’un utilisateur clique sur X ou sur "Annuler" lors de l’envoi d’un indicateur |
| FollowCollection | Chaque fois qu'une conversation est suivie ("Je suis intéressé" dans les révisions) |
| UnfollowedCollection | Lorsqu’une conversation n’est pas suivie |
| RequestMore | Chaque fois qu’un utilisateur chargeait plus de contenu dans une application (doit également être à grande vitesse) |
| ModalView | Chaque fois qu’un utilisateur clique pour afficher le contenu dans un module |
| TwitterRetweetClick | Où le contenu a été partagé dans : Retweet |
| PostButtonClick | Lorsqu’un utilisateur clique sur la publication ("Que pensez-vous ?") bouton |
| Connexion | Chaque fois qu’un utilisateur se connecte |
| Déconnexion | Chaque fois qu’un utilisateur se déconnecte |

Vous trouverez ci-dessous la liste des variables de conversion (eVars) fournies par Livefyre.

## Variables de conversion - eVars

| Événement | Description |
|--- |--- |
| ID réseau | ID réseau/nom dans Livefyre |
| ID application | URL de l’application |
| ID de contexte | ID de contenu dans Livefyre |
| Type d’application | Type d’application Livefyre. Option: <br><ul><li>Live Blog  </li><li> Feature Card</li><li>Carrousel</li><li>Chat </li><li>Commentaires</li><li>Filmstrip</li><li>Carte</li><li>Mosaïque</li><li>Media Wall</li><li>Suivi des tendances</li><li>Bouton Télécharger</li></ul> |
| Type de contenu | Instagram, Twitter, Facebook, LiveFyre, YouTube, etc. |

## Plus d’infos {#section_b3d_4yl_pdb}

Pour plus d'informations sur les sujets abordés sur cette page, voir :

* [Report Suite](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[ManagerDTM](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Règles](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)