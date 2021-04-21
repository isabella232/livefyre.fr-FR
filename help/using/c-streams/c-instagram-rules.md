---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de l’Instagram.
title: Règles Instagram
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Règles Instagram{#instagram-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de l’Instagram.

>[!NOTE]
>
>Avant de créer un flux Instagram, vous devez ajouter au moins un compte Instagram à la section **[!UICONTROL Social Accounts]** de **[!UICONTROL Network Settings]**. Pour plus d’informations sur la configuration d’un compte Instagram, voir [A propos des comptes Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Créez des règles Instagram basées sur @mentions ou hashtag.

>[!NOTE]
>
>Toutes les règles Instagram nécessitent au moins un hashtag. Ajouter des mots-clés et un nom d&#39;utilisateur pour votre règle renverra le contenu qui inclut les deux entrées.

Pour créer des règles Instagram permettant d’extraire du contenu des flux Instagram dans votre application ou dossier, filtrez par :

* **[!UICONTROL Words]**

   * Saisissez **[!UICONTROL hashtags]** à inclure ou à exclure de votre flux Instagram. Si vous spécifiez des valeurs pour les deux champs **[!UICONTROL Contains]** et **[!UICONTROL Does not contain]**, les images qui contiennent le premier et ne contiennent pas le second seront renvoyées.

   * Par exemple, la saisie de **[!UICONTROL Contains]** mots-clés Giants, Posey et **[!UICONTROL Does not contain]** mot-clé Dodger renvoie toutes les publications qui comprennent le mot Giants ou Posey et n’incluent pas le mot Dodger.

      >[!NOTE]
      >
      >Instagram Rules renvoie les publications qui incluent le hashtag listé dans les commentaires de l’auteur, qui peut ne pas apparaître dans le flux.

* **[!UICONTROL Mentions]**

   * Saisissez **[!UICONTROL @mentions]** pour extraire dans le flux ou exclure du flux.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Vous devez avoir un compte professionnel Instagram configuré dans Livefyre pour utiliser la recherche Auteur dans une règle Instagram Stream. Pour plus d’informations sur la configuration des comptes d’entreprise Instagram dans Livefyre, voir [A propos des comptes Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Saisissez **[!UICONTROL @usernames]** pour extraire dans le flux. Le compte associé à **@username** doit être un compte professionnel Instagram.

   * Saisissez **@usernames** pour exclure du flux.

* **[!UICONTROL Additional Filters]**

   * Indiquez si vous souhaitez inclure **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** ou **[!UICONTROL Photos Only]** dans votre flux.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
