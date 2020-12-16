---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu d’Instagram.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu d’Instagram.
seo-title: Règles Instagram
title: Règles Instagram
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Règles Instagram{#instagram-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu d’Instagram.

>[!NOTE]
>
>Avant de créer un flux Instagram, vous devez ajouter au moins un compte professionnel Instagram à la section **[!UICONTROL Social Accounts]** de **[!UICONTROL Network Settings]**. Pour plus d&#39;informations sur la configuration d&#39;un compte Instagram, voir [A propos des comptes Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Créez des règles Instagram basées sur @mentions ou hashtag.

>[!NOTE]
>
>Toutes les règles Instagram nécessitent au moins un hashtag. Ajouter des mots-clés et un nom d&#39;utilisateur pour votre règle renverra le contenu qui inclut les deux entrées.

Pour créer des règles Instagram pour extraire du contenu des flux Instagram dans votre application ou dossier, filtrez par :

* **[!UICONTROL Words]**

   * Saisissez **[!UICONTROL hashtags]** à inclure dans votre flux Instagram ou à exclure de celui-ci. Si vous spécifiez des valeurs pour les deux champs **[!UICONTROL Contains]** et **[!UICONTROL Does not contain]**, les images qui contiennent le premier et ne contiennent pas le second seront renvoyées.

   * Par exemple, la saisie de **[!UICONTROL Contains]** mots-clés Giants, Posey et **[!UICONTROL Does not contain]** mot-clé Dodger renvoie toutes les publications qui comprennent le mot Giants ou Posey et n’incluent pas le mot Dodger.

      >[!NOTE]
      >
      >Les règles Instagram renverront les publications qui incluent le hashtag répertorié dans les commentaires de l’auteur, qui peuvent ne pas apparaître dans le flux.

* **[!UICONTROL Mentions]**

   * Saisissez **[!UICONTROL @mentions]** pour extraire dans le flux ou exclure du flux.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Vous devez avoir un compte professionnel Instagram configuré dans Livefyre pour utiliser la recherche Auteur dans une règle de flux Instagram. Pour plus d&#39;informations sur la configuration de comptes d&#39;entreprise Instagram dans Livefyre, voir [A propos des comptes Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Saisissez **[!UICONTROL @usernames]** pour extraire dans le flux. Le compte associé à **@username** doit être un compte professionnel Instagram.

   * Saisissez **@usernames** pour exclure du flux.

* **[!UICONTROL Additional Filters]**

   * Indiquez si vous souhaitez inclure **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** ou **[!UICONTROL Photos Only]** dans votre flux.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
