---
description: Créez le point de terminaison d'extraction pour recevoir les demandes d'accès à votre système d'identité utilisateur et y répondre.
title: Créer un point de terminaison d’extraction
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# Générer le point de terminaison de l’extraction{#build-the-pull-endpoint}

Créez le point de terminaison d&#39;extraction pour recevoir les demandes d&#39;accès à votre système d&#39;identité utilisateur et y répondre.

1. Créez un point de terminaison HTTPS qui reçoit les requêtes Livefyre et répond avec un objet JSON qui contient les dernières données utilisateur.

   >[!NOTE]
   >
   >Ce point de terminaison doit être accessible. Il est également fortement recommandé que les requêtes et les réponses soient envoyées via le protocole HTTPS.

1. Enregistrez le point de terminaison avec Studio.
