---
description: Modifiez les options de taille, de largeur et d’interaction de l’application Mur de médias.
seo-description: Modifiez les options de taille, de largeur et d’interaction de l’application Mur de médias.
seo-title: Personnalisations du mur de médias
solution: Experience Manager
title: Personnalisations du mur de médias
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# Personnalisations du mur multimédia{#media-wall-customizations}

Modifiez les options de taille, de largeur et d’interaction de l’application Mur de médias.



Media Walls diffuse en continu des images en direct et d’autres contenus sur un mur social en temps réel, visualisant toutes les activités entourant un événement.

Si cette option est activée, les utilisateurs peuvent publier du texte, des images ou de la vidéo directement sur cette application. Les types de fichier pris en charge sont les suivants :

* Image : JPEG, GIF, PNG
* Vidéo : Quicktime/MOV, MP4, MPEG, WebM
* Audio : WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Définit le nombre initial d’éléments de contenu affichés.

* **[!UICONTROL Load content with animation.]** Activez cette option pour charger le mur multimédia sur une page avec animation. Désactivez cette option pour charger le mur multimédia sur une page sans animation.
* **[!UICONTROL Number of columns.]** Définissez le nombre de colonnes de la paroi multimédia. Le nombre de colonnes reste le même, quelle que soit la taille de la fenêtre ou du navigateur. Si vous sélectionnez Auto, le nombre de colonnes s’ajuste pour afficher un nombre optimisé de colonnes pour la taille de l’écran.
* **[!UICONTROL Fit content to width]**. Lorsque cette option est désactivée, le contenu est recadré sur un carré. Activez cette option pour afficher une image entière dans la carte, qu’elle remplisse la carte ou non.
* **[!UICONTROL Include content modal]**

   Permet aux utilisateurs de cliquer sur une photo dans le flux pour l’ouvrir dans une fenêtre contextuelle superposée.

* **[!UICONTROL Require rights]**. Activez cette option pour n’afficher que le contenu dont l’état de demande de droits est &quot;Octroyé&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Activez cette option pour supprimer le logo du réseau de médias sociaux d&#39;origine (Twitter ou Instagram) lorsque des droits sont accordés pour un élément de contenu.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Indiquez si vous autoriserez les utilisateurs à publier du texte, des photos ou des vidéos à l’aide du bouton de téléchargement.
   * **[!UICONTROL Require Media]**. Activez cette option pour obliger les utilisateurs à télécharger uniquement du contenu photo ou vidéo à l’aide du bouton Télécharger.
   * Vous pouvez modifier le texte par défaut des champs suivants de bouton de téléchargement :

      * **[!UICONTROL Upload Button Text]**. Texte du bouton Télécharger. Le texte par défaut est &quot;Qu’est-ce qui vous préoccupe ?&quot;
      * **[!UICONTROL Comment Modal Title]**. Titre du site modal que les visiteurs utilisent pour publier du contenu. Le texte par défaut est &quot;Publier votre commentaire&quot;.
      * **[!UICONTROL Comment Modal Button]**. Texte du bouton des visiteurs du site sur lequel ils cliquent pour publier du contenu. Le texte par défaut est &quot;Publier votre commentaire&quot;.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour toute action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l&#39;action.
   * **[!UICONTROL Require rights to display products]** Activez cette option pour que le propriétaire du contenu ait accordé des droits sur le contenu avant qu’un bouton Appel à l’action ne s’affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton Appel à l’action ne s’affiche pas avec le contenu à moins que des droits pour le contenu ne soient accordés.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton Appel à l’action dans le module de contenu. La formulation par défaut est &quot;Acheter ces produits :&quot;.
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l’action du module de contenu. Le texte par défaut est &quot;Acheter maintenant :&quot;.
   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher la photo et le nom du produit avec le bouton Appel à l’action.

      >[!NOTE]
      >
      >Les boutons Photo et Nom du produit apparaissent en bleu lorsqu’ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez la bascule sur Activé pour effectuer le suivi des références depuis cette application vers la page de produits associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produits associée.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique à chaque produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié sur l’application, mais balisé avec un autre ID de produit. Une fois que le contenu spécifique à un produit pour l’application s’affiche, Livefyre affiche le contenu pour d’autres produits et le contenu qui n’est pas associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié sur l’application avec d’autres ID de produit, puis au contenu publié sur l’application sans ID de produit.

Vous pouvez personnaliser la paroi multimédia à l’aide des éléments suivants :

* **[!UICONTROL Style]** et  **[!UICONTROL Config]** options pour toutes les applications dans le  **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options **[!UICONTROL Style]** et **[!UICONTROL Config]** standard pour toutes les applications dans le **[!UICONTROL App Designer]**.

* Outils d’intégration. Voir [Intégration du mur multimédia](/help/implementation/c-app-integrations/c-media-wall-integration.md) pour en savoir plus sur la personnalisation d’un mur multimédia à l’aide des outils d’intégration.

