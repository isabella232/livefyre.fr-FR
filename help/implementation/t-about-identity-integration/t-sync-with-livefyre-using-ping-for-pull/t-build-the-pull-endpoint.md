---
description: Créez le point de fin d’extraction pour recevoir les demandes d’accès à votre système d’identité utilisateur et y répondre.
seo-description: Créez le point de fin d’extraction pour recevoir les demandes d’accès à votre système d’identité utilisateur et y répondre.
seo-title: Création du point de fin d’extraction
solution: Experience Manager
title: Création du point de fin d’extraction
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Création du point de fin d’extraction{#build-the-pull-endpoint}

Créez le point de fin d’extraction pour recevoir les demandes d’accès à votre système d’identité utilisateur et y répondre.

1. Créez un point de fin HTTPS qui reçoit les demandes Livefyre et répond avec un objet JSON qui contient les dernières données utilisateur.

   >[!NOTE]
   >
   >Ce point de fin doit être accessible. Il est également vivement recommandé d’envoyer les requêtes et les réponses via le protocole HTTPS.

1. Enregistrez le point de fin avec Studio.
