---
description: Créez la structure des demandes d'extraction pour recevoir les demandes d'accès à votre système d'identité utilisateur et y répondre.
title: Extraire la structure de demande
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Extraire la structure de requête{#pull-request-structure}

Créez la structure des demandes d&#39;extraction pour recevoir les demandes d&#39;accès à votre système d&#39;identité utilisateur et y répondre.

Livefyre envoie une requête Pull à votre URL de point de terminaison.

Par exemple, si l’URL de votre point de terminaison Tirer est :

```
https://example.yoursite.com/some_path/?id={id}
```

la requête Livefyre Pull à ce point de terminaison sera :

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

où `lftoken` est un jeton Web JSON signé avec votre clé réseau et **[!UICONTROL {userAuthToken}]** est le jeton d’authentification utilisateur généré par Livefyre.

1. Utilisez `lftoken` pour vérifier que les requêtes de votre URL Ping for Pull ont été envoyées par Livefyre et non par un agent malveillant.
1. Pour toutes les requêtes entrantes :

   * Assurez-vous que la chaîne de requête `lftoken` est présente sur la demande.
   * Utilisez la méthode `validateLivefyreToken` dans les bibliothèques Livefyre pour vous assurer que `lftoken` a été signé avec votre clé réseau.

   * Si `lftoken` n&#39;est pas présent ou si la validation échoue, n&#39;autorisez pas votre point de terminaison à répondre avec les informations du profil. Au lieu de cela, répondez avec un code d’état 403 (interdit) et aucun corps de réponse.

1. `userAuthToken` est généré par la  `buildUserAuthToken` méthode Livefyre pour l’utilisateur, avec l’ID utilisateur &quot;system&quot;. Cet utilisateur est le premier utilisateur créé pour chaque nouveau réseau.
