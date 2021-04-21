---
description: Utilisez l’API Bootstrap et Stream avec les applications Livefyre.
title: Mise en oeuvre de l’application
uuid: null
exl-id: f1edef86-491d-4f8e-8ce5-f6e019d057ec
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Implémentation de l’application {#appimplementation}

Cas d’utilisation : En tant que client, je souhaite intégrer Livefyre dans mon CMS tiers à l’aide de la méthode Livefyre.js.

Il existe trois façons d’implémenter Livefyre dans un composant AEM personnalisé ou un autre composant CMS tel que WordPress, Sitecore ou DemandWare : Mise en oeuvre de l’application Designer, API, mise en oeuvre et intégration d’authentification tierce.

## Implémentation de l’application Designer {#designerapp}

Quoi : Méthode d’intégration la plus simple et la plus rapide d’une application Livefyre. Vous pouvez concevoir, configurer et générer un code incorporé JavaScript personnalisé pour intégrer une application Liveyfre sur une page en quelques minutes.

Comment : [Créer, Prévisualisation, publier et incorporer une application Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Exemple : [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implémentation de Livefyre.js {#livefyrejsimp}

Quoi : [Livefyre.js](/help/implementation/c-livefyre.js.md) est la bibliothèque principale qui alimente Apps et Auth sur un site. Il définit l’objet global `window.Livefyre` et une méthode publique unique, Livefyre.require, qui peut être utilisée pour charger d’autres bibliothèques JavaScript Livefyre qui permettent d’incorporer des applications Livefyre et de s’intégrer à des plateformes User Auth tierces.

Comment :

* [Création d’une collection à l’aide du jeton CollectionMeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Intégration d’applications dans un CMS tiers à l’aide des intégrations d’applications

Exemples :

* Application de commentaires : [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Reviews App : [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Mur des médias : [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Pour des personnalisations avancées à l’aide du SDK, voir SDK StreamHub.

## Implémentation de l&#39;API {#apiimplementation}

Pour créer des expériences personnalisées et des visualisations de données, vous pouvez créer des applications Livefyre à partir de zéro en consommant des données Livefyre et sociales à l’aide du Bootstrap et de l’API de diffusion en continu.

## Intégration d’authentification tierce {#thirdpartyauth}

Pour les applications Livefyre nécessitant une authentification, voir [Intégration d’identité](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) pour les plateformes d’authentification tierces.

## Exemples de clients {#customerexamples}

Les clients suivants ont mis en oeuvre Livefyre avec des intégrations CMS tierces :

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
