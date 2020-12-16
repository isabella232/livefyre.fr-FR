---
description: Vérifie les offres sur un large éventail de personnalisations, ce qui vous permet de créer une application de révision qui correspond à vos besoins et à votre marque.
seo-description: Vérifie les offres sur un large éventail de personnalisations, ce qui vous permet de créer une application de révision qui correspond à vos besoins et à votre marque.
seo-title: Création d’une application de révision
solution: Experience Manager
title: Création d’une application de révision
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---


# Création d’une application de révisions {#creating-a-reviews-app}

Vérifie les offres sur un large éventail de personnalisations, ce qui vous permet de créer une application de révision qui correspond à vos besoins et à votre marque.

Utilisez l’application Reviews en l’incorporant sur votre site en tant qu’application JS. Vous ne pouvez pas créer d’application de révisions dans Livefyre Studio. Pour créer une application Reviews sur votre site, voir [Intégration Reviews](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Notations {#section_hs5_c4h_21b}

Les évaluations sont la valeur numérique que vos utilisateurs attribuent à la révision. Chaque révision doit inclure un classement, qui est affiché par défaut comme système 5 étoiles. (Tandis que les cotes s’affichent de 0,5 à 5 dans l’application, Livefyre stocke un rapport de X/100 dans l’arrière-plan, de sorte que 1 étoile soit 20/100 et 2 étoiles soit 40/100. Ce ratio s’affiche lors de l’affichage des révisions dans Studio.)

L&#39;échelle de cotation de 0,5 à 5 peut être configurée jusqu&#39;à une cote de 100, la moitié des cotations étant également disponible.

Pour plus d’informations, voir le champ maxRating pour l’objet ConvConfig Reviews.

## Style d’icône de notation {#section_cqn_c4h_21b}

Les icônes de classement peuvent être personnalisées en fonction de votre marque et de votre style.

Pour plus d&#39;informations, voir **[!UICONTROL Configure Star Ratings]** sous Reviews Customization.

## Dimensions de notation {#section_cnx_snh_21b}

Les dimensions d’évaluation sont les catégories sur lesquelles vos réviseurs évaluent votre produit ou service. Les dimensions d’évaluation sont, par exemple, &quot;performances&quot;, &quot;conception&quot;, &quot;coût&quot;, &quot;global&quot; ou toute autre catégorie de votre choix.

La valeur par défaut est d’afficher une dimension d’évaluation &quot;globale&quot;, mais vous pouvez définir et implémenter plusieurs dimensions d’évaluation, comme indiqué dans l’exemple ci-dessous.

Pour plus d’informations, voir le champ ratingDimensions sous Réviser les métadonnées de la collection.

## Vérifier les champs de texte {#section_xcm_4nh_21b}

Vous pouvez également inclure des champs de texte supplémentaires sur le produit ou l’expérience en cours de révision. (Par exemple, les champs de texte peuvent inclure les avantages et les inconvénients ou ne pas manquer.) Le numéro, le titre et le texte par défaut du champ sont personnalisables. Les utilisateurs devront remplir tous les champs de texte, ainsi que le titre, le corps et l’évaluation de la révision, afin de publier leur révision. Il n’est pas possible d’inclure des champs de texte facultatifs.

Pour plus d’informations, voir le champ ratingDimensions pour les métadonnées de la collection de révisions.

## Résumé de la révision {#section_ysz_lnh_21b}

Par défaut, une section de résumé s’affiche en haut de l’application Révisions. Cette section comprend une visualisation de la note moyenne de l’utilisateur et de la ventilation des notes pour la collection d’examens, affichant uniquement des nombres entiers. Cette section est en lecture seule et peut être masquée si vous le souhaitez.

Pour plus d’informations, voir le champ ratingSummaryEnabled pour l’objet ConvConfig de la fonction Reviews.

## Filtre de messages indésirables et de profil {#section_hcm_jnh_21b}

Le texte du titre et du corps d’une révision est transmis par notre filtre de messages indésirables et notre filtre de profil dès que la révision est publiée.

## Personnalisation du texte {#section_tjf_hnh_21b}

Les chaînes de texte, y compris les info-bulles et les libellés, peuvent être personnalisées pour la langue ou pour s’adapter à votre marque.

## Réponse à une révision {#section_yng_fnh_21b}

Les utilisateurs peuvent répondre à leur propre révision ou à celle d’autres utilisateurs dans chaque collection Reviews. Seuls les utilisateurs connectés peuvent publier une réponse à une révision.

L’option permettant aux utilisateurs de répondre à une révision est activée dans Studio. Les propriétaires peuvent activer ce paramètre au niveau du réseau, du site ou de la collection. Les modérateurs peuvent activer ce paramètre uniquement pour leurs collections.

## SocialSync et Traiter {#section_llh_2nh_21b}

Etant donné que les révisions sont conçues pour ajouter une valeur numérique pour chaque élément de contenu envoyé, SocialSync et Traiter ne sont pas pris en charge avec les révisions.

## Reviews API s {#section_xrh_wmh_21b}

Les API de révision sont disponibles pour vous permettre d’afficher les informations de ventilation des évaluations et des évaluations des utilisateurs moyennes et de passer en revue les activités des utilisateurs sur d’autres sections de votre site.

[Classifications et révisions](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Le point de terminaison de l&#39;API du Bootstrap permet aux moteurs de recherche tels que Google de lire votre révision afin que le contenu et les mots-clés puissent améliorer l&#39;optimisation de votre moteur de recherche.

* **[!UICONTROL Average User Ratings]** L&#39;API Note utilisateur moyen récupère la note utilisateur moyenne pour une ou plusieurs collections de révisions, ce qui vous permet de créer une visualisation de ces informations sur une page d&#39;index ou de les ajouter à une page d&#39;index de recherche.

* **[!UICONTROL Ratings Breakdown]** L’API de ventilation des notes récupère une ventilation de toutes les évaluations pour une collection de révisions spécifique et vous permet de créer une visualisation qui affiche le nombre de révisions associées à chaque évaluation d’étoiles.

* **[!UICONTROL User Reviews]** L’API de révisions utilisateur récupère les révisions les plus récentes pour un utilisateur spécifique. Cette activité peut être utilisée pour afficher les commentaires d’un utilisateur sur sa page de profil public.
