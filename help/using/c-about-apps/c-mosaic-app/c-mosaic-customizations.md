---
description: Modifiez les options de taille, de largeur et d'interaction de l'application Mosaic.
seo-description: Modifiez les options de taille, de largeur et d'interaction de l'application Mosaic.
seo-title: Personnalisations de Mosaic
solution: Experience Manager
title: Personnalisations de Mosaic
uuid: 4 e 226 d 68-f 517-4922-bc 25-655 d 524 d 7 d 52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisations de Mosaic{#mosaic-customizations}

Modifiez les options de taille, de largeur et d&#39;interaction de l&#39;application Mosaic.

Toutes les applications utilisent **[!UICONTROL Style]** et **[!UICONTROL Config]** options dans **[!UICONTROL App Designer]** la section. Voir Personnalisation des applications pour plus d&#39;informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans la **[!UICONTROL App Designer.]**

Vous pouvez personnaliser Mosaic à l&#39;aide des options supplémentaires suivantes dans l&#39;application Designer :

* **[!UICONTROL Content interaction]**. Définit le style avec lequel le nouveau contenu sera chargé sur la page :

   * **[!UICONTROL Hover Fade]** pour accéder à l&#39;autre côté d&#39;une carte lorsqu&#39;un visiteur du site passe la souris sur le contenu.
   * **[!UICONTROL Hover Flip]** pour retourner à l&#39;autre côté d&#39;une carte lorsqu&#39;un visiteur du site passe la souris sur le contenu.
   * **[!UICONTROL Click]** pour afficher l&#39;autre côté d&#39;une carte lorsqu&#39;un visiteur du site clique sur le contenu de la souris.

* **[!UICONTROL Number of Tiles to Load]**. Nombre de mosaïques à charger dans une mosaïque. Cela peut affecter l&#39;affichage de la sortie. Mosaic ne s&#39;affiche pas dans une grille, sauf si vous choisissez le nombre correct de mosaïques pour correspondre à la largeur du conteneur. Vous devrez peut-être les ajuster pour que la grille s&#39;affiche correctement.
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d&#39;origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l&#39;action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l&#39;action.

   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu&#39;un bouton Appel à l&#39;action ne s&#39;affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s&#39;affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l&#39;action ne s&#39;affiche pas avec le contenu, sauf si les droits d&#39;accès au contenu sont accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d&#39;afficher le bouton Appel à l&#39;action sur une mosaïque Filmstrip plutôt que d&#39;afficher le bouton Appel à l&#39;action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l&#39;utilisateur à cliquer sur la carte pour ouvrir le modal Call-to-Action.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l&#39;en-tête au-dessus du bouton Appel à l&#39;action dans le modal du contenu. La formulation par défaut est « Shop these products :  ».

   * **[!UICONTROL Call-to-action button text]** Personnalisez le texte sur le bouton Appel à l&#39;action. Le texte par défaut est « Buy Now » (Acheter maintenant).  » »

   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le **[!UICONTROL Photo]** bouton et **[!UICONTROL Product name]** le bouton Appel à l&#39;action.

   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.

   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l&#39;application vers la page de produit associée.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l&#39;application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l&#39;application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l&#39;application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l&#39;application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l&#39;application, Livefyre affiche le contenu d&#39;autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l&#39;application avec d&#39;autres ID de produit, puis le contenu publié dans l&#39;application sans ID de produit.

Voir [Options de Mosaic](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) pour en savoir plus sur la personnalisation d&#39;une mosaïque à l&#39;aide de Livefyre. js.
