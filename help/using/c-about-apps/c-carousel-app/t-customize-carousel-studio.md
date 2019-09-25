---
description: Modifiez les options de taille, de largeur et d’interaction de l’application Carrousel.
seo-description: Modifiez les options de taille, de largeur et d’interaction de l’application Carrousel.
seo-title: Personnalisation d’un carrousel à l’aide de Studio
solution: Experience Manager
title: Personnalisation d’un carrousel à l’aide de Studio
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisation d’un carrousel à l’aide de Studio{#customize-a-carousel-using-studio}

Modifiez les options de taille, de largeur et d’interaction de l’application Carrousel.

Toutes les applications utilisent **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de la **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options standard **[!UICONTROL Style]** et **[!UICONTROL Config]** pour toutes les applications dans le **[!UICONTROL App Designer]**.

Vous pouvez personnaliser un carrousel à l’aide des options supplémentaires suivantes dans App Designer :

* **[!UICONTROL Max Number of Items]**

   Définit le nombre d’éléments à afficher dans le carrousel. La valeur par défaut est 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Pour les écrans d’ordinateur uniquement

   * Si le contenu dépasse 600 pixels, s’affiche horizontalement.
   * Si le contenu est inférieur à 600 pixels, s’affiche verticalement.
   * **Vertical.** Pour les écrans d’ordinateur ou les périphériques mobiles. Sur les périphériques mobiles, la carte se réduit pour s’adapter à la taille de l’écran.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou votre site afin d’effectuer d’autres actions.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton d’appel à l’action.
   * **[!UICONTROL Require rights to display products]** Activez cette option pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu’un bouton d’appel à l’action ne s’affiche pour le contenu.
   >[!NOTE]
   >
   >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton d’appel à l’action ne s’affiche pas avec le contenu, sauf si des droits sont accordés pour le contenu.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d’afficher le bouton d’appel à l’action sur une mosaïque au lieu d’afficher le bouton d’appel à l’action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l’utilisateur à cliquer sur la carte pour ouvrir le mode d’appel à l’action.
   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton Appel à l’action dans le module de contenu. Le texte par défaut est "Acheter ces produits :".
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l’action du module de contenu. Le texte par défaut est "Acheter maintenant :".
   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher le **[!UICONTROL Photo]** et le **[!UICONTROL Product name]** avec le bouton Appel à l’action.
   >[!NOTE]
   >
   >Les boutons Photo et Nom du produit sont tous deux en bleu lorsqu’ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Activez cette option pour effectuer le suivi des références de cette application vers la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produit associée.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique au produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produit de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez Ctrl/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l’application, mais balisé avec un ID de produit différent. Une fois que le contenu spécifique au produit de l’application s’affiche, Livefyre affiche le contenu d’autres produits et du contenu non associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié dans l’application avec d’autres ID de produit, puis au contenu publié dans l’application sans ID de produit.
