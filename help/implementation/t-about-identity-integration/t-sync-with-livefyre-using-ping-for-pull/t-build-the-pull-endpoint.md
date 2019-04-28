---
description: Générez le point de fin d'extraction pour recevoir et répondre aux demandes d'accès à votre système d'identité utilisateur.
seo-description: Générez le point de fin d'extraction pour recevoir et répondre aux demandes d'accès à votre système d'identité utilisateur.
seo-title: Création du point de fin Pull
solution: Experience Manager
title: Création du point de fin Pull
uuid: 1703152 f-aaa 7-4 a 88-aa 33-d 9 f 8957 ad 42 b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création du point de fin Pull{#build-the-pull-endpoint}

Générez le point de fin d&#39;extraction pour recevoir et répondre aux demandes d&#39;accès à votre système d&#39;identité utilisateur.

1. Créez un endpoint de terminaison HTTPS qui reçoit les requêtes Livefyre et répond à un objet JSON contenant les données utilisateur les plus récentes.

   >[!NOTE]
   >
   >Ce point de fin doit être accessible. Il est également vivement recommandé d&#39;envoyer les requêtes et les réponses au protocole HTTPS.

1. Enregistrez le point de fin avec Studio.
