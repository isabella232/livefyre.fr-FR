---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le
  contenu des flux RSS.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient
  le contenu des flux RSS.
seo-title: Règles RSS
solution: Experience Manager
title: Règles RSS
uuid: 3 c 9 e 2069-bb 85-41 dc -8 b 35-6237642 a 538 a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Règles RSS{#rss-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des flux RSS.

Les flux RSS mettent à jour toutes les 5 minutes, en recherchant le contenu qui n'existe pas déjà dans Livefyre à partir des 50 premiers éléments du flux. Livefyre ignore tout ce qui dépasse les 50 premiers éléments du flux.

Pour créer des règles RSS pour extraire du contenu des flux RSS vers votre application ou votre dossier, vous pouvez filtrer par :

* **[!UICONTROL URL]** du flux RSS.
* **[!UICONTROL Include recent items.]** Si cette valeur est définie sur :

   * **[!UICONTROL Enabled]**, Livefyre ajoute les 50 premiers éléments de contenu dans le flux au flux, quelle que soit la date de publication.
   * **[!UICONTROL Disabled]**, Livefyre ajoute les 50 premiers éléments de contenu dans votre flux au flux avec une date de publication identique à la date de création de la règle de diffusion en continu ou à une version ultérieure.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Extraire des informations à partir du lien d'élément ou du code XML.

**Règles RSS**

Livefyre analyse les flux RSS en fonction des spécifications RSS suivantes :

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Media RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Flux Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre ne lit pas les flux qui ne respectent pas ces spécifications et leur contenu ne sera pas extrait dans le flux. Utilisez WC 3 Feed Validation Service pour vérifier la syntaxe de votre flux RSS et vérifier qu'il est valide.

Pour obtenir des options de règle de diffusion en continu pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion en continu pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
