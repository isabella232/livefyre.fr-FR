---
description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Mur multimédia.
seo-description: Modifiez les options de taille, de largeur et d'interaction de l'application
  Mur multimédia.
seo-title: Personnalisations du mur multimédia
solution: Experience Manager
title: Personnalisations du mur multimédia
uuid: 79 aecd 92-3937-4 bb 4-a 1 a 6-b 090 fb 39 afb 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Personnalisations du mur multimédia{#media-wall-customizations}

Modifiez les options de taille, de largeur et d'interaction de l'application Mur multimédia.



Les murs de médias sont des images actives et d'autres contenus dans un mur social en temps réel, qui visualisent toutes les activités entourant un événement.

Si cette option est activée, les utilisateurs peuvent publier du texte, des images ou des vidéos directement dans cette application. Les types de fichiers pris en charge sont les suivants :

* Image : JPEG, GIF, PNG
* Vidéo : Quicktime/MOV, MP 4, MPEG, webm
* Audio : WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Définit le nombre initial d'éléments de contenu affichés.

* **[!UICONTROL Load content with animation.]** Activez cette option pour charger le mur multimédia sur une page avec une animation. Désactivez cette option pour charger le mur multimédia sur une page sans animation.
* **[!UICONTROL Number of columns.]** Définissez le nombre de colonnes pour le mur multimédia. Le nombre de colonnes reste le même, quelle que soit la taille de la fenêtre ou du navigateur. Si vous sélectionnez Auto, le nombre de colonnes s'ajuste pour afficher un nombre optimisé de colonnes pour la taille de l'écran.
* **[!UICONTROL Fit content to width]**. Lorsque cette option est désactivée, le contenu est recadré sur un carré. Activez cette option pour afficher une image entière dans la carte, qu'elle remplisse la totalité de la carte ou non.
* **[!UICONTROL Include content modal]**

   Permet aux utilisateurs de cliquer sur une photo dans le flux pour l'ouvrir dans une fenêtre contextuelle superposée.

* **[!UICONTROL Require rights]**. Activez cette option pour afficher uniquement le contenu avec un état de demande de droits « Accordé ».  » »
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d'origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Indiquez si vous autorisez les utilisateurs à publier du texte, une photo ou une vidéo avec le bouton de téléchargement.
   * **[!UICONTROL Require Media]**. Basculez sur pour demander aux utilisateurs de télécharger uniquement le contenu vidéo ou vidéo à l'aide du bouton Télécharger.
   * Vous pouvez modifier le texte par défaut des champs Bouton de téléchargement suivants :

      * **[!UICONTROL Upload Button Text]**. Texte du bouton Télécharger. Le texte par défaut est « What is on your mind ?  » »
      * **[!UICONTROL Comment Modal Title]**. Le titre des visiteurs du site modale utilise le contenu. Le texte par défaut est « Publier votre commentaire ».  » »
      * **[!UICONTROL Comment Modal Button]**. Le texte des visiteurs du site clique sur pour publier du contenu. Le texte par défaut est « Publier votre commentaire ».  » »

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l'action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l'action.
   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu'un bouton Appel à l'action ne s'affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s'affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l'action ne s'affiche pas avec le contenu, sauf si les droits d'accès au contenu sont accordés.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l'en-tête au-dessus du bouton Appel à l'action dans le modal du contenu. La formulation par défaut est « Shop these products :  ».
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l'action du modal du contenu. Le texte par défaut est « Buy Now :  ».
   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le nom de la photo et du produit avec le bouton Appel à l'action.

      >[!NOTE]
      >
      >Les boutons Photo et Nom de produit mettent en surbrillance le bleu lorsqu'ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l'application vers la page de produit associée.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l'application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l'application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l'application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l'application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l'application, Livefyre affiche le contenu d'autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l'application avec d'autres ID de produit, puis le contenu publié dans l'application sans ID de produit.

Vous pouvez personnaliser le mur multimédia à l'aide de :

* **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]**la section. Voir Personnalisation des applications pour plus d'informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]**la section.

* Outils d'intégration. Pour [plus d'informations sur la personnalisation d'un mur multimédia à l'aide des outils d'intégration, reportez-vous à la](/help/implementation/c-app-integrations/c-media-wall-integration.md) section Intégration du mur multimédia.

