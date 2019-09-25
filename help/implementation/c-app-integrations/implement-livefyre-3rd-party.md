---
description: Créez des applications Livefyre de zéro pour créer des expériences personnalisées et des visualisations de données.
seo-description: Créez des applications Livefyre de zéro pour créer des expériences personnalisées et des visualisations de données.
seo-title: Intégration de Livefyre à l’intégration tierce
solution: Experience Manager
title: Intégration de Livefyre dans un CMS
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# Mise en oeuvre de Livefyre avec intégration tierce

Créez des applications Livefyre de zéro pour créer des expériences personnalisées et des visualisations de données.

Vous pouvez créer une application Livefyre à partir de zéro en consommant des données Livefyre et sociales à l’aide de l’API d’amorçage et de diffusion en continu.

Pour les applications Livefyre nécessitant une authentification, voir Intégration d’identité pour plus d’informations sur les plateformes d’authentification tierces prises en charge.

Pour mettre en oeuvre des applications de conversation (commentaires, conversation, blog en direct, Sidenotes) :

1. Effectuez l’intégration de l’application.
a. Créez une collection à l’aide du jeton CollectionMeta.
b. Intégrez les applications Livefyre aux sites à l’aide de la structure de code intégré Livefyre.js.

   * Pour plus d’informations sur l’utilisation de la structure de code intégré Livefyre.js, voir [Incorporation d’une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Pour plus d’informations sur l’intégration de l’application de commentaires, voir [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md).

   * Pour plus d'informations sur la manière d'intégrer l'application de messagerie instantanée, consultez [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Pour plus d'informations sur l'intégration de l'application de blog en direct, consultez [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Pour plus d’informations sur l’intégration de l’application Sidenotes, voir [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Effectuez l’intégration de l’authentification.
a. Créez des jetons Auth utilisateur pour transmettre et stocker les données utilisateur dans Livefyre.
b. Intégrer des utilisateurs tiers et des plateformes d’authentification. Pour obtenir la liste des plateformes prises en charge, voir Intégration [des](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)identités.

1. Effectuez des personnalisations d’application. Options de personnalisation de l’application pour qu’elles correspondent à votre marque et à votre style et ajouter des fonctionnalités personnalisées.

Pour créer une application de visualisation (zone cliquable, mur multimédia, tendance, carrousel, bande de film, page Facebook, carte de fonctionnalités, mosaïque, sondages) :

1. Effectuez l’intégration de l’application.
a. Créez une collection à l’aide du jeton CollectionMeta.
b. Intégrez les applications Livefyre aux sites à l’aide de la structure de code intégré Livefyre.js. Pour plus d’informations sur l’utilisation de la structure de code intégré Livefyre.js, voir [Incorporation d’une application](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Pour plus d’informations sur l’intégration de l’application de mappage, voir [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Pour plus d’informations sur l’intégration de l’application Media Wall [, voir Mur](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md)des médias.

   * Pour plus d’informations sur l’intégration de l’application de tendance, voir [Tendance](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Effectuez l’intégration de l’authentification.
a. Créez des jetons Auth utilisateur pour transmettre et stocker les données utilisateur dans Livefyre.
b. Intégrer des utilisateurs tiers et des plateformes d’authentification. Pour obtenir la liste des plateformes prises en charge, voir Intégration [des](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)identités.

>[!NOTE]
>
>Livefyre ne prend pas en charge les applications Carousel, Filmstrip, Storify, Feature Card, Mosaic et Polls à l’aide de Livefyre.js.
Intégrez ces applications à l’aide du processus [Créer une application](/help/using/c-about-apps/c-create-an-app.md) .