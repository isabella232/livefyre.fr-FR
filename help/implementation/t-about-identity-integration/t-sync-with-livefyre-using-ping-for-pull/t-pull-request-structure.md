---
description: Créez la structure des demandes d’extraction pour recevoir les demandes d’accès à votre système d’identité utilisateur et y répondre.
seo-description: Créez la structure des demandes d’extraction pour recevoir les demandes d’accès à votre système d’identité utilisateur et y répondre.
seo-title: Extraire la structure de requête
solution: Experience Manager
title: Extraire la structure de requête
uuid: bf6b9e45-d08a-48e6-ac6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# Extraire la structure de requête{#pull-request-structure}

Créez la structure des demandes d’extraction pour recevoir les demandes d’accès à votre système d’identité utilisateur et y répondre.

Livefyre envoie une requête Pull à votre URL de point de fin.

Par exemple, si votre URL de point de fin d’extraction est :

```
https://example.yoursite.com/some_path/?id={id}
```

la requête Livefyre Pull à ce point de fin sera :

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

où `lftoken` est un jeton Web JSON signé avec votre clé réseau et **[!UICONTROL {userAuthToken}]** est le jeton d’authentification de l’utilisateur généré par Livefyre.

1. Utilisez `lftoken` pour vérifier que les requêtes envoyées à votre URL Ping for Pull ont été envoyées par Livefyre et non par un agent malveillant.
1. Pour toutes les requêtes entrantes :

   * Vérifiez que la chaîne de `lftoken` requête est présente dans la requête.
   * Utilisez la `validateLivefyreToken` méthode des bibliothèques Livefyre pour vous assurer que `lftoken` vous avez signé avec votre clé réseau.

   * Si `lftoken` la validation est absente ou échoue, n’autorisez pas votre point de fin à répondre avec les informations de profil. Au lieu de cela, répondez avec un code d’état 403 (interdit) et aucun corps de réponse.

1. `userAuthToken` est générée par la méthode Livefyre `buildUserAuthToken` pour l’utilisateur, avec l’ID utilisateur "system". Cet utilisateur est le premier utilisateur créé pour chaque nouveau réseau.
