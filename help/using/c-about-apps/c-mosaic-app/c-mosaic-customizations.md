---
description: Modifiez les options de taille, de largeur et d’interaction de l’application Mosaic.
seo-description: Modifiez les options de taille, de largeur et d’interaction de l’application Mosaic.
seo-title: Personnalisations de mosaïque
solution: Experience Manager
title: Personnalisations de mosaïque
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Personnalisations de mosaïque{#mosaic-customizations}

Modifiez les options de taille, de largeur et d’interaction de l’application Mosaic.

Toutes les applications utilisent les options **[!UICONTROL Style]** et **[!UICONTROL Config]** dans **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options **[!UICONTROL Style]** et **[!UICONTROL Config]** standard pour toutes les applications dans le **[!UICONTROL App Designer.]**

Vous pouvez personnaliser Mosaic à l’aide des options supplémentaires suivantes dans App Designer :

* **[!UICONTROL Content interaction]**. Définit le style de chargement du nouveau contenu sur la page :

   * **[!UICONTROL Hover Fade]** pour afficher un fondu vers l’autre côté d’une carte lorsqu’un visiteur de site passe sa souris sur le contenu.
   * **[!UICONTROL Hover Flip]** pour basculer vers l’autre côté d’une carte lorsqu’un visiteur de site passe sa souris sur le contenu.
   * **[!UICONTROL Click]** pour afficher l’autre côté d’une carte lorsqu’un visiteur de site clique sur sa souris sur le contenu.

* **[!UICONTROL Number of Tiles to Load]**. Nombre de mosaïques à charger dans une mosaïque. Cela peut avoir une incidence sur l’affichage de la sortie. La mosaïque ne s’affiche pas dans une grille à moins que vous ne choisissiez le nombre correct de mosaïques pour correspondre à la largeur du conteneur. Vous devrez peut-être les ajuster pour que la grille s&#39;affiche correctement.
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d&#39;origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour toute action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l&#39;action.

   * **[!UICONTROL Require rights to display products]** Activez cette option pour que le propriétaire du contenu ait accordé des droits sur le contenu avant qu’un bouton Appel à l’action ne s’affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton Appel à l’action ne s’affiche pas avec le contenu à moins que des droits pour le contenu ne soient accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d’afficher le bouton d’appel à l’action sur une mosaïque de bande de film au lieu d’afficher le bouton d’appel à l’action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l&#39;utilisateur à cliquer sur la carte pour ouvrir le module Appel à l&#39;action.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton Appel à l’action dans le module de contenu. La formulation par défaut est &quot;Acheter ces produits :&quot;.

   * **[!UICONTROL Call-to-action button text]** Personnalisez le texte du bouton Appel à l’action. Le texte par défaut est &quot;Acheter maintenant&quot;.

   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher le  **[!UICONTROL Photo]** et le  **[!UICONTROL Product name]** avec le bouton Appel à l&#39;action.

   * **[!UICONTROL Product URL referral tracking]** Basculez la bascule sur Activé pour effectuer le suivi des références depuis cette application vers la page de produits associée.

   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produits associée.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique à chaque produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié sur l’application, mais balisé avec un autre ID de produit. Une fois que le contenu spécifique à un produit pour l’application s’affiche, Livefyre affiche le contenu pour d’autres produits et le contenu qui n’est pas associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié sur l’application avec d’autres ID de produit, puis au contenu publié sur l’application sans ID de produit.

Voir [Options de mosaïque](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) pour en savoir plus sur la personnalisation d’une mosaïque à l’aide de Livefyre.js.
