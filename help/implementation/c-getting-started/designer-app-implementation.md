---
description: Utilisez Bootstrap et Stream API avec les applications Livefyre.
seo-description: Utilisez Bootstrap et Stream API avec les applications Livefyre.
seo-title: Implémentation de l’application
solution: Experience Manager
title: Implémentation de l’application
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# Implémentation de l’application {#appimplementation}

Cas d’utilisation : En tant que client, je souhaite intégrer Livefyre dans mon CMS tiers à l’aide de la méthode Livefyre.js.

Il existe trois manières d’implémenter Livefyre dans un composant AEM personnalisé ou un autre CMS comme WordPress, Sitecore ou DemandWare : Implémentation d’application Designer, API, implémentation et intégration d’authentification tierce.

## Implémentation d’applications Designer {#designerapp}

Quoi : Méthode la plus simple et la plus rapide d’intégration d’une application Livefyre. Vous pouvez concevoir, configurer et générer un code incorporé JavaScript personnalisé pour intégrer une application Liveyfre sur une page en quelques minutes.

Comment : [Créer, prévisualiser, publier et incorporer une application Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Exemple : [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implémentation de Livefyre.js {#livefyrejsimp}

Quoi : [Livefyre.js](/help/implementation/c-livefyre.js.md) est la bibliothèque principale qui alimente les applications et l’authentification sur un site. Il définit l’ `window.Livefyre` objet global et une méthode publique unique, Livefyre.require, qui peut être utilisée pour charger d’autres bibliothèques JavaScript Livefyre qui permettent d’incorporer des applications Livefyre et de les intégrer à des plateformes User Auth tierces.

Comment :

* [Création d’une collection à l’aide du jeton CollectionMeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Intégration d’applications dans un CMS tiers à l’aide des intégrations d’applications

Exemples :

* Application de commentaires : [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Reviews App : [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Mur des médias : [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Pour des personnalisations avancées à l’aide du SDK, voir SDK StreamHub.

## Implémentation d’API {#apiimplementation}

Pour créer des expériences personnalisées et des visualisations de données, vous pouvez créer des applications Livefyre à partir de zéro en utilisant les données Livefyre et sociales à l’aide de l’API d’amorçage et de diffusion en continu.

## Intégration de l’authentification tierce {#thirdpartyauth}

Pour les applications Livefyre nécessitant une authentification, voir Intégration [d’](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) identité pour les plateformes d’authentification tierces.

## Exemples de clients {#customerexamples}

Les clients suivants ont implémenté Livefyre avec des intégrations CMS tierces :

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
