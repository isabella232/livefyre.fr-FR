---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le
  contenu de Tumblr.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient
  le contenu de Tumblr.
seo-title: Règles Tumblr
solution: Experience Manager
title: Règles Tumblr
uuid: fe 9601 ab-aa 5 e -48 c 6-a 5 bf -5543 c 179 cb 90
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Règles Tumblr{#tumblr-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Tumblr.

Créez des règles Tumblr basées sur un blog Tumblr et filtrées par balise. Les flux Tumblr mettent à jour toutes les 5 minutes, en recherchant le contenu qui n'existe pas déjà dans Livefyre à partir des 20 premiers éléments du flux. Livefyre ignore tout ce qui dépasse les 20 premiers éléments du flux.

Pour créer des règles Tumblr pour extraire du contenu de Tumblr dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL Blog]**

   * Entrez le **[!UICONTROL Blog Name]** blog de Tumblr. Saisissez l'URL (*staff.tumblr.com*) ou le nom du blog (*personnel*).

   * Incluez jusqu'à un **[!UICONTROL Tag]** pour filtrer les résultats par publications, y compris une balise donnée.

* **[!UICONTROL Include recent items.]** Si cette valeur est définie sur :

   * **[!UICONTROL Enabled]**, Livefyre ajoute les 20 premiers éléments de contenu dans le flux au flux, quelle que soit la date de publication.
   * **[!UICONTROL Disabled]**, Livefyre ajoute les 20 premiers éléments de contenu dans votre flux au flux avec une date de publication identique à la date de création de la règle de diffusion en continu ou à une version ultérieure.

Pour obtenir des options de règle de diffusion en continu pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion en continu pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
