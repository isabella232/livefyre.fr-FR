---
description: Réponses aux questions fréquentes sur les demandes de confidentialité
  prêtes pour GDPR.
seo-description: Réponses aux questions fréquentes sur les demandes de confidentialité
  prêtes pour GDPR.
seo-title: FAQ sur la demande de confidentialité
solution: Experience Manager
title: FAQ sur la demande de confidentialité
uuid: 0 cd 6 f 0 d 2-504 d -46 e 9-ac 46-070536 cda 086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# FAQ sur la demande de confidentialité{#privacy-request-faqs}

Réponses aux questions fréquentes sur les demandes de confidentialité prêtes pour GDPR.

* **Comment les visiteurs du site peuvent-ils se désabonner d'un suivi sur un site qui utilise les applications Livefyre ?** Lorsqu'un visiteur du site se désabonne, l'implémentation du client doit indiquer à Livefyre que l'utilisateur s'est désabonné avant d'instancier une application. Livefyre has created a way to do this with the JavaScript option, `userPrivacyOptOut`. Pour plus d'informations sur l'utilisation `userPrivacyOptOut`, voir [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Lorsque `userPrivacyOptOut` l'indicateur est défini sur true, toutes les applications de la page ne transmettent pas de données aux serveurs Livefyre à l'aide de cookies ou d'une autre méthode. Livefyre ne met ensuite pas à jour le stockage local avec les données qui pourraient être utilisées pour effectuer le suivi des visiteurs du site. Si une source ne prend pas en charge un proxy, Livefyre affiche un masque sur le contenu, sauf si un utilisateur clique sur la vidéo et approuve le suivi potentiel de cette source.

   Si vous utilisez Livefyre Identity, les utilisateurs peuvent choisir de supprimer leur profil ou de créer un rapport des données suivies pour leur compte utilisateur.

* **Comment empêcher la collecte du contenu futur d'un visiteur du site qui s'est désabonné ?** Utilisez `userPrivacyOptOut` une `livefyre.js` webpage Web qui utilise les applications Livefyre. Pour plus d'informations `userPrivacyOptOut`, reportez-vous à [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Comment générer un rapport et supprimer les données pour les utilisateurs de l'application ou les propriétaires de comptes sociaux ?**[Demandes de confidentialité](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) pour générer un rapport et supprimer les données utilisateur des applications.

* **Comment supprimer tout le contenu d'un visiteur ?** Livefyre ne conserve pas les informations persistantes concernant les visiteurs du site, sauf sous la forme de cookies pour les identifier de manière unique pour les fonctionnalités Livecount. Livecount est un nombre transitoire et réel de visiteurs sur le site. Aucun historique n'est conservé lorsque le visiteur quitte ou efface les cookies.

   Créez une [demande de confidentialité](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) pour supprimer le compte. Livefyre supprime ou rend le profil utilisateur et les enregistrements associés anonymes.

* **Comment supprimer du contenu pour un utilisateur enregistré ?** Créez une [demande de confidentialité](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) pour supprimer le compte. Le profil utilisateur et les enregistrements associés seront entièrement détruits.

   >[!NOTE]
   >
   >Cette action ne peut pas être annulée.

* **Comment puis-je produire un rapport des données suivies d'un employé actuel ou précédent ?**[Affichez un rapport de confidentialité](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) pour générer un rapport des données suivies pour un compte utilisateur.

* **Le flux social Livefyre est-il conforme ?** Lorsqu'un utilisateur supprime une publication ou un tweet de son réseau social, dans un délai de 24 heures, le contenu est également supprimé de toutes les sources dans Livefyre. Cela s'applique à Twitter et Facebook.

