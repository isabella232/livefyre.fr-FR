---
description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Map.
seo-description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Map.
seo-title: Personnalisations de carte de fonctionnalités
solution: Experience Manager
title: Personnalisations de carte de fonctionnalités
uuid: dd 43 c 076-027 f -42 c 8-be 2 e -7 d 863 d 4 e 3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# Personnalisations de carte de fonctionnalités{#feature-card-customizations}

Modifiez les options de taille, de largeur et d'interaction de l'application Map.

<!-- 
r_feature_card_customization.dita
 -->

Les applications de carte de fonctionnalités incluent uniquement des personnalisations standard : ** [!UICONTROL Theme]**, Couleur de marque, Famille de polices et Taille de police.

Vous pouvez personnaliser les cartes de fonctionnalités à l'aide de :

* **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]**la section. Voir Personnalisation des applications pour plus d'informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]**la section.

* Outils d'intégration. Voir Intégrations d'applications pour en savoir plus sur la personnalisation des applications à l'aide des outils d'intégration.
* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l'action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l'action.
   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu'un bouton Appel à l'action ne s'affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s'affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l'action ne s'affiche pas avec le contenu, sauf si les droits d'accès au contenu sont accordés.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l'en-tête au-dessus du bouton Appel à l'action dans le modal du contenu. La formulation par défaut est « Shop these products :  ».
   * **[!UICONTROL Call-to-action button text]** Personnalisez le texte sur le bouton Appel à l'action. Le texte par défaut est « Buy Now » (Acheter maintenant).  » »
   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le **[!UICONTROL Photo]** bouton et **[!UICONTROL Product name]** le bouton Appel à l'action.
   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l'application vers la page de produit associée.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l'application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l'application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Permet `CTRL/Command + click` de sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l'application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l'application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l'application, Livefyre affiche le contenu d'autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l'application avec d'autres ID de produit, puis le contenu publié dans l'application sans ID de produit.

