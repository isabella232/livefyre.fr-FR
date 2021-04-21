---
description: Réponses aux questions fréquentes (FAQ) sur les demandes de protection des renseignements personnels prêtes pour le RMMD.
title: FAQ sur les requêtes de confidentialité
exl-id: 6d0add45-589a-46d0-b15a-63a7599aad73
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---

# FAQ sur la demande de confidentialité{#privacy-request-faqs}

Réponses aux questions fréquentes (FAQ) sur les demandes de protection des renseignements personnels prêtes pour le RMMD.

* **Comment les visiteurs du site peuvent-ils opt-out être suivis sur un site qui utilise les applications Livefyre ?** Lorsqu’un visiteur de site se désabonne, l’implémentation du client doit indiquer à Livefyre que l’utilisateur s’est désabonné avant d’instancier une application. Livefyre a créé un moyen de le faire avec l&#39;option JavaScript, `userPrivacyOptOut`. Pour plus d&#39;informations sur l&#39;utilisation de `userPrivacyOptOut`, consultez [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Lorsque l’indicateur `userPrivacyOptOut` est défini sur true, les applications de la page ne transmettent pas les données aux serveurs Livefyre à l’aide de cookies ou d’une autre méthode. Livefyre ne mettra alors pas à jour l&#39;enregistrement local avec les données qui pourraient être utilisées pour suivre les visiteurs du site. Si une source ne prend pas en charge de proxy, Livefyre affiche un masque sur le contenu, sauf si un utilisateur clique sur la vidéo et approuve le suivi potentiel à partir de cette source.

   Si vous utilisez l’identité Livefyre, les utilisateurs peuvent choisir de supprimer leur profil ou de créer un rapport des données suivies pour leur compte utilisateur.

* **Comment empêcher la collecte de contenu futur auprès d’un visiteur du site qui a choisi de ne pas participer ?** Utilisation  `userPrivacyOptOut` avec  `livefyre.js` sur une page Web qui utilise les applications Livefyre. Pour plus d&#39;informations sur `userPrivacyOptOut`, consultez [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Comment puis-je générer un rapport et supprimer les données pour les utilisateurs de l’application ou les propriétaires de comptes sociaux ?** [Confidentialité ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) Demande de générer un rapport et de supprimer les données utilisateur des applications.

* **Comment supprimer tout le contenu d’un visiteur ?** Livefyre ne conserve pas d&#39;informations persistantes sur les visiteurs du site, sauf sous la forme de cookies pour les identifier de manière unique pour les fonctionnalités de Livecount. Livecount est un nombre transitoire et en temps réel de visiteurs sur le site. Aucun historique n&#39;est conservé une fois que le visiteur quitte ou efface les cookies.

   Créez une [demande de confidentialité](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) pour supprimer le compte. Livefyre supprime ou rend anonyme l’utilisateur et tout enregistrement associé.

* **Comment supprimer du contenu pour un utilisateur enregistré ?** Créez une  [demande de ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) confidentialité pour supprimer le compte. Le profil utilisateur et les enregistrements associés seront entièrement détruits.

   >[!NOTE]
   >
   >Cette action ne peut pas être annulée.

* **Comment puis-je produire un rapport des données suivies d&#39;un employé actuel ou ancien employé ?** [Vue d’un ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) rapport de confidentialité pour générer un rapport de données suivies pour un compte d’utilisateur.

* **Livefyre est-il compatible avec les flux sociaux ?** Lorsqu’un utilisateur supprime une publication ou un tweet de son réseau social, dans les 24 heures, le contenu est également supprimé de toutes les sources de Livefyre. Cela s&#39;applique à Twitter et Facebook.
