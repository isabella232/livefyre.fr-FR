---
description: Modifiez les options de taille, de largeur et d’interaction de l’application Mur de médias.
seo-description: Modifiez les options de taille, de largeur et d’interaction de l’application Mur de médias.
seo-title: Personnalisations du mur multimédia
solution: Experience Manager
title: Personnalisations du mur multimédia
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisations du mur multimédia{#media-wall-customizations}

Change the size, width, and interaction options of the Media Wall app.



Les murs de médias diffusent en continu des images en direct et d’autres contenus sur un mur social en temps réel, visualisant toute l’activité entourant un événement.

S’ils sont activés, les utilisateurs peuvent publier du texte, des images ou de la vidéo directement sur cette application. Les types de fichier pris en charge sont les suivants :

* Image : JPEG, GIF, PNG
* Vidéo : Quicktime/MOV, MP4, MPEG, WebM
* Audio : WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Définit le nombre initial d’éléments de contenu affichés.

* **[!UICONTROL Load content with animation.]** Activez cette option pour charger le mur multimédia sur une page avec animation. Désactivez cette option pour charger le mur multimédia sur une page sans animation.
* **[!UICONTROL Number of columns.]** Définissez le nombre de colonnes pour le mur multimédia. Le nombre de colonnes reste le même, quelle que soit la taille de la fenêtre ou du navigateur. Si vous sélectionnez Auto, le nombre de colonnes s’ajuste pour afficher un nombre optimisé de colonnes pour la taille de l’écran.
* **[!UICONTROL Fit content to width]**. Lorsque cette option est désactivée, le contenu est recadré sur un carré. Activez cette option pour afficher une image entière dans la carte, qu’elle remplisse ou non la carte entière.
* **[!UICONTROL Include content modal]**

   Permet aux utilisateurs de cliquer sur une photo dans le flux pour l’ouvrir dans une fenêtre contextuelle superposée.

* **[!UICONTROL Require rights]**. Activez cette option pour n’afficher que le contenu dont l’état de demande de droits est "Octroyé".
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau social d’origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Indiquez si vous autoriserez les utilisateurs à publier du texte, des photos ou des vidéos avec le bouton de téléchargement.
   * **[!UICONTROL Require Media]**. Activez cette option pour demander aux utilisateurs de télécharger uniquement du contenu photo ou vidéo à l’aide du bouton Télécharger.
   * Vous pouvez modifier le texte par défaut pour les champs de bouton de téléchargement suivants :

      * **[!UICONTROL Upload Button Text]**. Texte du bouton Télécharger. Le texte par défaut est "Qu’est-ce que vous pensez ?"
      * **[!UICONTROL Comment Modal Title]**. Titre du site modal que les visiteurs utilisent pour publier du contenu. Le texte par défaut est "Publier votre commentaire".
      * **[!UICONTROL Comment Modal Button]**. Texte du bouton sur lequel les visiteurs du site cliquent pour publier du contenu. Default text is "Post Your Comment."

* **[!UICONTROL Call-to-action button]** You can use the Call-to-action button with a product catalog to direct users to a product or to your site for further action.

   * **[!UICONTROL Call-to-action button]** Switch the toggle to on to display the Call-to-action button.
   * **[!UICONTROL Require rights to display products]** Switch the toggle to on to require that the content owner has granted rights for the content before a Call-to-action button appears for the content.

      >[!NOTE]
      >
      >The content displays even if rights are not granted for the content, but the Call-to-action button will not display with the content unless rights for the content are granted.

   * **[!UICONTROL Call-to-action header text]** The words to display in the header above the Call-to-action button in the content modal. Default wording is, "Shop these products:".
   * **[!UICONTROL Call-to-action button text]** The words to display in the Call-to-action button in the content modal. Default text is, "Buy Now:".
   * **[!UICONTROL Product display options]** Choose whether you want to display the Photo and Product name with the Call-to-action button.

      >[!NOTE]
      >
      >Both the Photo and Product name buttons highlight blue when they are enabled.

   * **[!UICONTROL Product URL referral tracking]** Switch the toggle to on to track referrals from this App to the associated product page.
   * **[!UICONTROL Referral tracking key-value pairs]** Add parameters to further specify the referral tracking from your App content to the associated product page.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Select this option to create one App for multiple product pages. Filter product-specific UGC to the App for each product page. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produit de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez Ctrl/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié dans l’application, mais balisé avec un ID de produit différent. Une fois que le contenu spécifique au produit de l’application s’affiche, Livefyre affiche le contenu d’autres produits et du contenu non associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié dans l’application avec d’autres ID de produit, puis au contenu publié dans l’application sans ID de produit.

Vous pouvez personnaliser Media Wall à l’aide des éléments suivants :

* **[!UICONTROL Style]** et **[!UICONTROL Config]** les options pour toutes les applications dans le **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options standard **[!UICONTROL Style]** et **[!UICONTROL Config]** pour toutes les applications dans le **[!UICONTROL App Designer]**.

* Outils d’intégration. Voir Intégration [du mur](/help/implementation/c-app-integrations/c-media-wall-integration.md) multimédia pour en savoir plus sur la personnalisation d’un mur multimédia à l’aide des outils d’intégration.

