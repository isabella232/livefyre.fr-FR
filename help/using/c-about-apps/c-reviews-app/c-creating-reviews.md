---
description: Les révisions offrent une grande variété de personnalisations, ce qui vous permet de créer une application de révision qui correspond à vos besoins et à votre marque.
seo-description: Les révisions offrent une grande variété de personnalisations, ce qui vous permet de créer une application de révision qui correspond à vos besoins et à votre marque.
seo-title: Création d'une application de révision
solution: Experience Manager
title: Création d'une application de révision
uuid: 6 caeafe 7-c 04 e -484 e-b 02 f -98 dc 6 d 9 b 3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création d&#39;une application de révision{#creating-a-reviews-app}

Les révisions offrent une grande variété de personnalisations, ce qui vous permet de créer une application de révision qui correspond à vos besoins et à votre marque.

Utilisez l&#39;application de révision en l&#39;incorporant personnalisée sur votre site en tant qu&#39;application JS. Vous ne pouvez pas créer une application de révision dans Livefyre Studio. Pour créer une application de révision sur votre site, voir [Révision de l&#39;intégration](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Évaluations {#section_hs5_c4h_21b}

Les évaluations sont la valeur numérique que vos utilisateurs attribuent à la révision. Chaque révision doit inclure une évaluation, qui s&#39;affiche par défaut sous la forme d&#39;un système 5 étoiles. (Alors que les évaluations s&#39;affichent sous la forme 0.5 - 5 dans l&#39;application, Livefyre stocke un rapport X/100 dans le serveur principal, de sorte que 1 étoile soit 20/100 et 2 étoiles est de 40/100. Ce rapport s&#39;affiche lors de l&#39;affichage des révisions dans Studio.)

L&#39;échelle d&#39;évaluation de 0,5 à 5 peut être configurée jusqu&#39;à 100, avec une note de moitié également disponible.

Pour plus d&#39;informations, voir le champ maxrating pour l&#39;objet Reviews convconfig.

## Style de l&#39;icône de notation {#section_cqn_c4h_21b}

Les icônes d&#39;évaluation peuvent être personnalisées en fonction de votre marque et de votre style.

Pour plus d&#39;informations, **[!UICONTROL Configure Star Ratings]** consultez la section Révision de la personnalisation.

## Dimensions de notation {#section_cnx_snh_21b}

Les dimensions d&#39;évaluation sont les catégories sur lesquelles vos réviseurs évaluent votre produit ou service. Les exemples de dimensions d&#39;évaluation sont les « performances », « conception », « coût », « général » ou toute autre catégorie choisie.

Par défaut, vous pouvez afficher une dimension d&#39;évaluation globale, mais vous pouvez définir et implémenter plusieurs dimensions de notation, comme indiqué dans l&#39;exemple ci-dessous.

Pour plus d&#39;informations, voir le champ ratingdimensions sous Révision des métadonnées de collection.

## Examiner les champs de texte {#section_xcm_4nh_21b}

Vous pouvez également inclure des champs de texte supplémentaires sur le produit ou l&#39;expérience en cours de révision. (Par exemple, les champs de texte peuvent inclure les avantages - et - inconvénients ou Ne pas manquer.) Le numéro, le titre et le texte par défaut du champ sont personnalisables. Les utilisateurs devront remplir tous les champs de texte, ainsi que le titre, le corps et la note de révision afin de publier leur révision. Il est impossible d&#39;inclure des champs de texte facultatifs.

Pour plus d&#39;informations, voir le champ ratingdimensions pour les métadonnées de la collection de révisions.

## Résumé de révision {#section_ysz_lnh_21b}

Par défaut, une section de résumé s&#39;affiche en haut de l&#39;application de révision. Cette section comprend une visualisation de la note d&#39;utilisateur moyenne et de la ventilation d&#39;évaluation pour la collection des révisions, affichant des nombres entiers uniquement. Cette section est en lecture seule et peut être masquée si vous le souhaitez.

Pour plus d&#39;informations, voir le champ ratingsummaryenabled pour l&#39;objet Reviews convconfig.

## Filtre des messages indésirables et du profilage {#section_hcm_jnh_21b}

Le texte du titre et du corps d&#39;une révision est transmis via notre filtre de messages indésirables et le filtre de profilité dès que la révision est publiée.

## Personnalisation du texte {#section_tjf_hnh_21b}

Les chaînes de texte, y compris les info-bulles et les étiquettes, peuvent être personnalisées pour la langue ou pour s&#39;adapter à votre marque.

## Réponse à une révision {#section_yng_fnh_21b}

Les utilisateurs peuvent répondre à leur propre révision ou à la révision d&#39;un autre utilisateur dans chaque collection de révisions. Seuls les utilisateurs connectés peuvent publier une réponse à une révision.

L&#39;option permettant aux utilisateurs de répondre à une révision est activée dans Studio. Les propriétaires peuvent activer ce paramètre pour le niveau réseau, site ou collection. Les modérateurs peuvent uniquement activer ce paramètre pour leurs collections.

## Socialsync et traitement {#section_llh_2nh_21b}

Comme les révisions sont conçues pour ajouter une valeur numérique pour chaque élément du contenu envoyé, socialsync et Traiter ne sont pas pris en charge avec les révisions.

## API de révision {#section_xrh_wmh_21b}

Les API de révision permettent d&#39;afficher l&#39;évaluation moyenne des utilisateurs et les informations de ventilation de notation et l&#39;utilisateur passe en revue l&#39;activité des autres sections sur votre site.

[Évaluations et évaluations](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Le point de terminaison API d&#39;amorçage permet à votre révision d&#39;être lue par des moteurs de recherche tels que Google pour que le contenu et les mots-clés améliorent l&#39;optimisation du moteur de recherche.

* **[!UICONTROL Average User Ratings]** L&#39;API Classement moyen des utilisateurs récupère la note d&#39;utilisateur moyenne d&#39;un ou de plusieurs collections, ce qui vous permet de créer une visualisation de ces informations sur une page d&#39;index ou d&#39;ajouter à une page d&#39;index de recherche.

* **[!UICONTROL Ratings Breakdown]** L&#39;API Ventilation des notes récupère la ventilation de toutes les notes d&#39;une collection de révisions spécifique et vous permet de créer une visualisation qui affiche le nombre de révisions associées à chaque évaluation.

* **[!UICONTROL User Reviews]** L&#39;API des révisions utilisateur récupère les révisions les plus récentes pour un utilisateur spécifique. Cette activité peut être utilisée pour afficher les révisions d&#39;un utilisateur sur sa page de profil publique.
