---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des flux RSS.
title: Règles RSS
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Règles RSS{#rss-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des flux RSS.

Les flux RSS se mettent à jour toutes les 5 minutes, à la recherche de contenu qui n&#39;existe pas encore dans Livefyre à partir des 50 premiers éléments du flux. Livefyre ignore tout au-delà des 50 premiers éléments du flux.

Pour créer des règles RSS afin d’extraire du contenu des flux RSS dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL URL]** du flux RSS.
* **[!UICONTROL Include recent items.]** Si cette variable est définie sur :

   * **[!UICONTROL Enabled]**, Livefyre ajoute les 50 premiers éléments de contenu de votre flux au flux, quelle que soit la date de publication.
   * **[!UICONTROL Disabled]**, Livefyre ajoute les 50 premiers éléments de contenu de votre flux au flux avec une date de publication identique à la date de création des règles de flux ou ultérieure.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Extrayez les informations du lien de l’élément ou du code XML.

**Règles RSS**

Livefyre analyse les flux RSS en fonction des flux RSS suivants :

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Media RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Flux Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre ne lit pas les flux qui ne respectent pas ces spécifications et leur contenu ne sera pas extrait dans votre flux. Utilisez le service de validation de flux WC3 pour vérifier la syntaxe de votre flux RSS et vous assurer qu’il est valide.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
