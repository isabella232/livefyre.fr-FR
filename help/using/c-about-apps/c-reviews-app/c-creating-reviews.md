---
description: Les révisions offrent une grande variété de personnalisations, ce qui
  vous permet de créer une application de révision qui correspond à vos besoins et
  à votre marque.
seo-description: Les révisions offrent une grande variété de personnalisations, ce
  qui vous permet de créer une application de révision qui correspond à vos besoins
  et à votre marque.
seo-title: Création d'une application de révision
solution: Experience Manager
title: Création d'une application de révision
uuid: 6 caeafe 7-c 04 e -484 e-b 02 f -98 dc 6 d 9 b 3184
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Création d'une application de révision{#creating-a-reviews-app}

Les révisions offrent une grande variété de personnalisations, ce qui vous permet de créer une application de révision qui correspond à vos besoins et à votre marque.

Utilisez l'application de révision en l'incorporant personnalisée sur votre site en tant qu'application JS. Vous ne pouvez pas créer une application de révision dans Livefyre Studio. Pour créer une application de révision sur votre site, voir [Révision de l'intégration](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Évaluations {#section_hs5_c4h_21b}

Les évaluations sont la valeur numérique que vos utilisateurs attribuent à la révision. Chaque révision doit inclure une évaluation, qui s'affiche par défaut sous la forme d'un système 5 étoiles. (Alors que les évaluations s'affichent sous la forme 0.5 - 5 dans l'application, Livefyre stocke un rapport X/100 dans le serveur principal, de sorte que 1 étoile soit 20/100 et 2 étoiles est de 40/100. Ce rapport s'affiche lors de l'affichage des révisions dans Studio.)

L'échelle d'évaluation de 0,5 à 5 peut être configurée jusqu'à 100, avec une note de moitié également disponible.

Pour plus d'informations, voir le champ maxrating pour l'objet Reviews convconfig.

## Style de l'icône de notation {#section_cqn_c4h_21b}

Les icônes d'évaluation peuvent être personnalisées en fonction de votre marque et de votre style.

Pour plus d'informations, **[!UICONTROL Configure Star Ratings]** consultez la section Révision de la personnalisation.

## Dimensions de notation {#section_cnx_snh_21b}

Les dimensions d'évaluation sont les catégories sur lesquelles vos réviseurs évaluent votre produit ou service. Les exemples de dimensions d'évaluation sont les « performances », « conception », « coût », « général » ou toute autre catégorie choisie.

Par défaut, vous pouvez afficher une dimension d'évaluation globale, mais vous pouvez définir et implémenter plusieurs dimensions de notation, comme indiqué dans l'exemple ci-dessous.

Pour plus d'informations, voir le champ ratingdimensions sous Révision des métadonnées de collection.

## Examiner les champs de texte {#section_xcm_4nh_21b}

Vous pouvez également inclure des champs de texte supplémentaires sur le produit ou l'expérience en cours de révision. (Par exemple, les champs de texte peuvent inclure les avantages - et - inconvénients ou Ne pas manquer.) Le numéro, le titre et le texte par défaut du champ sont personnalisables. Les utilisateurs devront remplir tous les champs de texte, ainsi que le titre, le corps et la note de révision afin de publier leur révision. Il est impossible d'inclure des champs de texte facultatifs.

Pour plus d'informations, voir le champ ratingdimensions pour les métadonnées de la collection de révisions.

## Résumé de révision {#section_ysz_lnh_21b}

Par défaut, une section de résumé s'affiche en haut de l'application de révision. Cette section comprend une visualisation de la note d'utilisateur moyenne et de la ventilation d'évaluation pour la collection des révisions, affichant des nombres entiers uniquement. Cette section est en lecture seule et peut être masquée si vous le souhaitez.

Pour plus d'informations, voir le champ ratingsummaryenabled pour l'objet Reviews convconfig.

## Filtre des messages indésirables et du profilage {#section_hcm_jnh_21b}

Le texte du titre et du corps d'une révision est transmis via notre filtre de messages indésirables et le filtre de profilité dès que la révision est publiée.

## Personnalisation du texte {#section_tjf_hnh_21b}

Les chaînes de texte, y compris les info-bulles et les étiquettes, peuvent être personnalisées pour la langue ou pour s'adapter à votre marque.

## Réponse à une révision {#section_yng_fnh_21b}

Les utilisateurs peuvent répondre à leur propre révision ou à la révision d'un autre utilisateur dans chaque collection de révisions. Seuls les utilisateurs connectés peuvent publier une réponse à une révision.

L'option permettant aux utilisateurs de répondre à une révision est activée dans Studio. Les propriétaires peuvent activer ce paramètre pour le niveau réseau, site ou collection. Les modérateurs peuvent uniquement activer ce paramètre pour leurs collections.

## Socialsync et traitement {#section_llh_2nh_21b}

Comme les révisions sont conçues pour ajouter une valeur numérique pour chaque élément du contenu envoyé, socialsync et Traiter ne sont pas pris en charge avec les révisions.

## API de révision {#section_xrh_wmh_21b}

Les API de révision permettent d'afficher l'évaluation moyenne des utilisateurs et les informations de ventilation de notation et l'utilisateur passe en revue l'activité des autres sections sur votre site.

[Évaluations et évaluations](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Le point de terminaison API d'amorçage permet à votre révision d'être lue par des moteurs de recherche tels que Google pour que le contenu et les mots-clés améliorent l'optimisation du moteur de recherche.

* **[!UICONTROL Average User Ratings]** L'API Classement moyen des utilisateurs récupère la note d'utilisateur moyenne d'un ou de plusieurs collections, ce qui vous permet de créer une visualisation de ces informations sur une page d'index ou d'ajouter à une page d'index de recherche.

* **[!UICONTROL Ratings Breakdown]** L'API Ventilation des notes récupère la ventilation de toutes les notes d'une collection de révisions spécifique et vous permet de créer une visualisation qui affiche le nombre de révisions associées à chaque évaluation.

* **[!UICONTROL User Reviews]** L'API des révisions utilisateur récupère les révisions les plus récentes pour un utilisateur spécifique. Cette activité peut être utilisée pour afficher les révisions d'un utilisateur sur sa page de profil publique.
