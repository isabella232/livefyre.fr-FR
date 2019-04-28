---
description: Modifiez les options de taille, de largeur et d'interaction de l'application Carrousel.
seo-description: Modifiez les options de taille, de largeur et d'interaction de l'application Carrousel.
seo-title: Personnalisation d'un carrousel avec Studio
solution: Experience Manager
title: Personnalisation d'un carrousel avec Studio
uuid: 24 f 080 fc -37 bf -40 d 4-8 c 1 a-a 502 ee 8 ac 978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisation d&#39;un carrousel avec Studio{#customize-a-carousel-using-studio}

Modifiez les options de taille, de largeur et d&#39;interaction de l&#39;application Carrousel.

Toutes les applications utilisent **[!UICONTROL Style]** et **[!UICONTROL Config]** options dans **[!UICONTROL App Designer]** la section. Voir Personnalisation des applications pour plus d&#39;informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]** la section.

Vous pouvez personnaliser un carrousel à l&#39;aide des options supplémentaires suivantes dans l&#39;application Designer :

* **[!UICONTROL Max Number of Items]**

   Définit le nombre d&#39;éléments à afficher dans le carrousel. La valeur par défaut est 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Pour les écrans d&#39;ordinateur uniquement

   * Si le contenu est supérieur à 600 pixels, s&#39;affiche horizontalement
   * Si le contenu est inférieur à 600 pixels, s&#39;affiche verticalement
   * **Vertical.** Pour les écrans d&#39;ordinateur ou les périphériques mobiles. Sur les périphériques mobiles, la carte s&#39;adapte à la taille de l&#39;écran.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l&#39;action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez le bouton bascule pour afficher le bouton Appel à l&#39;action.
   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu&#39;un bouton Appel à l&#39;action ne s&#39;affiche pour le contenu.
   >[!NOTE]
   >
   >Le contenu s&#39;affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l&#39;action ne s&#39;affiche pas avec le contenu, sauf si les droits d&#39;accès au contenu sont accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d&#39;afficher le bouton Appel à l&#39;action sur une mosaïque plutôt que d&#39;afficher le bouton Appel à l&#39;action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l&#39;utilisateur à cliquer sur la carte pour ouvrir le modal call-to-action.
   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l&#39;en-tête au-dessus du bouton Appel à l&#39;action dans le modal du contenu. Le texte par défaut est « Shop these products :  ».
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l&#39;action du modal du contenu. Le texte par défaut est « Buy Now :  ».
   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le **[!UICONTROL Photo]** bouton et **[!UICONTROL Product name]** le bouton Appel à l&#39;action.
   >[!NOTE]
   >
   >Les boutons Photo et Nom de produit mettent en surbrillance le bleu lorsqu&#39;ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l&#39;application vers la page de produit associée.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l&#39;application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l&#39;application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l&#39;application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l&#39;application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l&#39;application, Livefyre affiche le contenu d&#39;autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l&#39;application avec d&#39;autres ID de produit, puis le contenu publié dans l&#39;application sans ID de produit.
