---
description: Modifiez les options de taille, de largeur et d’interaction de l’application Mosaic.
seo-description: Modifiez les options de taille, de largeur et d’interaction de l’application Mosaic.
seo-title: Personnalisations de Mosaic
solution: Experience Manager
title: Personnalisations de Mosaic
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisations de Mosaic{#mosaic-customizations}

Modifiez les options de taille, de largeur et d’interaction de l’application Mosaic.

Toutes les applications utilisent **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de la **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options standard **[!UICONTROL Style]** et **[!UICONTROL Config]** pour toutes les applications dans la section **[!UICONTROL App Designer.]**

Vous pouvez personnaliser Mosaic à l’aide des options supplémentaires suivantes dans App Designer :

* **[!UICONTROL Content interaction]**. Définit le style avec lequel le nouveau contenu sera chargé sur la page :

   * **[!UICONTROL Hover Fade]** pour qu’un visiteur de site passe de la souris sur le contenu de l’autre côté d’une carte.
   * **[!UICONTROL Hover Flip]** pour basculer vers l’autre côté d’une carte lorsqu’un visiteur du site passe sa souris sur le contenu.
   * **[!UICONTROL Click]** pour afficher l’autre côté d’une carte lorsqu’un visiteur du site clique sur son contenu.

* **[!UICONTROL Number of Tiles to Load]**. Nombre de mosaïques à charger dans une mosaïque. Cela peut affecter l’affichage de la sortie. Mosaic ne s’affiche pas dans une grille, sauf si vous choisissez le nombre correct de mosaïques correspondant à la largeur du conteneur. Vous devrez peut-être les ajuster pour que la grille s’affiche correctement.
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau social d’origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou votre site afin d’effectuer d’autres actions.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l’action.

   * **[!UICONTROL Require rights to display products]** Activez cette option pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu’un bouton Appel à l’action ne s’affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton Appel à l’action ne s’affiche pas avec le contenu, sauf si des droits sont accordés pour le contenu.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d’afficher le bouton d’appel à l’action sur une mosaïque de film fixe au lieu d’afficher le bouton d’appel à l’action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l’utilisateur à cliquer sur la carte pour ouvrir le mode Appel à l’action.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton Appel à l’action dans le module de contenu. Le libellé par défaut est "Acheter ces produits :".

   * **[!UICONTROL Call-to-action button text]** Personnalisez le texte du bouton Appel à l’action. Le texte par défaut est "Acheter maintenant".

   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher le **[!UICONTROL Photo]** et le **[!UICONTROL Product name]** avec le bouton Appel à l’action.

   * **[!UICONTROL Product URL referral tracking]** Activez cette option pour effectuer le suivi des références de cette application vers la page de produit associée.

   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produit associée.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique au produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produit de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez Ctrl/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l’application, mais balisé avec un ID de produit différent. Une fois que le contenu spécifique au produit de l’application s’affiche, Livefyre affiche le contenu d’autres produits et du contenu non associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié dans l’application avec d’autres ID de produit, puis au contenu publié dans l’application sans ID de produit.

Pour plus d’informations sur la personnalisation d’une mosaïque à l’aide de Livefyre.js, reportez-vous à la section Options [](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) de mosaïque.
