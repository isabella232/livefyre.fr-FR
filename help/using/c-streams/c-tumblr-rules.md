---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Tumblr.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Tumblr.
seo-title: Règles Tumblr
solution: Experience Manager
title: Règles Tumblr
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Règles Tumblr{#tumblr-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Tumblr.

Créez des règles Tumblr basées sur un blog Tumblr et filtrées par balise. Les flux Tumblr se mettent à jour toutes les 5 minutes, à la recherche de contenu qui n&#39;existe pas déjà dans Livefyre à partir des 20 premiers éléments du flux. Livefyre ignore tout au-delà des 20 premiers éléments du flux.

Pour créer des règles Tumblr permettant d’extraire du contenu de Tumblr dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL Blog]**

   * Entrez **[!UICONTROL Blog Name]** pour le blog Tumblr. Entrez l&#39;URL (*staff.tumblr.com*) ou le nom du blog (*staff*).

   * Incluez jusqu’à un **[!UICONTROL Tag]** pour filtrer les résultats par publications, y compris une balise donnée.

* **[!UICONTROL Include recent items.]** Si cette variable est définie sur :

   * **[!UICONTROL Enabled]**, Livefyre ajoute les 20 premiers éléments de contenu de votre flux au flux, quelle que soit la date de publication.
   * **[!UICONTROL Disabled]**, Livefyre ajoute les 20 premiers éléments de contenu de votre flux au flux avec une date de publication identique à la date de création des règles de flux ou ultérieure.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
