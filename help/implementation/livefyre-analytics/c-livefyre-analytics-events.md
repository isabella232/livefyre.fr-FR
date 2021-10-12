---
title: Événements Livefyre Analytics
description: Événements Livefyre Analytics
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 5%

---

# Événements Livefyre Analytics

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

## Événements et eVars Livefyre Analytics {#section_u3k_tft_mcb}

Les événements Livefyre suivants à mapper aux événements personnalisés à utiliser dans les rapports à l’aide du Gestionnaire de suites de rapports. Pour plus d’informations sur les suites de rapports dans Adobe Analytics, voir [Gestionnaire de suites de rapports](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en). Pour plus d’informations sur l’utilisation des événements Livefyre avec le Gestionnaire de suites de rapports, voir [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Événements Livefyre Analytics

| Événement | Description |
|---|---|
| Init | Lorsqu’une page qui comprend au moins une application Livefyre est chargée |
| Load | Chaque fois qu’une application était chargée sur une page, quelle que soit la vue de l’utilisateur. |
| Affichage | Lorsqu’une application est entrée dans la fenêtre d’affichage pour la première fois. |
| Publication | Chaque fois qu’un utilisateur publie un commentaire ou un contenu, y compris par exemple : publication de niveau supérieur, réponses, commentaires, téléchargements de mur multimédia |
| Publié | Lorsqu’une publication a réussi. |
| Twitter_Reply | Chaque fois qu’un utilisateur a répondu sur Twitter |
| Twitter_Like | Où le contenu a été partagé sur : Retweet |
| Livefyre_Like | Chaque fois que la fonction &quot;j’aime&quot; est utilisée dans une application. |
| Livefyre_Contrairement | Chaque fois qu’un utilisateur n’aime pas une virée comme |
| ShareOnPost | Chaque fois qu’un utilisateur publie du contenu et utilise la fonction de partage sur publication |
| ShareButtonClick | Chaque fois qu’un utilisateur clique sur le bouton de partage d’un commentaire |
| ShareTwitter | Lorsque vous cliquez sur Partager sur Twitter |
| ShareFacebook | Lorsque vous cliquez sur Partager sur Facebook |
| ShareURL | Lorsque la zone de texte Partager sur l’URL est sélectionnée/copiée. |
| Développer les réponses | Lorsqu’un utilisateur clique sur le lien + ou Développer pour afficher toutes les réponses dans une publication de niveau supérieur |
| Réduire les réponses | Lorsqu’un utilisateur clique sur le lien - ou Réduire pour afficher toutes les réponses sur une publication de niveau supérieur |
| FlagClick | Chaque fois qu’un utilisateur ouvre le modèle d’indicateur |
| FlagSpam | Lorsqu’un utilisateur marque le contenu comme indésirable |
| FlagDissame | Lorsqu’un utilisateur marque le contenu comme en désaccord |
| FlagOffensive | Lorsqu’un utilisateur marque le contenu comme étant offensant |
| FlagOffTopic | Lorsqu’un utilisateur marque le contenu comme non-sujet |
| FlagCancel | Chaque fois qu’un utilisateur clique sur X ou &quot;annule&quot; lors de l’envoi d’un indicateur |
| FollowCollection | Chaque fois qu&#39;une conversation est suivie (&quot;Je suis intéressé&quot; dans Révisions) |
| UnFollowCollection | Lorsqu’une conversation n’est pas suivie |
| RequestMore | Chaque fois qu’un utilisateur charge plus de contenu dans une application (doit également être à grande vitesse) |
| ModalView | Chaque fois qu’un utilisateur clique pour afficher du contenu dans un modal. |
| TwitterRetweetClick | Où le contenu a été partagé sur : Retweet |
| PostButtonClick | Lorsqu’un utilisateur clique sur la publication (&quot;Qu’est-ce que vous pensez ?&quot;) button |
| Connexion | Chaque fois qu’un utilisateur se connecte |
| Déconnexion | Chaque fois qu’un utilisateur s’est connecté. |

Vous trouverez ci-dessous une liste des variables de conversion (eVars) fournies par Livefyre.

## Variables de conversion - eVars

| Événement | Description |
|--- |--- |
| Identifiant réseau | Identifiant/nom réseau dans Livefyre |
| ID application | URL de l’application |
| ID de contexte | ID de contenu dans Livefyre |
| Type d’application | Type d’application Livefyre. Option: <br><ul><li>Live Blog  </li><li> Carte des fonctionnalités</li><li>Carrousel</li><li>Chat </li><li>Commentaires</li><li>Filmstrip</li><li>Carte</li><li>Mosaic</li><li>Mur multimédia</li><li>Suivi des tendances</li><li>Bouton Télécharger</li></ul> |
| Type de contenu | Instagram, Twitter, Facebook, LiveFyre, YouTube, etc. |

## Plus d’infos {#section_b3d_4yl_pdb}

Pour plus d’informations sur les sujets abordés sur cette page, voir :

* [Gestionnaire de suites de rapports](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)
* [Balises](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
