---
description: Ces options s’appliquent à toutes les règles de flux de tous les réseaux sociaux ou méthodes de publication.
seo-description: Ces options s’appliquent à toutes les règles de flux de tous les réseaux sociaux ou méthodes de publication.
seo-title: Options des règles de diffusion en continu pour toutes les règles de diffusion en continu
solution: Experience Manager
title: Options des règles de diffusion en continu pour toutes les règles de diffusion en continu
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2

---


# Options des règles de diffusion en continu pour toutes les règles de diffusion en continu{#stream-rule-options-for-all-stream-rules}

Ces options s’appliquent à toutes les règles de flux de tous les réseaux sociaux ou méthodes de publication.

Fonctions de recherche de texte et de champs de mot-clé :

* Lorsque vous saisissez des mots-clés, Livefyre utilise automatiquement l’opérateur booléen **OU** quand pour des mots individuels. Par exemple, pour rechercher des publications avec le mot *gâteau* ou *recette*, saisissez *gâteau*, puis saisissez *recette dans le champ .***[!UICONTROL keyword]**

* You can search for exact phrases by surrounding the exact phrase text in quotes. For example, to search for the exact phrase *cake recipe*, enter *"cake recipe"* in the **[!UICONTROL keyword]** field.

* Vous pouvez combiner les recherches de type Boolean et expression exacte dans une règle de flux continu. Par exemple, vous pouvez rechercher *gâteau*, *recette* et *"recette de gâteau"* en saisissant chaque expression une par une.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Sélectionnez l’une des options suivantes :

   * **[!UICONTROL All Content.]** Autorisez tout contenu.
   * **[!UICONTROL Media Required.]** Autorisez uniquement le contenu avec des images et des vidéos. (Pour le contenu Instagram et Facebook, vous pouvez spécifier **[!UICONTROL Photos]** ou **[!UICONTROL Videos]** uniquement).

* **[!UICONTROL Language]**. Choisissez la langue dans laquelle effectuer la recherche. L’anglais est la langue par défaut.
* **[!UICONTROL Smart Tags]**. Choisissez les balises à utiliser pour identifier le contenu. Livefyre utilise la technologie de la vision par ordinateur pour identifier les photos et les vidéos avec des balises intelligentes spécifiques pour rendre cette recherche plus précise. Utilisez le **[!UICONTROL ANY]** modificateur pour filtrer le contenu dans le flux à l’aide d’une balise quelconque ou du **[!UICONTROL ALL]** modificateur pour filtrer le contenu dans le flux qui utilise toutes les balises. Utilisez le **[!UICONTROL Image contains none of these smart tags]** champ pour entrer des balises pour les photos contenant le contenu que vous ne souhaitez pas dans le flux. Cette option ne fonctionne pas pour le contenu de texte.

* **[!UICONTROL Products]**. Ajoutez des balises de produit pour qu’elles correspondent à la règle de flux avec les produits de votre catalogue de produits.
* **[!UICONTROL Premoderate]**. Sélectionnez l’une des options suivantes :

   * **[!UICONTROL On]**. Prémodérez tout le contenu des règles entrantes. Vous pouvez afficher le contenu prémodéré dans la section Flux de ModQ. **[!UICONTROL On]** remplace les paramètres dans les paramètres de l’application.
   * **[!UICONTROL Off]**. Ne prémodérez aucun contenu de règle entrant. **[!UICONTROL Off]** overrides the settings in App Settings.
   * **[!UICONTROL Inherited (Off)]**. Utilisez les paramètres prémodérés du site (sous **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Select one of the following:
   * **[!UICONTROL Apply SAFE Rules]**. Apply all SAFE Rules to this stream.
   * **[!UICONTROL Apply SAFE Rules for:]** Select one or more of the options to apply SAFE Rules for this stream rule.
   * **[!UICONTROL Disable SAFE Rules]**. Do not apply any SAFE Rules to this stream.

For Stream rule options specific to a social network or content type, see the following documentation for the respective social network or content type:

* [Pages Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Courriel](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
