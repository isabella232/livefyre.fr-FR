---
description: Réponses à la Foire aux questions (FAQ) sur les demandes de confidentialité prêtes pour le RMMD.
seo-description: Réponses à la Foire aux questions (FAQ) sur les demandes de confidentialité prêtes pour le RMMD.
seo-title: FAQ sur les requêtes de confidentialité
solution: Experience Manager
title: FAQ sur les requêtes de confidentialité
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# FAQ sur les requêtes de confidentialité{#privacy-request-faqs}

Réponses à la Foire aux questions (FAQ) sur les demandes de confidentialité prêtes pour le RMMD.

* **Comment les visiteurs du site peuvent-ils se désinscrire du suivi sur un site qui utilise des applications Livefyre ?** Lorsqu’un visiteur du site se désactive, l’implémentation du client doit indiquer à Livefyre que l’utilisateur a choisi de s’exclure avant d’instancier une application. Livefyre a créé un moyen de le faire avec l'option JavaScript, `userPrivacyOptOut`. Pour plus d’informations sur l’utilisation `userPrivacyOptOut`, voir [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Lorsque l’ `userPrivacyOptOut` indicateur est défini sur true, les applications de la page ne transmettent pas les données aux serveurs Livefyre à l’aide de cookies ou d’une autre méthode. Livefyre ne mettra alors pas à jour le stockage local avec les données qui pourraient être utilisées pour suivre les visiteurs du site. Si une source ne prend pas en charge de proxy, Livefyre affiche un masque sur le contenu, sauf si un utilisateur clique sur la vidéo et approuve le suivi potentiel à partir de cette source.

   Si vous utilisez l’identité Livefyre, les utilisateurs peuvent choisir de supprimer leur profil ou de créer un rapport des données suivies pour leur compte utilisateur.

* **Comment empêcher la collecte de contenu futur auprès d’un visiteur du site qui s’est désabonné ?** Utilisation `userPrivacyOptOut` avec `livefyre.js` sur une page Web qui utilise les applications Livefyre. Pour plus d’informations `userPrivacyOptOut`, voir [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Comment générer un rapport et supprimer les données pour les utilisateurs d’applications ou les propriétaires de comptes sociaux ?** Demande [de](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) confidentialité pour générer un rapport et supprimer les données utilisateur des applications.

* **Comment supprimer tout le contenu d’un visiteur ?** Livefyre ne conserve pas d’informations persistantes sur les visiteurs du site, sauf sous la forme de cookies pour les identifier de manière unique pour les fonctionnalités Livecount. Livecount est un nombre transitoire et en temps réel de visiteurs sur le site. Aucun historique n’est conservé une fois que le visiteur quitte ou efface les cookies.

   Créez des requêtes [de](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) confidentialité pour supprimer le compte. Livefyre supprime ou rend anonyme le profil utilisateur et les enregistrements associés.

* **Comment supprimer du contenu pour un utilisateur enregistré ?** Créez une requête [de](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) confidentialité pour supprimer le compte. Le profil utilisateur et les enregistrements associés seront entièrement détruits.

   >[!NOTE]
   >
   >Cette action ne peut pas être annulée.

* **Comment puis-je produire un rapport des données suivies d’un employé actuel ou ancien employé ?** [Affichez un rapport](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) sur la confidentialité pour générer un rapport des données suivies pour un compte utilisateur.

* **Livefyre est-il compatible avec les flux sociaux ?** Lorsqu’un utilisateur supprime une publication ou un tweet de son réseau social, le contenu est également supprimé de toutes les sources de Livefyre dans les 24 heures. Cela s’applique à Twitter et Facebook.

