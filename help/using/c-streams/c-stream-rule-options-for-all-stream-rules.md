---
description: Ces options s'appliquent à toutes les règles de diffusion en continu
  issues de tous les réseaux sociaux ou méthodes de publication.
seo-description: Ces options s'appliquent à toutes les règles de diffusion en continu
  issues de tous les réseaux sociaux ou méthodes de publication.
seo-title: Options de règle de diffusion en continu pour toutes les règles de diffusion
  en continu
solution: Experience Manager
title: Options de règle de diffusion en continu pour toutes les règles de diffusion
  en continu
uuid: 4072 ee 83-31 e 7-4 de 6-918 c -134 b 8 b 8032 e 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Options de règle de diffusion en continu pour toutes les règles de diffusion en continu{#stream-rule-options-for-all-stream-rules}

Ces options s'appliquent à toutes les règles de diffusion en continu issues de tous les réseaux sociaux ou méthodes de publication.

Rechercher des fonctions pour les champs de texte et de mot-clé :

* Lorsque vous saisissez des mots-clés, Livefyre utilise automatiquement l'opérateur booléen **OU** lorsque pour des mots individuels. Par exemple, pour rechercher des publications avec le *gâteau* ou *la recette du mot*, saisissez *un gâteau*, puis entrez *une recette* dans **[!UICONTROL keyword]** le champ.

* Vous pouvez rechercher des phrases exactes en entourant exactement le texte de phrase entre guillemets. Par exemple, pour rechercher la recette exacte *de gâteau de phrase*, entrez *« recette de gâteau »* dans **[!UICONTROL keyword]** le champ.

* Vous pouvez combiner les recherches booléennes et exactes dans une règle de diffusion en continu. Par exemple, vous pouvez rechercher *un gâteau*, *une recette*et *une recette de gâteau* en saisissant chaque phrase un par un.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Sélectionnez l'une des options suivantes :

   * **[!UICONTROL All Content.]** Autoriser tout contenu.
   * **[!UICONTROL Media Required.]** Autorisez uniquement le contenu avec des images et des vidéos. (Pour le contenu Instagram et Facebook, vous pouvez spécifier **[!UICONTROL Photos]** ou **[!UICONTROL Videos]** uniquement).

* **[!UICONTROL Language]**. Choisissez la langue dans laquelle effectuer une recherche. L'anglais est la langue par défaut.
* **[!UICONTROL Smart Tags]**. Choisissez les balises à utiliser pour identifier le contenu. Livefyre utilise la technologie de visionnage informatique pour identifier les photos et les vidéos avec des balises intelligentes spécifiques pour rendre cette recherche plus précise. Utilisez **[!UICONTROL ANY]** le modificateur pour filtrer le contenu dans le flux à l'aide d'une balise ou d' **[!UICONTROL ALL]** un modificateur pour filtrer le contenu dans le flux qui utilise toutes les balises. Utilisez **[!UICONTROL Image contains none of these smart tags]** le champ pour saisir des balises pour les photos contenant du contenu que vous ne souhaitez pas dans le flux. Cette option ne fonctionne pas pour le contenu du texte.

* **[!UICONTROL Products]**. Ajoutez des balises de produit pour faire correspondre la règle de diffusion en continu avec les produits de votre catalogue de produits.
* **[!UICONTROL Premoderate]**. Sélectionnez l'une des options suivantes :

   * **[!UICONTROL On]**. Prémodérez tous les contenus de règle entrants. Vous pouvez afficher le contenu prémodéré à partir de la section Flux de modq. **[!UICONTROL On]** remplace les paramètres dans Paramètres d'application.
   * **[!UICONTROL Off]**. Ne prémodérez aucun contenu de règle entrant. **[!UICONTROL Off]** remplace les paramètres dans Paramètres d'application.
   * **[!UICONTROL Inherited (Off)]**. Utilisez les paramètres prémodérés du site (sous **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Sélectionnez l'une des options suivantes :
   * **[!UICONTROL Apply SAFE Rules]**. Appliquez toutes les règles SAFE à ce flux.
   * **[!UICONTROL Apply SAFE Rules for:]** Sélectionnez une ou plusieurs options pour appliquer des règles SAFE pour cette règle de diffusion en continu.
   * **[!UICONTROL Disable SAFE Rules]**. N'appliquez aucune règle SAFE à ce flux.

Pour les options de règle de diffusion en continu spécifiques à un réseau social ou un type de contenu, consultez la documentation suivante pour le réseau social ou le type de contenu correspondant :

* [Pages Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Courriel](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
