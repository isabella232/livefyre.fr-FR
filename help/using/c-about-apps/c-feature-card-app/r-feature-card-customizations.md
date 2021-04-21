---
description: Modifiez les options de taille, de largeur et d’interaction de l’application Carte.
title: Personnalisations des cartes de fonctions
exl-id: b907885a-211d-4628-9955-5f1a5ec577cf
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Personnalisations des cartes de fonctionnalités{#feature-card-customizations}

Modifiez les options de taille, de largeur et d’interaction de l’application Carte.

<!-- 
r_feature_card_customization.dita
 -->

Les applications de cartes de fonctions incluent uniquement des personnalisations standard :** [!UICONTROL Theme]**, couleur de la marque, famille de polices et taille de police.

Vous pouvez personnaliser les cartes de fonctions à l’aide des éléments suivants :

* **[!UICONTROL Style]** et  **[!UICONTROL Config]** options pour toutes les applications dans le  **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options **[!UICONTROL Style]** et **[!UICONTROL Config]** standard pour toutes les applications dans le **[!UICONTROL App Designer]**.

* Outils d’intégration. Pour plus d’informations sur la personnalisation des applications à l’aide des outils d’intégration, voir Intégration d’applications.
* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour toute action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton Appel à l&#39;action.
   * **[!UICONTROL Require rights to display products]** Activez cette option pour que le propriétaire du contenu ait accordé des droits sur le contenu avant qu’un bouton Appel à l’action ne s’affiche pour le contenu.

      >[!NOTE]
      >
      >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton Appel à l’action ne s’affiche pas avec le contenu à moins que des droits pour le contenu ne soient accordés.

   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton Appel à l’action dans le module de contenu. La formulation par défaut est &quot;Acheter ces produits :&quot;.
   * **[!UICONTROL Call-to-action button text]** Personnalisez le texte du bouton Appel à l’action. Le texte par défaut est &quot;Acheter maintenant&quot;.
   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher le  **[!UICONTROL Photo]** et le  **[!UICONTROL Product name]** avec le bouton Appel à l&#39;action.
   * **[!UICONTROL Product URL referral tracking]** Basculez la bascule sur Activé pour effectuer le suivi des références depuis cette application vers la page de produits associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produits associée.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique à chaque produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez `CTRL/Command + click` pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié sur l’application, mais balisé avec un autre ID de produit. Une fois que le contenu spécifique à un produit pour l’application s’affiche, Livefyre affiche le contenu pour d’autres produits et le contenu qui n’est pas associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié sur l’application avec d’autres ID de produit, puis au contenu publié sur l’application sans ID de produit.
