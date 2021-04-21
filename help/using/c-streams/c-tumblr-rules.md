---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Tumblr.
title: Règles Tumblr
exl-id: 5d49b266-6d1f-4ec2-8891-5e98fcab14a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '183'
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
