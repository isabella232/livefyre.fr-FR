---
description: Ces options s’appliquent à toutes les règles de flux provenant de tous les réseaux sociaux ou méthodes de publication.
title: Options des règles de diffusion en continu pour toutes les règles de diffusion en continu
exl-id: eff1a3cb-395f-4eb1-be93-f0f09bba95e2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---

# Options de règle de diffusion pour toutes les règles de diffusion{#stream-rule-options-for-all-stream-rules}

Ces options s’appliquent à toutes les règles de flux provenant de tous les réseaux sociaux ou méthodes de publication.

Fonctions de recherche des champs de texte et de mots-clés :

* Lorsque vous saisissez des mots-clés, Livefyre utilise automatiquement l’opérateur booléen **OR** pour les mots individuels. Par exemple, pour rechercher des publications avec le mot *gâteau* ou *recette*, saisissez *gâteau*, puis saisissez *recette* dans le champ **[!UICONTROL keyword]**.

* Vous pouvez rechercher des expressions exactes en entourant le texte exact de l’expression entre guillemets. Par exemple, pour rechercher l&#39;expression exacte *recette de gâteau*, entrez *&quot;recette de gâteau&quot;* dans le champ **[!UICONTROL keyword]**.

* Vous pouvez combiner les recherches de type Boolean et expression exacte dans une règle de flux continu. Par exemple, vous pouvez rechercher *cake*, *recipe* et *&quot;cake recipe&quot;* en saisissant chaque expression une par une.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Sélectionnez l’une des options suivantes :

   * **[!UICONTROL All Content.]** Autorisez tout contenu.
   * **[!UICONTROL Media Required.]** Autoriser uniquement le contenu avec des images et des vidéos. (Pour le contenu Instagram et Facebook, vous pouvez spécifier **[!UICONTROL Photos]** ou **[!UICONTROL Videos]** uniquement).

* **[!UICONTROL Language]**. Sélectionnez la langue dans laquelle effectuer la recherche. L’anglais est la langue par défaut.
* **[!UICONTROL Smart Tags]**. Choisissez les balises à utiliser pour identifier le contenu. Livefyre utilise la technologie de la vision par ordinateur pour identifier les photos et les vidéos avec des balises intelligentes spécifiques pour rendre cette recherche plus précise. Utilisez le modificateur **[!UICONTROL ANY]** pour filtrer le contenu dans le flux à l’aide d’une balise ou du modificateur **[!UICONTROL ALL]** pour filtrer le contenu dans le flux qui utilise toutes les balises. Utilisez le champ **[!UICONTROL Image contains none of these smart tags]** pour entrer des balises pour les photos contenant du contenu que vous ne souhaitez pas voir dans le flux. Cette option ne fonctionne pas pour le contenu de texte.

* **[!UICONTROL Products]**. Ajoutez des balises de produit pour qu’elles correspondent à la règle de flux avec les produits de votre catalogue de produits.
* **[!UICONTROL Premoderate]**. Sélectionnez l’une des options suivantes :

   * **[!UICONTROL On]**. Prémodérer tout le contenu de la règle entrante. Vous pouvez vue du contenu prémodéré à partir de la section Flux de ModQ. **[!UICONTROL On]** remplace les paramètres définis dans les paramètres de l’application.
   * **[!UICONTROL Off]**. Ne prémodérez aucun contenu de règle entrant. **[!UICONTROL Off]** remplace les paramètres définis dans les paramètres de l’application.
   * **[!UICONTROL Inherited (Off)]**. Utilisez les paramètres prémodérés du site (sous **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Sélectionnez l’une des options suivantes :
   * **[!UICONTROL Apply SAFE Rules]**. Appliquez toutes les règles SAFE à ce flux.
   * **[!UICONTROL Apply SAFE Rules for:]** Sélectionnez une ou plusieurs options pour appliquer des règles SAFE pour cette règle de flux.
   * **[!UICONTROL Disable SAFE Rules]**. N&#39;appliquez aucune règle SAFE à ce flux.

Pour connaître les options de règles de diffusion en continu spécifiques à un réseau social ou à un type de contenu, consultez la documentation suivante pour les types de contenu ou de réseau social respectifs :

* [Pages Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Courriel](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
