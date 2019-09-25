---
description: Modifiez les options de taille, de largeur et d’interaction de l’application de mappage.
seo-description: Modifiez les options de taille, de largeur et d’interaction de l’application de mappage.
seo-title: Personnalisations des cartes de fonctionnalités
solution: Experience Manager
title: Personnalisations des cartes de fonctionnalités
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# Personnalisations des cartes de fonctionnalités{#feature-card-customizations}

Modifiez les options de taille, de largeur et d’interaction de l’application de mappage.

<!-- 
r_feature_card_customization.dita
 -->

Les applications de cartes de caractéristiques comprennent uniquement des personnalisations standard :** [!UICONTROL Theme]**, couleur de marque, famille de polices et taille de police.

Vous pouvez personnaliser les cartes de caractéristiques à l’aide des éléments suivants :

* **[!UICONTROL Style]** et **[!UICONTROL Config]** les options pour toutes les applications dans le **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options standard **[!UICONTROL Style]** et **[!UICONTROL Config]** pour toutes les applications dans le **[!UICONTROL App Designer]**.

* Outils d’intégration. Pour plus d’informations sur la personnalisation des applications à l’aide des outils d’intégration, reportez-vous à la section Intégrations d’applications.
* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou votre site afin d’effectuer d’autres actions.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l’action.
   * **[!UICONTROL Require rights to display products]** Activez cette option pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu’un bouton Appel à l’action ne s’affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton Appel à l’action ne s’affiche pas avec le contenu, sauf si des droits sont accordés pour le contenu.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton Appel à l’action dans le module de contenu. Le libellé par défaut est "Acheter ces produits :".
   * **[!UICONTROL Call-to-action button text]** Personnalisez le texte du bouton Appel à l’action. Le texte par défaut est "Acheter maintenant".
   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher le **[!UICONTROL Photo]** et le **[!UICONTROL Product name]** avec le bouton Appel à l’action.
   * **[!UICONTROL Product URL referral tracking]** Activez cette option pour effectuer le suivi des références de cette application vers la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produit associée.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique au produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produit de niveau supérieur à utiliser pour filtrer les fichiers UGC. Permet `CTRL/Command + click` de sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l’application, mais balisé avec un ID de produit différent. Une fois que le contenu spécifique au produit de l’application s’affiche, Livefyre affiche le contenu d’autres produits et du contenu non associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié dans l’application avec d’autres ID de produit, puis au contenu publié dans l’application sans ID de produit.

