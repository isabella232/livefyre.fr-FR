---
description: Définissez les paramètres de demande de droits pour les publications Instagram et Twitter.
seo-description: Définissez les paramètres de demande de droits pour les publications Instagram et Twitter.
seo-title: Configuration de Rights Management
solution: Experience Manager
title: Configuration de Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Configuration de Rights Management{#set-up-rights-management}

Définissez les paramètres de demande de droits pour les publications Instagram et Twitter.

Avant de pouvoir définir les paramètres de demande de droits, vous devez configurer un ou plusieurs comptes sociaux pour Instagram ou Twitter. Pour plus d’informations sur la configuration d’un compte social, voir [Ajout d’un compte](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)social.

>[!NOTE]
>
>Vous pouvez configurer la gestion des droits au niveau du réseau uniquement. Vous ne pouvez pas configurer la gestion des droits propres au site.

1. Dans Livefyre Studio, accédez à **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Vous aurez besoin d’autorisations au niveau du réseau du modérateur ou de l’administrateur pour configurer des comptes Rights Management.

1. Sélectionnez **[!UICONTROL +Add New Account]** si aucun compte Rights Management n’est configuré.
1. Cliquez sur **[!UICONTROL Create New Setting]** sous le réseau social à utiliser pour Rights Management.

   >[!NOTE]
   >
   >Pour les comptes Instagram, vous devez disposer d’un compte Instagram pour demander des droits avec une automatisation partielle. Pour plus d’informations sur les différents types de comptes Instagram et leur utilisation, voir [A propos des comptes](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)Instagram.

1. Renseignez les champs affichés. Tous les champs sont obligatoires.

   * **[!UICONTROL Display name:]** Entrez un nom d’affichage pour identifier le compte Twitter ou Instagram à utiliser pour votre compte de demande de droits. Ce nom est interne uniquement.
   * **[!UICONTROL Enabled:]**Défini sur activé par défaut. Permet la gestion des droits pour le compte.
   * **[!UICONTROL Approval hashtag:]** Hashtag que le propriétaire du contenu utilisera pour indiquer qu’il consent à utiliser son contenu.
   * **[!UICONTROL Terms and conditions:]** Lien vers les Conditions générales de votre réseau pour la réutilisation du contenu. Ce champ est sensible à la casse.
   * **[!UICONTROL Network and sites:]** Réseau ou site pour lequel ce compte peut demander des droits de réutilisation du contenu. Pour rendre ce compte disponible sur l'ensemble du réseau, sélectionnez le premier élément de la liste ou limitez-le à des sites spécifiques à l'aide de la touche Commande/CTRL.
   * **[!UICONTROL Default message:]** Message à afficher avec votre demande de droits. Vous pouvez remplacer ce message lorsque vous demandez des droits.

      * Livefyre présente l’un des messages par défaut aux modérateurs lorsqu’un modérateur émet une requête à un auteur de contenu. Les modérateurs peuvent générer un autre message par défaut ou modifier le message avant l’envoi. Les messages doivent inclure le compte Twitter ou Instagram de l’auteur ({handle}), le hashtag d’approbation ({grantTag}) et un lien vers vos conditions d’utilisation ({termsLink}).

         **[!UICONTROL Note:]** {handle}, {grantTag} et {termsLink} sont tous sensibles à la casse.

         **[!UICONTROL Note:]** Pour éviter toute utilisation malveillante, Twitter encapsule les URL incluses avec [le formatage de t.co](https://t.co/) . Pour éviter que votre message par défaut ne dépasse 140 caractères, Livefyre recommande de ne pas inclure d’URL dans votre message par défaut.

      * Meilleures pratiques pour la rédaction de messages de demande de droits :

         * Créez plusieurs messages par défaut afin de ne pas ressembler à un robot. Enregistrez chaque message par défaut avant de créer votre prochain message par défaut.
         * Encouragez vos modérateurs à personnaliser cette note avant de l’envoyer, afin d’éviter que les requêtes de votre réseau ne soient balisées comme des messages indésirables.

1. Cliquez sur **[!UICONTROL Save Settings]** pour ajouter votre compte de demande de droits.
Envoyez une demande de droits à partir de la bibliothèque de fichiers. Voir [Envoyer une demande](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) de droits pour plus d’informations sur la manière d’envoyer une demande de droits à partir de la bibliothèque de fichiers.