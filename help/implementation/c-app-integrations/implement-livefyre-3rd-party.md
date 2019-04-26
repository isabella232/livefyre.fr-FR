---
description: Créez des applications Livefyre à partir de zéro pour créer des expériences
  personnalisées et des visualisations de données.
seo-description: Créez des applications Livefyre à partir de zéro pour créer des expériences
  personnalisées et des visualisations de données.
seo-title: Intégration de Livefyre avec l'intégration tiers
solution: Experience Manager
title: Intégration de Livefyre dans un CMS
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# Implémentation de Livefyre avec intégration tiers

Créez des applications Livefyre à partir de zéro pour créer des expériences personnalisées et des visualisations de données.

Vous pouvez créer une application Livefyre à partir de zéro en consommant Livefyre et les données sociales à l'aide de l'API d'amorçage et de diffusion en continu.

Pour les applications Livefyre qui requièrent une authentification, reportez-vous à la section Intégration d'identité pour plus d'informations sur les plateformes d'authentification tierces prises en charge.

Pour mettre en œuvre des applications de conversation (commentaires, chat, blog en direct, notes de sidenom) :

1. Intégration de l'application.
a. Création d'une collection à l'aide du jeton collectionmeta.
b. Intégrer les applications Livefyre aux sites à l'aide de la structure de code intégré Livefyre. js.

   * Pour plus d'informations sur l'utilisation de la structure de code intégré Livefyre. js, voir [Incorporation d'une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Pour plus d'informations sur l'intégration de l'application de commentaires, voir [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md).

   * Pour plus d'informations sur la manière d'intégrer l'application de Chat, voir [Messagerie instantanée](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Pour plus d'informations sur l'intégration de l'application de blog en direct, voir [Blog en direct](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Pour plus d'informations sur l'intégration de l'application Sidenotes, reportez-vous à [la section Remarques de Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Intégration d'authentification.
a. Créer des jetons authentiques User pour transmettre et stocker des données utilisateur dans Livefyre.
b. Intégration des plateformes d'authentification et d'utilisateur tierces. Pour obtenir la liste des plateformes prises en charge, voir [Intégration d'identité](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Personnalisation des applications. Options de personnalisation de l'application pour faire correspondre votre marque et votre style et ajouter des fonctionnalités personnalisées.

Pour créer une application de visualisation (Carte, Mur multimédia, Tendance, Carrousel, Film fixe, Storify, Carte de fonctionnalités, Mosaïque, Sondages) :

1. Intégration de l'application.
a. Création d'une collection à l'aide du jeton collectionmeta.
b. Intégrer les applications Livefyre aux sites à l'aide de la structure de code intégré Livefyre. js. Pour plus d'informations sur l'utilisation de la structure de code intégré Livefyre. js, voir [Incorporation d'une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Pour plus d'informations sur l'intégration de l'application Map, voir [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Pour plus d'informations sur l'intégration de l'application Mur multimédia, voir [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Pour plus d'informations sur l'intégration de l'application de tendance, voir [Tendance](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Intégration d'authentification.
a. Créez des jetons authentiques User pour transmettre et stocker des données utilisateur dans Livefyre.
b. Intégration des plateformes d'authentification et d'utilisateur tierces. Pour obtenir la liste des plateformes prises en charge, voir [Intégration d'identité](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre ne prend pas en charge les applications Carrousel, Filmstrip, Storify, Feature Card, Mosaic et Sondages utilisant Livefyre. js.
Intégration de ces applications à l'aide du [processus Créer une application](/help/using/c-about-apps/c-create-an-app.md) .