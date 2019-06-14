---
description: Générez la structure de demande d'extraction pour recevoir et répondre aux demandes d'accès à votre système d'identité utilisateur.
seo-description: Générez la structure de demande d'extraction pour recevoir et répondre aux demandes d'accès à votre système d'identité utilisateur.
seo-title: Extraire la structure de demande
solution: Experience Manager
title: Extraire la structure de demande
uuid: bf 6 b 9 e 45-d 08 a -48 e 6-acc 6-e 4 fa 56428 d 25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# Extraire la structure de demande{#pull-request-structure}

Générez la structure de demande d&#39;extraction pour recevoir et répondre aux demandes d&#39;accès à votre système d&#39;identité utilisateur.

Livefyre envoie une demande de pull à votre URL de endpoint de fin.

Par exemple, si l&#39;URL de endpoint de fin Pull est :

```
https://example.yoursite.com/some_path/?id={id}
```

La demande Pull Livefyre à ce point de fin sera :

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

où `lftoken` est un jeton Web JSON signé avec votre clé réseau. **[!UICONTROL {userAuthToken}]** Il s&#39;agit du jeton authentique de l&#39;utilisateur généré par Livefyre.

1. Servez-vous `lftoken` de cette option pour vérifier que les requêtes à votre Ping pour l&#39;URL d&#39;extraction ont été envoyées par Livefyre et non par un agent malveillant.
1. Pour toutes les requêtes entrantes :

   * Vérifiez que la chaîne `lftoken` de requête est présente dans la requête.
   * Utilisez `validateLivefyreToken` la méthode dans les bibliothèques Livefyre pour vérifier que `lftoken` celle-ci a été signée avec votre clé réseau.

   * Si `lftoken` le paramètre est absent ou échoue, n&#39;autorisez pas votre point de fin à répondre aux informations de profil. Répondez plutôt à un code d&#39;état 403 (Interdit) et sans corps de réponse.

1. `userAuthToken` est générée par la méthode Livefyre `buildUserAuthToken` pour l&#39;utilisateur, avec user - id « system ». Cet utilisateur est le premier utilisateur créé pour chaque nouveau réseau.
