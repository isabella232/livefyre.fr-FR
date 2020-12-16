---
description: Créez des applications Livefyre à partir de zéro pour créer des expériences et des visualisations de données personnalisées.
seo-description: Créez des applications Livefyre à partir de zéro pour créer des expériences et des visualisations de données personnalisées.
seo-title: Intégration de Livefyre à une intégration tierce
solution: Experience Manager
title: Intégration de Livefyre dans un CMS
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 2436c389cbe14c7d64dd8c0392a3e0f031468836
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Mise en oeuvre de Livefyre avec intégration tierce

Créez des applications Livefyre à partir de zéro pour créer des expériences et des visualisations de données personnalisées.

Vous pouvez créer une application Livefyre à partir de zéro en consommant des données Livefyre et sociales à l’aide du Bootstrap et de l’API de diffusion en continu.

Pour les applications Livefyre nécessitant une authentification, voir Intégration d’identité pour plus d’informations sur les plateformes d’authentification tierces prises en charge.

Pour mettre en oeuvre des applications de conversation (commentaires, conversation, blog en direct, Sidenotes) :

1. Effectuez l’intégration de l’application.
a. Créez une collection à l’aide du jeton CollectionMeta.
b. Intégrez les applications Livefyre aux sites à l’aide de la structure de code intégrée Livefyre.js.

   * Pour plus d’informations sur l’utilisation de la structure de code incorporé Livefyre.js, voir [Incorporation d’une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Pour plus d’informations sur la façon d’intégrer l’application de commentaires, voir [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md).

   * Pour plus d&#39;informations sur la façon d&#39;intégrer l&#39;application de messagerie instantanée, consultez [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Pour plus d&#39;informations sur l&#39;intégration de l&#39;application de blog en direct, consultez [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Pour plus d’informations sur la façon d’intégrer l’application Sidenotes, voir [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Effectuez l’intégration de l’authentification.
a. Créez des jetons Auth utilisateur pour transmettre et stocker les données utilisateur dans Livefyre.
b. Intégration de plateformes d’authentification et d’utilisateurs tiers. Pour une liste des plateformes prises en charge, voir [Intégration d’identité](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Effectuez des personnalisations de l’application. Options Personnalisations de l’application pour qu’elles correspondent à votre marque et à votre style et ajouter des fonctionnalités personnalisées.

Pour créer une application de visualisation (Carte, Mur de médias, Trending, Carrousel, Filmstrip, Storify, Feature Card, Mosaic, Polluages) :

1. Effectuez l’intégration de l’application.
a. Créez une collection à l’aide du jeton CollectionMeta.
b. Intégrez les applications Livefyre aux sites à l’aide de la structure de code intégrée Livefyre.js. Pour plus d’informations sur l’utilisation de la structure de code incorporé Livefyre.js, voir [Incorporation d’une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Pour plus d’informations sur la façon d’intégrer l’application de mappage, voir [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Pour plus d’informations sur l’intégration de l’application Media Wall App, voir [Mur des médias](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Pour plus d’informations sur la façon d’intégrer l’application de tendance, voir [Trending](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Effectuez l’intégration de l’authentification.
a. Créez des jetons Auth utilisateur pour transmettre et stocker les données utilisateur dans Livefyre.
b. Intégration de plateformes d’authentification et d’utilisateurs tiers. Pour une liste des plateformes prises en charge, voir [Intégration d’identité](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre ne prend pas en charge les applications Carousel, Filmstrip, Storify, Feature Card, Mosaic et Polls à l’aide de Livefyre.js.

Intégrez ces applications à l’aide du processus [Créer une application](/help/using/c-about-apps/c-create-an-app.md).