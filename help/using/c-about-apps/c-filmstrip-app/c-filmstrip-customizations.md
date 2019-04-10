---
description: valeur nulle
seo-description: valeur nulle
seo-title: Personnalisations du film fixe
solution: Experience Manager
title: Personnalisations du film fixe
uuid: 99 f 8 b 697-4 aa 3-4813-bcac-d 0 e 0 bdee 252 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Personnalisations du film fixe{#filmstrip-customizations}

Toutes les applications utilisent **[!UICONTROL Style]** et **[!UICONTROL Config]** options dans **[!UICONTROL App Designer]**la section. Voir Personnalisation des applications pour plus d'informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans la **[!UICONTROL App Designer.]**

Vous pouvez personnaliser le film fixe à l'aide des options supplémentaires suivantes dans l'application Designer :

* **[!UICONTROL Content fit]**. Choisissez **[!UICONTROL crop]** de recadrer le contenu pour remplir la carte ou **[!UICONTROL Aspect Ratio]** afficher une image entière dans la carte, qu'elle remplisse la carte entière ou non.
* **[!UICONTROL Tile Size]**. Entrez la taille des mosaïques en pixels.
* **[!UICONTROL Show Notifications]**. Choisissez d'afficher une notification pour le nouveau contenu au fur et à mesure de son flux dans l'application Film fixe.
* **[!UICONTROL Require rights]**. Activez cette option pour afficher uniquement le contenu avec un état de demande de droits « Accordé ».  » »
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d'origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.
* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l'action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez le bouton bascule pour afficher le bouton Appel à l'action.
   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu'un bouton Appel à l'action ne s'affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s'affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l'action ne s'affiche pas avec le contenu, sauf si les droits d'accès au contenu sont accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d'afficher le bouton Appel à l'action sur une mosaïque Filmstrip plutôt que d'afficher le bouton Appel à l'action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l'utilisateur à cliquer sur la carte pour ouvrir le modal call-to-action.
   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l'en-tête au-dessus du bouton Appel à l'action dans le modal du contenu. Le texte par défaut est « Shop these products :  ».
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l'action du modal du contenu. Le texte par défaut est « Buy Now :  ».
   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le **[!UICONTROL Photo]** bouton et **[!UICONTROL Product name]** le bouton Appel à l'action.

      >[!NOTE]
      >
      >Les boutons Photo et Nom de produit mettent en surbrillance le bleu lorsqu'ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l'application vers la page de produit associée.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l'application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l'application.
   * **[!UICONTROL Select product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l'application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l'application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l'application, Livefyre affiche le contenu d'autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l'application avec d'autres ID de produit, puis le contenu publié dans l'application sans ID de produit.

Pour [plus d'informations sur la personnalisation d'une bande film à l'aide de Livefyre. js, voir Options](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) du film fixe.

