---
description: Modifiez les options de taille, de largeur et d'interaction de l'application Mur multimédia.
seo-description: Modifiez les options de taille, de largeur et d'interaction de l'application Mur multimédia.
seo-title: Personnalisations du mur multimédia
solution: Experience Manager
title: Personnalisations du mur multimédia
uuid: 79 aecd 92-3937-4 bb 4-a 1 a 6-b 090 fb 39 afb 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisations du mur multimédia{#media-wall-customizations}

Modifiez les options de taille, de largeur et d&#39;interaction de l&#39;application Mur multimédia.



Les murs de médias sont des images actives et d&#39;autres contenus dans un mur social en temps réel, qui visualisent toutes les activités entourant un événement.

Si cette option est activée, les utilisateurs peuvent publier du texte, des images ou des vidéos directement dans cette application. Les types de fichiers pris en charge sont les suivants :

* Image : JPEG, GIF, PNG
* Vidéo : Quicktime/MOV, MP 4, MPEG, webm
* Audio : WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Définit le nombre initial d&#39;éléments de contenu affichés.

* **[!UICONTROL Load content with animation.]** Activez cette option pour charger le mur multimédia sur une page avec une animation. Désactivez cette option pour charger le mur multimédia sur une page sans animation.
* **[!UICONTROL Number of columns.]** Définissez le nombre de colonnes pour le mur multimédia. Le nombre de colonnes reste le même, quelle que soit la taille de la fenêtre ou du navigateur. Si vous sélectionnez Auto, le nombre de colonnes s&#39;ajuste pour afficher un nombre optimisé de colonnes pour la taille de l&#39;écran.
* **[!UICONTROL Fit content to width]**. Lorsque cette option est désactivée, le contenu est recadré sur un carré. Activez cette option pour afficher une image entière dans la carte, qu&#39;elle remplisse la totalité de la carte ou non.
* **[!UICONTROL Include content modal]**

   Permet aux utilisateurs de cliquer sur une photo dans le flux pour l&#39;ouvrir dans une fenêtre contextuelle superposée.

* **[!UICONTROL Require rights]**. Activez cette option pour afficher uniquement le contenu avec un état de demande de droits « Accordé ».  » »
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d&#39;origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Indiquez si vous autorisez les utilisateurs à publier du texte, une photo ou une vidéo avec le bouton de téléchargement.
   * **[!UICONTROL Require Media]**. Basculez sur pour demander aux utilisateurs de télécharger uniquement le contenu vidéo ou vidéo à l&#39;aide du bouton Télécharger.
   * Vous pouvez modifier le texte par défaut des champs Bouton de téléchargement suivants :

      * **[!UICONTROL Upload Button Text]**. Texte du bouton Télécharger. Le texte par défaut est « What is on your mind ?  » »
      * **[!UICONTROL Comment Modal Title]**. Le titre des visiteurs du site modale utilise le contenu. Le texte par défaut est « Publier votre commentaire ».  » »
      * **[!UICONTROL Comment Modal Button]**. Le texte des visiteurs du site clique sur pour publier du contenu. Le texte par défaut est « Publier votre commentaire ».  » »

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l&#39;action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour une action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l&#39;action.
   * **[!UICONTROL Require rights to display products]** Activez la bascule pour exiger que le propriétaire du contenu ait accordé des droits pour le contenu avant qu&#39;un bouton Appel à l&#39;action ne s&#39;affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s&#39;affiche même si les droits ne sont pas accordés pour le contenu, mais le bouton Appel à l&#39;action ne s&#39;affiche pas avec le contenu, sauf si les droits d&#39;accès au contenu sont accordés.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l&#39;en-tête au-dessus du bouton Appel à l&#39;action dans le modal du contenu. La formulation par défaut est « Shop these products :  ».
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l&#39;action du modal du contenu. Le texte par défaut est « Buy Now :  ».
   * **[!UICONTROL Product display options]** Choisissez si vous souhaitez afficher le nom de la photo et du produit avec le bouton Appel à l&#39;action.

      >[!NOTE]
      >
      >Les boutons Photo et Nom de produit mettent en surbrillance le bleu lorsqu&#39;ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez le commutateur sur pour suivre les références de cette application à la page de produit associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour préciser le suivi des références depuis votre contenu de l&#39;application vers la page de produit associée.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez UGC spécifique au produit à l&#39;application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l&#39;application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour le filtrage UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise le dossier pour déterminer les produits de ce dossier à afficher dans l&#39;application sur diverses pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l&#39;application, mais avec un ID de produit différent. Une fois le contenu spécifique au produit affiché pour l&#39;application, Livefyre affiche le contenu d&#39;autres produits et contenus non associés à un produit. Livefyre prioritise en priorité le contenu avec le même ID de produit, puis le contenu publié sur l&#39;application avec d&#39;autres ID de produit, puis le contenu publié dans l&#39;application sans ID de produit.

Vous pouvez personnaliser le mur multimédia à l&#39;aide de :

* **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]** la section. Voir Personnalisation des applications pour plus d&#39;informations sur la norme **[!UICONTROL Style]** et **[!UICONTROL Config]** les options de toutes les applications dans **[!UICONTROL App Designer]** la section.

* Outils d&#39;intégration. Pour [plus d&#39;informations sur la personnalisation d&#39;un mur multimédia à l&#39;aide des outils d&#39;intégration, reportez-vous à la](/help/implementation/c-app-integrations/c-media-wall-integration.md) section Intégration du mur multimédia.

