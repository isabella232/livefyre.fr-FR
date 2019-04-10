---
description: Utilisez l'API d'amorçage et de diffusion en continu avec les applications
  Livefyre.
seo-description: Utilisez l'API d'amorçage et de diffusion en continu avec les applications
  Livefyre.
seo-title: Implémentation de l'application
solution: Experience Manager
title: Implémentation de l'application
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---

# Implémentation de l'application {#appimplementation}

Cas d'utilisation : En tant que client, je souhaite intégrer Livefyre dans mon CMS tiers à l'aide de la méthode Livefyre. js.

Il existe trois façons d'implémenter Livefyre dans un composant AEM ou un autre CMS, comme wordpress, Sitecore ou demandware : Implémentation de l'application Designer, API, implémentation et intégration d'authentification tierce.

## Implémentation de l'application Designer {#designerapp}

Quoi : Manière la plus simple et la plus rapide d'intégrer une application Livefyre. Vous pouvez concevoir, configurer et générer un code intégré Javascript personnalisé pour intégrer une application Liveyfre sur une page en quelques minutes.

Comment : [Création, prévisualisation, publication et incorporation d'une application Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Exemple : [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implémentation de Livefyre. js {#livefyrejsimp}

Quoi : [Livefyre. js](/help/implementation/c-livefyre.js.md) est la bibliothèque principale qui alimente les applications et les authentiques sur un site. Il définit l'objet global `window.Livefyre` et une méthode publique unique, Livefyre. require, qui peut être utilisée pour charger d'autres bibliothèques JavaScript Livefyre qui facilitent l'intégration des applications Livefyre et l'intégration aux plateformes tierces User Authentiques.

Comment:

* [Création d'une collection à l'aide du jeton collectionmeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Intégration d'applications dans un CMS tiers à l'aide des intégrations d'applications

Exemples :

* Application de commentaires : [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Révision de l'application : [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Mur multimédia : [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Pour des personnalisations avancées à l'aide du SDK, reportez-vous à la page SDK streamhub.

## Implémentation de l'API {#apiimplementation}

Pour créer des expériences et des visualisations de données personnalisées, vous pouvez créer des applications Livefyre à partir de zéro en consommant Livefyre et les données sociales à l'aide de l'API d'amorçage et de diffusion en continu.

## Intégration d'authentification tierce {#thirdpartyauth}

Pour les applications Livefyre nécessitant une authentification, reportez-vous à la section [Intégration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) d'identité pour les plateformes d'authentification tierces.

## Exemples de clients {#customerexamples}

Les clients suivants ont implémenté Livefyre avec des intégrations CMS tierces :

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
