---
description: Créez le point de terminaison d'extraction pour recevoir les demandes d'accès à votre système d'identité utilisateur et y répondre.
seo-description: Créez le point de terminaison d'extraction pour recevoir les demandes d'accès à votre système d'identité utilisateur et y répondre.
seo-title: Créer un point de terminaison d’extraction
solution: Experience Manager
title: Créer un point de terminaison d’extraction
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Générer le point de terminaison de l’extraction{#build-the-pull-endpoint}

Créez le point de terminaison d&#39;extraction pour recevoir les demandes d&#39;accès à votre système d&#39;identité utilisateur et y répondre.

1. Créez un point de terminaison HTTPS qui reçoit les requêtes Livefyre et répond avec un objet JSON qui contient les dernières données utilisateur.

   >[!NOTE]
   >
   >Ce point de terminaison doit être accessible. Il est également fortement recommandé que les requêtes et les réponses soient envoyées via le protocole HTTPS.

1. Enregistrez le point de terminaison avec Studio.
