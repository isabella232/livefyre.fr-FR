---
product: livefyre
audience: end-user
user-guide-title: Guide de mise en oeuvre Livefyre
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---


# Guide de mise en oeuvre de Livefyre {#implementation}

+ [Guide de mise en oeuvre Livefyre](home.md)
+ Prise en main {#getting-started}
   + [Prise en main de l’intégration Livefyre](c-getting-started/c-getting-started.md)
   + Processus de mise en œuvre {#implementation-process}
      + [Processus de mise en œuvre](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [Types d’intégration d’application](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [Mise en oeuvre de l’application](c-getting-started/designer-app-implementation.md)
      + [Mise en oeuvre de Livefyre avec intégration tierce](c-app-integrations/implement-livefyre-3rd-party.md)
      + [Architecture](c-getting-started/c-implementation-process/c-architecture.md)
      + [Incorporer une application](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [Ajouter l’authentification à une application à l’aide de Livefyre.js](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [Créer des jetons côté serveur](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta Token](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [Jeton d’authentification utilisateur](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [Création d’une collection à l’aide du jeton CollectionMeta](t-create-a-collectionmeta-token.md)
      + [Création d’une somme de contrôle](c-creating-a-checksum.md)
+ Intégration d&#39;identité {#identity-integration}
   + [Intégration d’identité](t-about-identity-integration/t-about-identity-integration.md)
   + [Package d’authentification](t-about-identity-integration/c-authorization-package.md)
   + [AuthDelegate, objet](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [Validation des autorisations d’utilisateur sur des systèmes externes (facultatif)](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + Mise en oeuvre de l’authentification unique {#implementing-sso}
      + [Implémentation d’une authentification unique](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [Débogage du délégué d’authentification](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + Synchronisation avec Livefyre {#sync-ping-for-pull}
      + [Synchronisation avec Livefyre à l’aide de Ping pour extraction](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [Créer un point de terminaison d’extraction](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [Enregistrement du point de terminaison avec Studio](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [Création du ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [Extraire la structure de demande](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [Créer un ping pour une réponse à extraction](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Identité Livefyre {#livefyre-identity}
   + [Identité Livefyre](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [Activer l&#39;identité Livefyre](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + Utilisation des applications sociales avec l’identité Livefyre {#use-social-apps-with-livefyre-identity}
      + [Création de vos applications Social](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [Création d’une application Facebook à utiliser avec l’identité Livefyre](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [Création d’une application Twitter à utiliser avec l’identité Livefyre](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [Créez un Yahoo! Application à utiliser avec l’identité Livefyre](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [Création d’une application d’identité Microsoft Live pour une utilisation avec l’identité Livefyre](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [Création d’une application LinkedIn à utiliser avec l’identité Livefyre](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [Création d’une application d’identité GitHub à utiliser avec l’identité Livefyre](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [Utilisation de Studio pour connecter vos applications Social à votre mise en oeuvre Livefyre](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [Ajouter Livefyre.js à la page](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [Initialiser l&#39;identité Livefyre](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [Courriels pour l’identité Livefyre](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Capture/fond de panier en janvier](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + Installation {#installation}
      + [Installation des bibliothèques](c-installing-libraries/c-installing-libraries.md)
      + [Classes et méthodes](c-installing-libraries/c-methods-livefyre.md)
      + [Méthodes réseau](c-installing-libraries/c-network-methods.md)
      + [setSSL Network, méthode](c-installing-libraries/r-setssl-method.md)
      + [buildLivefyreToken, méthode réseau](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [buildUserAuthToken, méthode réseau](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLivefyreToken, méthode réseau](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncUrl, méthode réseau](c-installing-libraries/r-setusersyncurl-method.md)
      + [syncUser Network, méthode](c-installing-libraries/r-syncuser-method.md)
      + [getUrn Network, méthode](c-installing-libraries/r-geturn-method.md)
      + [getUrnForUser, méthode réseau](c-installing-libraries/r-geturnforuser-method.md)
      + [Méthode réseau getNetworkName](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite Network, méthode](c-installing-libraries/r-getsite-method.md)
      + [Méthodes de classe réseau](c-installing-libraries/c-network-class-methods.md)
      + [Méthodes de classe de collection](c-installing-libraries/c-collection-methods.md)
      + [createOrUpdate, méthode de collecte](c-installing-libraries/r-createorupdate-collection-method.md)
      + [buildCollectionMetaToken, méthode de collecte](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [Méthode de collecte buildChecksum](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent, méthode de collecte](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [getUrn, méthode de collecte](c-installing-libraries/r-geturn-collection-method.md)
      + [Méthodes de classe de site](c-installing-libraries/c-site-methods.md)
      + [buildBlogCollection, méthode du site](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [buildChatCollection, méthode du site](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [buildCommentsCollection, méthode du site](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [buildCountingCollection, méthode du site](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [buildRatingsCollection, méthode du site](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [buildReviewsCollection, méthode du site](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [buildSitenotesCollection, méthode du site](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [buildCollection, méthode du site](c-installing-libraries/r-buildcollection-site-method.md)
      + [getUrn, méthode du site](c-installing-libraries/r-geturn-site-method.md)
      + [Exemples](c-installing-libraries/c-libraries-examples.md)
   + SDK mobiles {#mobile-sdks}
      + [SDK mobiles](c-mobile-sdks/c-mobile-sdks.md)
      + [SDK iOS Livefyre](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [SDK Android](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [Création de jetons Livefyre C#](c-creating-livefyre-tokens-c-.md)
+ Intégrations des applications {#app-integrations}
   + [Chat](c-app-integrations/c-app-integratios-chat.md)
   + Commentaires {#comments}
      + [Commentaires](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [Live Blog](c-app-integrations/c-live-blog-integration.md)
   + [Critiques](c-app-integrations/c-reviews-integration.md)
   + Sidenotes {#sidenotes}
      + [Intégration de Sidenotes](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [Ajouter des identifiants à une page](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Identifie les Événements d’application](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [Identifie les options de configuration](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [Identifie les styles personnalisés](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Sidenotes Chaînes personnalisées](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Implémentation de Sidenotes](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [updateAnchors, méthode](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [Carte](c-app-integrations/c-map-integration.md)
   + [Mur multimédia](c-app-integrations/c-media-wall-integration.md)
   + [Suivi des tendances](c-app-integrations/c-trending-integration.md)
+ Personnalisations de l’application {#app-customizations}
   + [Personnalisations de l’application](c-app-customizations/c-app-customizations.md)
   + [Modifier les options d&#39;affichage](c-app-customizations/c-change-display-options.md)
   + [Classes CSS](c-app-customizations/c-css-classes.md)
   + [Storify CSS Classes](c-app-customizations/c-storify-css-classes.md)
   + [Jeux de transformations](c-app-customizations/c-translation-sets.md)
   + [Déplacer le logo Livefyre](c-app-customizations/c-move-the-livefyre-logo.md)
   + [Restreindre le média](c-app-customizations/c-restrict-media.md)
   + [Masquer les éléments d’application](c-app-customizations/c-hide-app-elements.md)
   + [Modifier l’icône de @mention](c-app-customizations/c-change-mention-icon.md)
   + [Mettre le contenu en surbrillance](c-app-customizations/c-highlight-content.md)
   + [Personnalisation de l’horodatage et de la date](c-app-customizations/c-date-time-stamp.md)
   + Contenu des fonctionnalités {#feature-content}
      + [Contenu des fonctionnalités](c-app-customizations/t-feature-content.md)
      + [Activation du contenu phare dans Studio](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [Sélectionner le contenu à inclure dans une application](c-app-customizations/t-select-content-to-feature.md)
      + [Sélectionner le contenu à inclure dans la fonction depuis Studio](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [Utiliser CSS pour mettre en forme le contenu proposé](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [API de fonctionnalités](c-app-customizations/c-feature-apis.md)
   + [Connexion de Janrain à Livefyre à l’aide d’AuthDelegate](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [Contenu proposé agrégé à l’aide des API phare](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + Contenu du style {#style-content}
      + [Contenu du groupe d’utilisateurs Style](c-app-customizations/c-style-user-group-content.md)
      + [Ajouter des utilisateurs aux groupes](c-app-customizations/c-adding-users-to-groups.md)
   + Appliquer des styles personnalisés {#apply-custom-styles}
      + [Application de styles personnalisés](c-app-customizations/c-applying-custom-styles-.md)
      + [Ajouter des boutons personnalisés](c-app-customizations/t-add-custom-buttons.md)
   + Événements JavaScript {#javascript-events}
      + [Définitions et exemples de Événements JavaScript](c-app-customizations/c-javascript-events.md)
      + [Événements JavaScript pour les applications de visualisation](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [Événements JavaScript pour la paroi multimédia](c-app-customizations/c-javascript-events-media-wall.md)
      + [Événements JavaScript pour les applications de conversation](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [Incorporer une application de commentaires](c-app-customizations/c-embed-a-comments-app.md)
   + [Suivi des renvois](c-app-customizations/c-referral-tracking.md)
   + [Prise en charge du périphérique et du navigateur](c-app-customizations/c-device-and-browser-support.md)
   + [Exigences d’affichage Twitter](c-app-customizations/c-twitter-display-requirements.md)
+ [Stratégie de test de stress](c-stress-test-policy.md)
+ Analytics {#analytics}
   +  [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [Utilisation de Livefyre avec Adobe Analytics et Dynamic Tag Manager (DTM)](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [Utilisation de Livefyre avec d’autres outils Analytics](livefyre-analytics/c-livefyre-analytics.md)
   + [Événements Livefyre Analytics](livefyre-analytics/c-livefyre-analytics-events.md)
+ [Intégration de Livefyre avec AEM](c-livefyre-aem-integration.md)
+ Rubriques avancées {#advanced-topics}
   + [Afficher le nombre de commentaires](c-advanced-topics/t-display-comment-count.md)
   + [Activation du partage sur les réseaux sociaux](c-advanced-topics/c-enabling-social-sharing.md)
   + [Flux d’Activité](c-advanced-topics/c-activity-stream.md)
   + [HTML Bootstrap](c-advanced-topics/c-bootstrap-html.md)
   + [Modifier la collection](c-advanced-topics/c-change-collection.md)
   + [Collections multiples](c-advanced-topics/c-multiple-collections.md)
   + [Changer les types d’application principaux](c-advanced-topics/c-switch-core-app-types.md)
   + [Compteur social](c-advanced-topics/c-social-counter.md)
   + [Utilisation de l’API Bootsrap et Stream avec les applications Livefyre](c-advanced-topics/bootstrap-stream-api.md)
