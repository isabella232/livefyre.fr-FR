---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu d’Instagram.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu d’Instagram.
seo-title: Règles Instagram
title: Règles Instagram
uuid: 98108ddb-5710-4331-891b-7e1bb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Règles Instagram{#instagram-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu d’Instagram.

>[!NOTE]
>
>Avant de créer un flux Instagram, vous devez ajouter au moins un compte professionnel Instagram à la **[!UICONTROL Social Accounts]** section de **[!UICONTROL Network Settings]**. Pour plus d’informations sur la configuration d’un compte Instagram, voir [A propos des comptes](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)Instagram.

Créez des règles Instagram basées sur @mentions ou hashtag.

>[!NOTE]
>
>Toutes les règles Instagram nécessitent au moins un hashtag. L’ajout de mots-clés et d’un nom d’utilisateur pour votre règle renverra le contenu qui comprend les deux entrées.

Pour créer des règles Instagram pour extraire du contenu des flux Instagram dans votre application ou dossier, filtrez par :

* **[!UICONTROL Words]**

   * Entrez **[!UICONTROL hashtags]** pour être inclus ou exclu de votre flux Instagram. Si vous spécifiez des valeurs pour les deux **[!UICONTROL Contains]** et **[!UICONTROL Does not contain]** les champs, les images qui contiennent le premier et ne contiennent pas le second seront renvoyées.

   * Par exemple, la saisie de **[!UICONTROL Contains]** mots-clés Giants, Posey et **[!UICONTROL Does not contain]** le mot-clé Dodger renvoie toutes les publications qui incluent le mot Giants ou Posey, et ne comprennent pas le mot Dodger.

      >[!NOTE]
      >
      >Les règles Instagram renverront les publications qui incluent le hashtag répertorié dans les commentaires de l’auteur, qui peuvent ne pas apparaître dans le flux.

* **[!UICONTROL Mentions]**

   * Saisissez **[!UICONTROL @mentions]** pour extraire dans le flux ou excluez-le du flux.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Vous devez avoir un compte d’entreprise Instagram configuré dans Livefyre pour utiliser la recherche Auteur dans une règle de flux Instagram. Pour plus d’informations sur la configuration des comptes d’entreprise Instagram dans Livefyre, voir [A propos des comptes](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)Instagram.

   * Entrez **[!UICONTROL @usernames]** pour accéder au flux. Le compte associé à **@username** doit être un compte d’entreprise Instagram.

   * Entrez le **@usernames** à exclure du flux.

* **[!UICONTROL Additional Filters]**

   * Indiquez si vous souhaitez inclure **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** ou **[!UICONTROL Photos Only]** dans votre flux.

Pour obtenir des options de règle de diffusion en continu supplémentaires pour toutes les règles de diffusion en continu, voir Options de règle de [diffusion en continu pour toutes les règles](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de diffusion en continu.
