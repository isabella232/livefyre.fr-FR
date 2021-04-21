---
description: Proposez une gestion centralisée des stocks spécifique au produit à des points spécifiques du parcours client afin d’augmenter le mode d’achat et la conversion à l’aide de la fonction Commerce de l’UGC.
title: UGC Commerce
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 2%

---


# UGC Commerce{#ugc-commerce}

Proposez une gestion centralisée des stocks spécifique au produit à des points spécifiques du parcours client afin d’augmenter le mode d’achat et la conversion à l’aide de la fonction Commerce de l’UGC.

Utilisez la fonction Commerce UGC pour influencer le mode d&#39;achat et la conversion sur les pages de détails des produits et des commandes UGC. Accélérer la mise sur le marché en associant de manière transparente l&#39;UGC à l&#39;inventaire des produits. Fidélisez votre marque en créant une communauté à l’aide de l’outil UGC pour mettre en évidence les témoignages authentiques des clients.

AEM Livefyre fournit plusieurs méthodes pour importer les informations du catalogue de produits, notamment le SKU, les images miniatures, le prix et le nom du produit. Gérez facilement l’association des produits avec l’UGC en utilisant les demandes de droits d’AEM Livefyre, le balisage des règles de diffusion automatique et les workflows de modération.

En plus d’influencer les achats, les capacités de l’offre commerciale UGC d’AEM Livefyre peuvent être exploitées pour générer des conversions de différentes manières, notamment :

* Génération de pistes B2B : placer des boutons d&#39;appel à l&#39;action sous l&#39;UGC pour capturer les pistes
* Téléchargements d’applications B2C : inviter les utilisateurs à télécharger une application
* Références à l&#39;article : lier les utilisateurs aux articles liés à des éléments de l&#39;UGC

Placez des appels à l’action de produit en même temps que l’UGC pour générer des conversions. Vous pouvez :

* Ajoutez le CU spécifique au produit à l&#39;échelle de milliers de pages de détails du produit.
* Incorporez les applications de visualisation AEM Livefyre qui prennent en charge les fonctionnalités de commerce UGC, telles que Media Wall et Mosaic, dans les pages de détails des produits.
* Utilisez des codes de suivi de référence configurables avec une solution d&#39;analyse pour mesurer les conversions à partir des DEC de produit placées sur les CU et CU placées sur les pages de détails des produits.

AEM Les utilisateurs du commerce peuvent intégrer en toute transparence leur catalogue de produits existant dans Livefyre afin de stimuler l’engagement des utilisateurs dans les applications de visualisation de Livefyre. Les utilisateurs de Livefyre qui n’utilisent pas AEM Commerce peuvent importer manuellement leurs catalogues de produits dans Livefyre. Voir [Télécharger des produits vers Livefyre à l’aide du téléchargement de fichier](/help/using/c-features-livefyre/c-ugc-commerce.md), pour en savoir plus.

Applications qui utilisent cette fonctionnalité :

* [Feature Card](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app). Pour plus d’informations sur l’utilisation du commerce UGC dans une carte de fonction, voir [Personnalisations des cartes de fonction](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Pour plus d’informations sur l’utilisation du commerce UGC dans un film strip, voir [Personnalisations du film strip](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Mur](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app) des médias. Pour plus d’informations sur l’utilisation du commerce UGC dans un mur multimédia, voir [Personnalisations du mur multimédia](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaïque](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Pour plus d’informations sur l’utilisation du commerce UGC dans une mosaïque, voir [Mosaic Customizations](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Présentation : Utilisation du bouton Appel à l&#39;action commercial UGC {#section_s2d_tln_n1b}

1. Créez une application à l’aide d’un bouton d’appel à l’action. Voir [Ajouter un bouton d’appel à l’action à une application](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Ajoutez votre catalogue de produits sur Livefyre. Vous pouvez importer du contenu de l’une des deux manières suivantes :

   * [Importez des produits dans Livefyre à l’aide d’AEM ](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) Commerce si vous utilisez AEM Commerce.
   * [Téléchargez des produits sur ](/help/using/c-features-livefyre/c-ugc-commerce.md) Livefyresi vous n’utilisez pas AEM Commerce.

1. Associez des produits au contenu. Vous pouvez le faire de quatre manières différentes :

   * Depuis la bibliothèque. Voir [Association de produits au contenu à l’aide de la bibliothèque](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * De ModQ. Voir [Modération du contenu à l’aide de ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md).
   * Contenu de l’application. Voir [Ajouter un bouton d’appel à l’action à une application](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * A partir d&#39;un flux. Voir [Options des règles de diffusion pour toutes les règles de diffusion](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Télécharger des produits vers Livefyre à l’aide du téléchargement de fichier {#section_n1s_4hz_m1b}

Téléchargez des produits à utiliser avec votre bouton d’appel à l’action pour ajouter des produits à associer au contenu ou pour modifier et supprimer des fichiers existants.

>[!NOTE]
>
>Le téléchargement d’un fichier dans un dossier contenant des fichiers existants supprime tous les fichiers qu’il contient et les remplace par le nouveau fichier.

1. Accédez à **[!UICONTROL Network Settings > Products.]**
1. Créez un **[!UICONTROL Product Folder]** ou utilisez un **[!UICONTROL Product Folder]** existant.

1. Cliquez sur le **[!UICONTROL Product Folder]** pour le sélectionner.
1. Cliquez sur le bouton **[!UICONTROL Upload Products]**.
1. Téléchargez un fichier de produit dans l’un des formats suivants :

   * Format de fichier de produits Google
   * Format Livefyre (voir ci-dessous)

   Téléchargez un fichier JSON au format standard. Vous pouvez télécharger un modèle pour voir un exemple du format standard. Voici un exemple d’une ligne de produits dans un modèle. Il suit la séquence `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}` :

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   Le tableau décrit les paires clé/valeur dont vous avez besoin pour télécharger des produits :

## Paires clé/valeur pour le format standard de téléchargement du catalogue de produits

| Clé | Type | Description |
|--- |--- |--- |
| id | Chaîne | ID unique du produit. |
| oembed | Objet | Pièce jointe `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | Chaîne | Titre du produit. |
| isFolder | Booléen | Si la valeur est true, le produit est traité comme un dossier (par exemple, homme, femme, etc.). |
| parentId | Chaîne | Définit le dossier dans lequel se trouve le produit. |
| description | Chaîne | Description du produit. |
| prix | Chaîne | Valeur du produit en dollars. Par exemple, &quot;23.36&quot;. |
| sku | Chaîne | Unité de gestion des stocks (UGS) du produit. |
| url | Chaîne | Lien vers la page du produit. |
| enabled | Booléen | La valeur True signifie que le produit est principal. |
| attributs | Tableau | Types et valeurs qui définissent le produit (par exemple, couleur, taille, etc.). Il s&#39;agit d&#39;un tableau d&#39;objets.</br>**Propriétés:** </br>type  </br>Type : </br>StringDescription : Couleur,  </br>valeur de taille  </br>Type : Chaîne  </br>Description : Vert, XS |
| balises | Tableau | Balises définissant des catégories de contenu (par exemple, voitures, chaussures, etc.). C&#39;est un tableau de chaînes. |

## ModQ {#section_os1_v4t_n1b}

Vous pouvez associer du contenu aux produits de votre catalogue de produits dans ModQ en fonction de vos workflows de modération existants. Pour plus d’informations sur l’utilisation du commerce UGC avec ModQ, voir [Modération du contenu à l’aide de ModQ](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Flux {#section_qtj_v4t_n1b}

Vous pouvez associer automatiquement des produits au contenu à l’aide de règles de diffusion en continu, puis publier automatiquement le contenu sur une application, l’enregistrer dans la bibliothèque ou le modérer à l’aide de ModQ. Pour plus d’informations sur l’utilisation du commerce UGC avec les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
