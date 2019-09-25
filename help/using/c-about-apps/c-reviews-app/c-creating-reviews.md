---
description: Reviews offre un large éventail de personnalisations, vous permettant de créer une application de révision qui correspond à vos besoins et à votre marque.
seo-description: Reviews offre un large éventail de personnalisations, vous permettant de créer une application de révision qui correspond à vos besoins et à votre marque.
seo-title: Création d’une application de révision
solution: Experience Manager
title: Création d’une application de révision
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d’une application de révision{#creating-a-reviews-app}

Reviews offre un large éventail de personnalisations, vous permettant de créer une application de révision qui correspond à vos besoins et à votre marque.

Utilisez l’application Reviews en l’incorporant sur votre site en tant qu’application JS. Vous ne pouvez pas créer d’application de révisions dans Livefyre Studio. Pour créer une application de révisions sur votre site, voir Intégration des [révisions](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Évaluations {#section_hs5_c4h_21b}

Les évaluations sont la valeur numérique que vos utilisateurs attribuent à la révision. Chaque révision doit inclure une note, qui s’affiche par défaut sous la forme d’un système 5 étoiles. (Alors que les notes sont affichées de 0,5 à 5 dans l’application, Livefyre stocke un rapport de X/100 dans le serveur principal, de sorte qu’une étoile soit 20/100 et que 2 étoiles soit 40/100. Ce ratio s’affiche lors de l’affichage des révisions dans Studio.)

L’échelle de notation de 0,5 à 5 peut être configurée jusqu’à 100, la moitié des évaluations étant également disponible.

Pour plus d’informations, voir le champ maxRating pour l’objet ConvConfig Reviews.

## Style d’icône de classement {#section_cqn_c4h_21b}

Les icônes d’évaluation peuvent être personnalisées en fonction de votre marque et de votre style.

Pour plus d’informations, voir **[!UICONTROL Configure Star Ratings]** sous Reviews Customization.

## Évaluation des dimensions {#section_cnx_snh_21b}

Les dimensions d’évaluation sont les catégories dans lesquelles vos réviseurs évaluent votre produit ou service. Les dimensions d’évaluation sont, par exemple, "performance", "conception", "coût", "global" ou toute autre catégorie que vous choisissez.

La valeur par défaut est d’afficher une dimension "globale", mais vous pouvez définir et implémenter plusieurs dimensions, comme illustré dans l’exemple ci-dessous.

Pour plus d’informations, voir le champ ratingDimensions sous Réviser les métadonnées de la collection.

## Vérifier les champs de texte {#section_xcm_4nh_21b}

Vous pouvez également inclure des champs de texte supplémentaires sur le produit ou l’expérience en cours de révision. (Par exemple, les champs de texte peuvent inclure les avantages et les inconvénients ou ne pas manquer.) Le numéro, le titre et le texte par défaut du champ sont personnalisables. Les utilisateurs devront remplir tous les champs de texte, ainsi que le titre, le corps et l’évaluation de la révision, afin de publier leur révision. Il n’est pas possible d’inclure des champs de texte facultatifs.

Pour plus d’informations, voir le champ ratingDimensions pour les métadonnées de la collection de révisions.

## Résumé de la révision {#section_ysz_lnh_21b}

Par défaut, une section de résumé s’affiche en haut de l’application de révisions. Cette section comprend une visualisation de la note moyenne de l’utilisateur et de la ventilation des notes pour la collection Reviews, affichant uniquement des nombres entiers. Cette section est en lecture seule et peut être masquée si vous le souhaitez.

Pour plus d’informations, voir le champ ratingSummaryEnabled pour l’objet ConvConfig des révisions.

## Filtre spam et profil {#section_hcm_jnh_21b}

Le texte du titre et du contenu d’une révision est transmis par notre filtre de messages indésirables et de profil dès que la révision est publiée.

## Personnalisation du texte {#section_tjf_hnh_21b}

Les chaînes de texte, y compris les info-bulles et les étiquettes, peuvent être personnalisées pour la langue ou pour s’adapter à votre marque.

## Réponse à une révision {#section_yng_fnh_21b}

Les utilisateurs peuvent répondre à leur propre révision ou à celle d’autres utilisateurs dans chaque collection Reviews. Seuls les utilisateurs connectés peuvent publier une réponse à une révision.

L’option permettant aux utilisateurs de répondre à une révision est activée dans Studio. Les propriétaires peuvent activer/désactiver ce paramètre au niveau du réseau, du site ou de la collection. Les modérateurs peuvent activer ce paramètre uniquement pour leurs collections.

## SocialSync et traiter {#section_llh_2nh_21b}

Etant donné que les révisions sont conçues pour ajouter une valeur numérique pour chaque élément de contenu envoyé, SocialSync et le traitement ne sont pas pris en charge avec les révisions.

## API Reviews {#section_xrh_wmh_21b}

Les API de révision sont disponibles pour vous permettre d’afficher les informations de ventilation de notation et d’évaluation des utilisateurs moyens et l’activité de révision des utilisateurs sur d’autres sections de votre site.

[Notations et révisions](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Le point de terminaison de l'API Bootstrap permet à votre révision d'être lue par des moteurs de recherche comme Google, de sorte que le contenu et les mots-clés puissent améliorer l'optimisation de votre moteur de recherche.

* **[!UICONTROL Average User Ratings]** L’API Note utilisateur moyenne récupère la note utilisateur moyenne pour une ou plusieurs collections Reviews, ce qui vous permet de créer une visualisation de ces informations sur une page d’index ou de les ajouter à une page d’index de recherche.

* **[!UICONTROL Ratings Breakdown]** L’API de ventilation des notes récupère une ventilation de toutes les évaluations pour une collection de révisions spécifique et vous permet de créer une visualisation qui affiche le nombre de révisions associées à chaque évaluation.

* **[!UICONTROL User Reviews]** L’API de révisions utilisateur récupère les révisions les plus récentes pour un utilisateur spécifique. Cette activité peut être utilisée pour afficher les commentaires d’un utilisateur sur sa page de profil publique.
