---
description: valeur nulle
seo-description: valeur nulle
seo-title: Personnalisations du film strip
solution: Experience Manager
title: Personnalisations du film strip
uuid: 99f8b697-4aa3-4813-bcac-d0e0bdee252d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---


# Personnalisations du film strip{#filmstrip-customizations}

Toutes les applications utilisent les options **[!UICONTROL Style]** et **[!UICONTROL Config]** dans **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options **[!UICONTROL Style]** et **[!UICONTROL Config]** standard pour toutes les applications dans le **[!UICONTROL App Designer.]**

Vous pouvez personnaliser le film strip à l’aide des options supplémentaires suivantes dans App Designer :

* **[!UICONTROL Content fit]**. Choisissez **[!UICONTROL crop]** pour recadrer le contenu pour remplir la carte ou **[!UICONTROL Aspect Ratio]** pour afficher une image entière dans la carte, qu’elle remplisse la carte ou non.
* **[!UICONTROL Tile Size]**. Entrez la taille des mosaïques en pixels.
* **[!UICONTROL Show Notifications]**. Choisissez si vous souhaitez afficher une notification pour le nouveau contenu au fur et à mesure qu’il est diffusé dans l’application Filmstrip.
* **[!UICONTROL Require rights]**. Activez cette option pour n’afficher que le contenu dont l’état de demande de droits est &quot;Octroyé&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d&#39;origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.
* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton d’appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou votre site pour toute action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton d’appel à l’action.
   * **[!UICONTROL Require rights to display products]** Activez cette option pour que le propriétaire du contenu ait accordé des droits sur le contenu avant qu’un bouton d’appel à l’action ne s’affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton d’appel à l’action ne s’affiche pas avec le contenu à moins que des droits pour le contenu ne soient accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d’afficher le bouton d’appel à l’action sur une mosaïque de bande de film au lieu d’afficher le bouton d’appel à l’action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l’utilisateur à cliquer sur la carte pour ouvrir le module d’appel à l’action.
   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton d’appel à l’action dans le module de contenu. Le texte par défaut est &quot;Acheter ces produits :&quot;.
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton d’appel à l’action dans le module de contenu. Le texte par défaut est &quot;Acheter maintenant :&quot;.
   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher le  **[!UICONTROL Photo]** et le  **[!UICONTROL Product name]** avec le bouton d’appel à l’action.

      >[!NOTE]
      >
      >Les boutons Photo et Nom du produit apparaissent en bleu lorsqu’ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez la bascule sur Activé pour effectuer le suivi des références depuis cette application vers la page de produits associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produits associée.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique à chaque produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié sur l’application, mais balisé avec un autre ID de produit. Une fois que le contenu spécifique à un produit pour l’application s’affiche, Livefyre affiche le contenu pour d’autres produits et le contenu qui n’est pas associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié sur l’application avec d’autres ID de produit, puis au contenu publié sur l’application sans ID de produit.

Pour plus d’informations sur la personnalisation d’une bande de film à l’aide de Livefyre.js, voir [Options de bande de film](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

