---
description: Utilisez l'API d'amorçage et de diffusion en continu avec les applications Livefyre.
seo-description: Utilisez l'API d'amorçage et de diffusion en continu avec les applications Livefyre.
seo-title: Implémentation de l'application
solution: Experience Manager
title: Implémentation de l'application
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# Implémentation de l&#39;application {#appimplementation}

Cas d&#39;utilisation : En tant que client, je souhaite intégrer Livefyre dans mon CMS tiers à l&#39;aide de la méthode Livefyre. js.

Il existe trois façons d&#39;implémenter Livefyre dans un composant AEM ou un autre CMS, comme wordpress, Sitecore ou demandware : Implémentation de l&#39;application Designer, API, implémentation et intégration d&#39;authentification tierce.

## Implémentation de l&#39;application Designer {#designerapp}

Quoi : Manière la plus simple et la plus rapide d&#39;intégrer une application Livefyre. Vous pouvez concevoir, configurer et générer un code intégré Javascript personnalisé pour intégrer une application Liveyfre sur une page en quelques minutes.

Comment : [Création, prévisualisation, publication et incorporation d&#39;une application Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Exemple : [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implémentation de Livefyre. js {#livefyrejsimp}

Quoi : [Livefyre. js](/help/implementation/c-livefyre.js.md) est la bibliothèque principale qui alimente les applications et les authentiques sur un site. Il définit l&#39;objet global `window.Livefyre` et une méthode publique unique, Livefyre. require, qui peut être utilisée pour charger d&#39;autres bibliothèques JavaScript Livefyre qui facilitent l&#39;intégration des applications Livefyre et l&#39;intégration aux plateformes tierces User Authentiques.

Comment:

* [Création d&#39;une collection à l&#39;aide du jeton collectionmeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Intégration d&#39;applications dans un CMS tiers à l&#39;aide des intégrations d&#39;applications

Exemples :

* Application de commentaires : [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Révision de l&#39;application : [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Mur multimédia : [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Pour des personnalisations avancées à l&#39;aide du SDK, reportez-vous à la page SDK streamhub.

## Implémentation de l&#39;API {#apiimplementation}

Pour créer des expériences et des visualisations de données personnalisées, vous pouvez créer des applications Livefyre à partir de zéro en consommant Livefyre et les données sociales à l&#39;aide de l&#39;API d&#39;amorçage et de diffusion en continu.

## Intégration d&#39;authentification tierce {#thirdpartyauth}

Pour les applications Livefyre nécessitant une authentification, reportez-vous à la section [Intégration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) d&#39;identité pour les plateformes d&#39;authentification tierces.

## Exemples de clients {#customerexamples}

Les clients suivants ont implémenté Livefyre avec des intégrations CMS tierces :

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
