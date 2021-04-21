---
description: Suivez les étapes de la liste de contrôle pour vous assurer que vous réussirez la conversion du protocole HTTP en protocole HTTPS.
title: Liste de contrôle SSL
exl-id: 20161aa5-57c9-417b-af0e-c9e1e771f861
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Liste de contrôle SSL{#ssl-checklist}

Suivez les étapes de la liste de contrôle pour vous assurer que vous réussirez la conversion du protocole HTTP en protocole HTTPS.

Si les éléments suivants sont terminés, la conversion HTTP en HTTPS est réussie :

* Toutes mes intégrations serveur à serveur utilisent HTTPS.
* Toutes mes intégrations serveur à serveur prennent en charge le chiffrement TLS 1.2.
* Toutes mes applications mobiles utilisent le protocole HTTPS.
* Toutes mes applications mobiles prennent en charge le chiffrement TLS 1.2.
* Toutes mes intégrations JavaScript personnalisées (StreamhubSDK ou utilisation directe d’API) utilisent HTTPS.
* Si je rassemble du code JavaScript Livefyre, nous utilisons les dernières versions.
* J’ai notifié tout service tiers (par exemple, analyse de contenu, modération, etc.) qui consomme des API Livefyre pour mon compte.
