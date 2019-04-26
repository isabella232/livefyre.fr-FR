---
description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Carrousel.
seo-description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Carrousel.
seo-title: Personnalisation d'un carrousel avec Studio
solution: Experience Manager
title: Personnalisation d'un carrousel avec Studio
uuid: 24 f 080 fc -37 bf -40 d 4-8 c 1 a-a 502 ee 8 ac 978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisation d'un carrousel avec Studio{#customize-a-carousel-using-studio}

Modifiez les options de taille, de largeur et d'interaction de l'application Carrousel.

Toutes les applications utilisent **[!UICONTROL Style]** et **[!UICONTROL Config]** options dans **[!UICONTROL App Designer]**la section. Voir Personnalisation des applications pour plus d'informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]**la section.

Vous pouvez personnaliser un carrousel à l'aide des options supplémentaires suivantes dans l'application Designer :

* **[!UICONTROL Max Number of Items]**

   Définit le nombre d'éléments à afficher dans le carrousel. La valeur par défaut est 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Pour les écrans d'ordinateur uniquement

   * Si le contenu est supérieur à 600 pixels, s'affiche horizontalement
   * Si le contenu est inférieur à 600 pixels, s'affiche verticalement
   * **Vertical.** Pour les écrans d'ordinateur ou les périphériques mobiles. Sur les périphériques mobiles, la carte s'adapte à la taille de l'écran.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l'action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez le bouton bascule pour afficher le bouton Appel à l'action.
   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu'un bouton Appel à l'action ne s'affiche pour le contenu.
   >[!NOTE]
   >
   >Le contenu s'affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l'action ne s'affiche pas avec le contenu, sauf si les droits d'accès au contenu sont accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d'afficher le bouton Appel à l'action sur une mosaïque plutôt que d'afficher le bouton Appel à l'action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l'utilisateur à cliquer sur la carte pour ouvrir le modal call-to-action.
   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l'en-tête au-dessus du bouton Appel à l'action dans le modal du contenu. Le texte par défaut est « Shop these products :  ».
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l'action du modal du contenu. Le texte par défaut est « Buy Now :  ».
   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le **[!UICONTROL Photo]** bouton et **[!UICONTROL Product name]** le bouton Appel à l'action.
   >[!NOTE]
   >
   >Les boutons Photo et Nom de produit mettent en surbrillance le bleu lorsqu'ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l'application vers la page de produit associée.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l'application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l'application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l'application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l'application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l'application, Livefyre affiche le contenu d'autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l'application avec d'autres ID de produit, puis le contenu publié dans l'application sans ID de produit.
