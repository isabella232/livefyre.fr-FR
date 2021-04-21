---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des règles YouTube.
title: Règles de YouTube
exl-id: 720a6fc6-d5de-4c78-a14e-51bced6e8dda
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Règles YouTube {#youtube-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des règles YouTube.

Créez des règles YouTube en fonction de l’utilisateur, du Canal ou de la liste de lecture.

Pour créer des règles YouTube afin d’extraire du contenu de YouTube dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL User]**
   * Saisissez la chaîne vanity pour un **[!UICONTROL User]** afin d’inclure des vidéos de l’utilisateur dans le flux.
   * Par exemple, si l’URL du flux utilisateur que vous souhaitez entrer est `https://www.youtube.com/user/livefyresupport`, il vous suffit de saisir `livefyresupport`.

* **[!UICONTROL Channel]**
   * Saisissez la chaîne vanity pour un **[!UICONTROL Channel]** afin d’inclure des vidéos d’un Canal dans le flux.
   * Par exemple, si l’URL du flux de Canal que vous souhaitez entrer est `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, entrez simplement `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Saisissez la chaîne vanity pour un **[!UICONTROL Playlist]** afin d’inclure des vidéos d’une liste de lecture dans le flux.
   * Par exemple, si l’URL du flux de liste de lecture que vous souhaitez saisir est `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, entrez simplement `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Si cette variable est définie sur :
   * **[!UICONTROL Enabled]**, Livefyre ajoute les 15 premiers éléments de contenu de votre flux au flux, quelle que soit la date de publication.
   * **[!UICONTROL Disabled]**, Livefyre ajoute les 15 premiers éléments de contenu de votre flux au flux avec une date de publication identique à la date de création de la règle de flux ou ultérieure.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
