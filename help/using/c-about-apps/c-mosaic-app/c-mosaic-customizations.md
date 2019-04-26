---
description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Mosaic.
seo-description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Mosaic.
seo-title: Personnalisations de Mosaic
solution: Experience Manager
title: Personnalisations de Mosaic
uuid: 4 e 226 d 68-f 517-4922-bc 25-655 d 524 d 7 d 52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisations de Mosaic{#mosaic-customizations}

Modifiez les options de taille, de largeur et d'interaction de l'application Mosaic.

Toutes les applications utilisent **[!UICONTROL Style]** et **[!UICONTROL Config]** options dans **[!UICONTROL App Designer]**la section. Voir Personnalisation des applications pour plus d'informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans la **[!UICONTROL App Designer.]**

Vous pouvez personnaliser Mosaic à l'aide des options supplémentaires suivantes dans l'application Designer :

* **[!UICONTROL Content interaction]**. Définit le style avec lequel le nouveau contenu sera chargé sur la page :

   * **[!UICONTROL Hover Fade]** pour accéder à l'autre côté d'une carte lorsqu'un visiteur du site passe la souris sur le contenu.
   * **[!UICONTROL Hover Flip]** pour retourner à l'autre côté d'une carte lorsqu'un visiteur du site passe la souris sur le contenu.
   * **[!UICONTROL Click]** pour afficher l'autre côté d'une carte lorsqu'un visiteur du site clique sur le contenu de la souris.

* **[!UICONTROL Number of Tiles to Load]**. Nombre de mosaïques à charger dans une mosaïque. Cela peut affecter l'affichage de la sortie. Mosaic ne s'affiche pas dans une grille, sauf si vous choisissez le nombre correct de mosaïques pour correspondre à la largeur du conteneur. Vous devrez peut-être les ajuster pour que la grille s'affiche correctement.
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d'origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l'action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l'action.

   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu'un bouton Appel à l'action ne s'affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s'affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l'action ne s'affiche pas avec le contenu, sauf si les droits d'accès au contenu sont accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d'afficher le bouton Appel à l'action sur une mosaïque Filmstrip plutôt que d'afficher le bouton Appel à l'action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l'utilisateur à cliquer sur la carte pour ouvrir le modal Call-to-Action.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l'en-tête au-dessus du bouton Appel à l'action dans le modal du contenu. La formulation par défaut est « Shop these products :  ».

   * **[!UICONTROL Call-to-action button text]** Personnalisez le texte sur le bouton Appel à l'action. Le texte par défaut est « Buy Now » (Acheter maintenant).  » »

   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le **[!UICONTROL Photo]** bouton et **[!UICONTROL Product name]** le bouton Appel à l'action.

   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.

   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l'application vers la page de produit associée.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l'application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l'application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l'application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l'application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l'application, Livefyre affiche le contenu d'autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l'application avec d'autres ID de produit, puis le contenu publié dans l'application sans ID de produit.

Voir [Options de Mosaic](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) pour en savoir plus sur la personnalisation d'une mosaïque à l'aide de Livefyre. js.
