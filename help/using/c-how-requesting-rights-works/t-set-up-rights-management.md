---
description: Définissez les paramètres de demande de droits pour les publications Instagram et Twitter.
title: Configuration du Rights Management
exl-id: d3d3e837-0ed0-47a8-ac5c-7b9da431d149
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Configuration du Rights Management{#set-up-rights-management}

Définissez les paramètres de demande de droits pour les publications Instagram et Twitter.

Avant de pouvoir définir des paramètres de demande de droits, vous devez configurer un ou plusieurs comptes sociaux pour Instagram ou Twitter. Pour plus d’informations sur la configuration d’un compte social, voir [Ajouter un compte social](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Vous pouvez configurer la gestion des droits au niveau du réseau uniquement. Vous ne pouvez pas configurer la gestion des droits spécifiques au site.

1. Dans Livefyre Studio, accédez à **[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Pour configurer des comptes Rights Management, vous aurez besoin d’autorisations au niveau du réseau de modérateur ou d’administrateur.

1. Sélectionnez **[!UICONTROL +Add New Account]** si vous n’avez aucun compte de Rights Management configuré.
1. Cliquez sur **[!UICONTROL Create New Setting]** sous le réseau social que vous souhaitez utiliser pour le Rights Management.

   >[!NOTE]
   >
   >Pour les comptes Instagram, vous devez disposer d’un compte d’entreprise Instagram pour demander des droits avec une automatisation partielle. Pour plus d&#39;informations sur les différents types de comptes Instagram et comment les utiliser, voir [A propos des comptes Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Renseignez les champs affichés. Tous les champs sont obligatoires.

   * **[!UICONTROL Display name:]** Entrez un nom d’affichage pour identifier le compte Twitter ou Instagram à utiliser pour votre compte Demande de droits. Ce nom est interne uniquement.
   * **[!UICONTROL Enabled:]**Défini sur activé par défaut. Permet la gestion des droits pour le compte.
   * **[!UICONTROL Approval hashtag:]** Hashtag que le propriétaire du contenu utilisera pour indiquer qu’il consent à utiliser son contenu.
   * **[!UICONTROL Terms and conditions:]** Lien vers les Conditions générales de votre réseau pour la réutilisation du contenu. Ce champ est sensible à la casse.
   * **[!UICONTROL Network and sites:]** Réseau ou site pour lequel ce compte peut demander des droits de réutilisation de contenu. Pour rendre ce compte disponible sur l&#39;ensemble du réseau, sélectionnez le premier élément de la liste ou limitez-le à des sites spécifiques à l&#39;aide de la touche Commande/CTRL.
   * **[!UICONTROL Default message:]** Message à afficher avec votre demande de droits. Vous pouvez remplacer ce message lorsque vous demandez des droits.

      * Livefyre présente l’un des messages par défaut aux modérateurs lorsqu’un modérateur envoie une requête à un auteur de contenu. Les modérateurs peuvent générer un autre message par défaut ou modifier le message avant de l’envoyer. Les messages doivent inclure le nom d&#39;utilisateur Twitter ou Instagram de l&#39;auteur ({handle}), le hashtag d&#39;approbation ({grantTag}) et un lien vers vos termes et conditions ({termsLink}).

         **[!UICONTROL Note:]** {handle}, {grantTag} et {termsLink} sont tous sensibles à la casse.

         **[!UICONTROL Note:]** Pour éviter toute utilisation malveillante, Twitter encapsule les URL incluses avec  [t.](https://t.co/) coformatage. Pour éviter que votre message par défaut ne dépasse 140 caractères, Livefyre recommande de ne pas inclure d’URL dans votre message par défaut.

      * Meilleures pratiques pour la rédaction de messages de demande de droits :

         * Créez plusieurs messages par défaut pour ne pas ressembler à un robot. Enregistrez chaque message par défaut avant de créer votre prochain message par défaut.
         * Encouragez vos modérateurs à personnaliser cette note avant de l’envoyer, afin d’éviter que les requêtes de votre réseau ne soient balisées Spam.

1. Cliquez sur **[!UICONTROL Save Settings]** pour ajouter votre compte de demande de droits.
Envoyez une demande de droits à partir de la bibliothèque de fichiers. Voir [Envoyer une demande de droits](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) pour plus d’informations sur la manière d’envoyer une demande de droits à partir de la bibliothèque de fichiers.
