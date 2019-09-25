---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des flux RSS.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des flux RSS.
seo-title: Règles RSS
solution: Experience Manager
title: Règles RSS
uuid: 3c9e2069-bb85-41dc-8b35-6237642a538a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Règles RSS{#rss-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des flux RSS.

Les flux RSS se mettent à jour toutes les 5 minutes, à la recherche de contenu qui n'existe pas encore dans Livefyre à partir des 50 premiers éléments du flux. Livefyre ignore tout ce qui dépasse les 50 premiers éléments du flux.

Pour créer des règles RSS afin d’extraire du contenu des flux RSS dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL URL]** du flux RSS.
* **[!UICONTROL Include recent items.]** Si cette variable est définie sur :

   * **[!UICONTROL Enabled]**, Livefyre ajoute les 50 premiers éléments de contenu de votre flux au flux, quelle que soit la date de publication.
   * **[!UICONTROL Disabled]**, Livefyre ajoute les 50 premiers éléments de contenu de votre flux au flux avec une date de publication identique à la date de création des règles de flux ou ultérieure.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Extrayez les informations du lien de l’élément ou du code XML.

**Règles RSS**

Livefyre analyse les flux RSS en fonction des spécifications RSS suivantes :

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Media RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Flux Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre ne lit pas les flux qui ne respectent pas ces spécifications et leur contenu ne sera pas extrait dans votre flux. Utilisez le service de validation des flux WC3 pour vérifier la syntaxe de votre flux RSS et vous assurer qu’il est valide.

Pour obtenir des options de règle de diffusion en continu supplémentaires pour toutes les règles de diffusion en continu, voir Options de règle de [diffusion en continu pour toutes les règles](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de diffusion en continu.
