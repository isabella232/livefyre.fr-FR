---
description: Découvrez comment fonctionnent les demandes de droits. Lorsque vous incorporez du contenu généré par l’utilisateur dans une application Livefyre, le contenu inclut une autorisation tacite de réutilisation. Vous devez disposer de l’autorisation de l’auteur pour utiliser du contenu de Twitter ou Instagram.
title: Demande de droits
exl-id: c709f55b-1773-4de6-82c2-6d3963671095
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Demande de droits{#requesting-rights}

Découvrez comment fonctionnent les demandes de droits. Lorsque vous incorporez du contenu généré par l’utilisateur dans une application Livefyre, le contenu inclut une autorisation tacite de réutilisation. Vous devez disposer de l’autorisation de l’auteur pour utiliser du contenu de Twitter ou Instagram.

Les états de droits suivants sont disponibles à partir de la bibliothèque, du contenu de l’application, de ModQ et d’AEM Commerce :

* **[!UICONTROL Granted]**. Lorsque l’auteur vous accorde le droit de réutiliser leur contenu, l’état de la ressource devient **[!UICONTROL Granted]**.

* **[!UICONTROL Expired]**. Livefyre surveille les flux Instagram et Twitter pour obtenir la réponse de l’auteur pendant 14 jours. Après 14 jours, la demande expire, l’état de la demande de droits devient **[!UICONTROL Expired]** et vous pouvez envoyer une seconde demande ou supprimer l’élément de votre bibliothèque.
* **[!UICONTROL Requested]**. Demandez l’autorisation pour le contenu de la bibliothèque. Vous pouvez effectuer cette opération pour une ou plusieurs ressources à la fois. Après avoir demandé l’autorisation, Livefyre définit l’état de la ressource sur **[!UICONTROL Requested]**.
* **[!UICONTROL Needs Review]**. Si l’auteur répond par une note qui n’inclut pas votre #approvalHashtag, l’état de la ressource devient **[!UICONTROL Needs Review]**.

* **[!UICONTROL Request Failed]**. Échec de l&#39;envoi de la demande (en raison d&#39;un jeton expiré, etc.).
* **[!UICONTROL Request Pending]**. Place la demande de droits en file d’attente afin qu’un nombre limité d’envois soit envoyé simultanément.

Vous pouvez demander des droits pour les actifs que vous avez obtenus de Twitter et Instagram. Vous devez enregistrer le fichier dans la bibliothèque pour demander des droits.

Vous devez configurer un *compte commercial Instagram* pour demander des droits sur les ressources à Instagram à l’aide d’un processus partiellement automatisé.

Vous ne pouvez utiliser cette fonctionnalité que pour le contenu que vous avez obtenu à partir d’une recherche ou d’une recherche de flux par un compte d’entreprise. Pour demander des droits sur le contenu que vous avez obtenu à partir d’un compte Instagram personnel, vous devez envoyer des demandes de droits manuellement.

>[!NOTE]
>
>Pour plus d&#39;informations sur les différents types de comptes Instagram et comment les utiliser, voir [A propos des comptes Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts). Pour plus d’informations sur la façon de demander des droits pour les comptes Instagram, voir [Envoyer des demandes de droits manuels](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md#c_send_instagram_manual_rights_request) et [Envoyer des demandes de droits partiellement automatisés](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md#c_send_an_instagram_rights_request_from_the_library).
