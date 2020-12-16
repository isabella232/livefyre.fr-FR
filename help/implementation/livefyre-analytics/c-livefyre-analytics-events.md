---
description: valeur nulle
seo-description: valeur nulle
seo-title: Événements Livefyre Analytics
solution: Experience Manager
title: Événements Livefyre Analytics
uuid: 4eb5a196-ca33-40f8-a96d-ed46469223de
translation-type: tm+mt
source-git-commit: 5dc11c42a9f8bf3fa088f3245e21b6942d4865fe
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 4%

---


# Événements Livefyre Analytics

## Définition d&#39;objet événement {#section_dh1_yhn_pdb}

Le code suivant définit les champs de l’objet de événement qui sont reçus par le gestionnaire d’analyses sur une page.

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

## Événements et eVars Livefyre Analytics {#section_u3k_tft_mcb}

Les événements Livefyre suivants à mapper sur des événements personnalisés à utiliser dans les rapports à l’aide du Gestionnaire de Report Suites. Pour plus d’informations sur les Report Suites en Adobe Analytics, voir [Gestionnaire de Report Suites](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html). Pour plus d&#39;informations sur l&#39;utilisation des événements Livefyre avec le Gestionnaire de Report Suites, voir [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Événements Livefyre Analytics

| Événement | Description |
|---|---|
| Init | Lorsqu’une page contenant au moins une application Livefyre est chargée |
| Load | Chaque fois qu’une application était chargée sur une page, quelle que soit la vue de l’utilisateur |
| Affichage | Lorsqu’une application est entrée dans la fenêtre d’affichage pour la première fois. |
| Publication | Chaque fois qu’un utilisateur publie un commentaire ou un élément de contenu, y compris par exemple : publication de niveau supérieur, réponses, commentaires, téléchargements de mur multimédia |
| Publié | Lorsqu’une publication a réussi. |
| Twitter_Reply | Chaque fois qu’un utilisateur répond sur Twitter |
| Twitter_Like | Où le contenu a été partagé avec : Retweet |
| Livefyre_Like | Chaque fois que la fonction &quot;j’aime&quot; est utilisée dans une application |
| Livefyre_Contrairement | Chaque fois qu’un utilisateur n’aime pas un livre animé comme |
| ShareOnPost | Chaque fois qu’un utilisateur publie du contenu et utilise la fonction de partage sur la publication |
| ShareButtonClick | Chaque fois qu’un utilisateur clique sur le bouton de partage d’un commentaire. |
| ShareTwitter | Lorsque vous cliquez sur Partager sur Twitter |
| ShareFacebook | Lorsque vous cliquez sur Partager sur Facebook |
| ShareURL | Lorsque la zone de texte Partager sur l’URL est sélectionnée/copiée. |
| DévelopperRéponses | Lorsqu’un utilisateur clique sur le lien + ou Développer pour vue toutes les réponses d’une publication de niveau supérieur |
| RéduireRéponses | Lorsqu’un utilisateur clique sur le lien - ou Réduire pour vue toutes les réponses dans une publication de niveau supérieur |
| FlagClick | Chaque fois qu&#39;un utilisateur ouvre le modèle d&#39;indicateur |
| IndicateurIndésirable | Lorsqu’un utilisateur marque un contenu comme indésirable |
| DrapeauDésaccord | Lorsqu’un utilisateur marque le contenu comme en désaccord |
| DrapeauOffensive | Lorsqu’un utilisateur marque un contenu comme offensant |
| FlagOffTopic | Lorsqu’un utilisateur marque le contenu comme non-sujet |
| IndicateurAnnuler | Chaque fois qu’un utilisateur clique sur X ou sur &quot;annuler&quot; lors de l’envoi d’un indicateur |
| FollowCollection | Chaque fois qu&#39;une conversation est suivie (&quot;Je suis intéressé&quot; dans les critiques) |
| UnfollowCollection | Lorsqu’une conversation n’est pas suivie |
| RequestMore | Chaque fois qu’un utilisateur a chargé plus de contenu dans une application (doit également être à grande vitesse) |
| ModalView | Chaque fois qu’un utilisateur clique pour vue du contenu dans un module |
| TwitterRetweetClick | Où le contenu a été partagé avec : Retweet |
| PostButtonClick | Lorsqu’un utilisateur clique sur la publication (&quot;Qu’est-ce que vous pensez ?&quot;) bouton |
| Connexion | Chaque fois qu’un utilisateur se connecte |
| Déconnexion | Chaque fois qu’un utilisateur se déconnecte |

Voici une liste de variables de conversion (eVars) fournies par Livefyre.

## Variables de conversion - eVars

| Événement | Description |
|--- |--- |
| ID réseau | ID/nom réseau dans Livefyre |
| ID application | URL de l’application |
| ID de contexte | ID de contenu dans Livefyre |
| Type d’application | Type d’application Livefyre. Option: <br><ul><li>Live Blog  </li><li> Carte des fonctionnalités</li><li>Carrousel</li><li>Chat </li><li>Commentaires</li><li>Filmstrip</li><li>Carte</li><li>Mosaïque</li><li>Mur multimédia</li><li>Suivi des tendances</li><li>Bouton Télécharger</li></ul> |
| Type de contenu | Instagram, Twitter, Facebook, LiveFyre, YouTube, etc. |

## Plus d’infos {#section_b3d_4yl_pdb}

Pour plus d&#39;informations sur les sujets abordés sur cette page, voir :

* [Report Suite ](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[ManagerDTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [Règles](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)