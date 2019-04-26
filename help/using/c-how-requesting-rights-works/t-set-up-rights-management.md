---
description: Définissez les paramètres de demande des droits pour les publications
  Instagram et Twitter.
seo-description: Définissez les paramètres de demande des droits pour les publications
  Instagram et Twitter.
seo-title: Configuration de Rights Management
solution: Experience Manager
title: Configuration de Rights Management
uuid: 3 ffcbc 95-484 f -4 eba-b 817-658 c 1 d 658 bf 8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Configuration de Rights Management{#set-up-rights-management}

Définissez les paramètres de demande des droits pour les publications Instagram et Twitter.

Avant de pouvoir définir les Paramètres de demande de droits, vous devez configurer un ou plusieurs comptes sociaux pour Instagram ou Twitter. Pour plus d'informations sur la configuration d'un compte social, voir [Ajout d'un compte Social](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Vous pouvez configurer la gestion des droits au niveau réseau uniquement. Vous ne pouvez pas configurer la gestion des droits spécifique au site.

1. Dans Livefyre Studio, accédez **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**à.

   >[!NOTE]
   >
   >Vous devez disposer des autorisations au niveau du réseau modérateur ou administrateur pour configurer les comptes Rights Management.

1. Sélectionnez **[!UICONTROL +Add New Account]** si vous n'avez aucune configuration de comptes Rights Management.
1. Cliquez **[!UICONTROL Create New Setting]** sur sous le réseau social que vous souhaitez utiliser pour Rights Management.

   >[!NOTE]
   >
   >Pour les comptes Instagram, vous devez disposer d'un compte d'entreprise Instagram pour demander des droits d'automatisation partielle. Pour plus d'informations sur les différents types de comptes Instagram et sur leur utilisation, voir [A propos des comptes Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Renseignez les champs affichés. Tous les champs sont obligatoires.

   * **[!UICONTROL Display name:]** Saisissez un nom d'affichage pour identifier le compte Twitter ou Instagram à utiliser pour votre compte de demande de droits. Ce nom est interne uniquement.
   * ****[!UICONTROL Enabled:]Définir par défaut. Active la gestion des droits pour le compte.
   * **[!UICONTROL Approval hashtag:]** hashtag utilisé par le propriétaire du contenu pour indiquer qu'il consent à utiliser son contenu.
   * **[!UICONTROL Terms and conditions:]** Lien vers les termes et conditions de votre réseau pour la réutilisation du contenu. Ce champ est sensible à la casse.
   * **[!UICONTROL Network and sites:]** Réseau ou site pour lequel ce compte peut demander des droits de réutilisation de contenu. Pour rendre ce compte disponible sur l'ensemble de votre réseau, sélectionnez le premier élément de la liste ou limitez-le à des sites spécifiques à l'aide de la touche Commande/CTRL.
   * **[!UICONTROL Default message:]** Message à afficher avec votre demande de droits. Vous pouvez remplacer ce message lorsque vous demandez des droits.

      * Livefyre présente l'un des messages par défaut aux modérateurs lorsqu'un modérateur envoie une demande à un auteur de contenu. Les modérateurs peuvent générer un autre message par défaut ou modifier le message avant d'envoyer. Les messages doivent inclure la poignée Twitter ou Instagram de l'auteur ({hand}), votre hashtag d'approbation ({granttag}) et un lien vers vos termes et conditions ({termslink}).

         **[!UICONTROL Note:]** {hand}, {granttag} et {termslink} sont sensibles à la casse.

         **[!UICONTROL Note:]** Pour éviter une utilisation malveillante, Twitter englobe toutes les URL incluses avec [formatage t. co](https://t.co/) . Pour éviter que votre message par défaut ne dépasse 140 caractères, Livefyre recommande de ne pas inclure les URL dans votre message par défaut.

      * Recommandations relatives à l'écriture des messages de demande de droits :

         * Créez plusieurs messages par défaut afin de ne pas être un robot. Enregistrez chaque message par défaut avant de créer le message par défaut suivant.
         * Encouragez vos modérateurs à personnaliser cette note avant d'envoyer, afin d'éviter que les requêtes de votre réseau ne soient balisées par messages indésirables.

1. Cliquez sur **[!UICONTROL Save Settings]** pour ajouter votre compte de demande de droits.
Envoyez une demande de droits à partir de la bibliothèque de fichiers. Voir [Envoi d'une demande de droits](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) pour plus d'informations sur la manière d'envoyer une demande de droits à partir de la bibliothèque de fichiers.