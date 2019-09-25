---
description: Générez le ping de sorte que votre page fasse des pings Livefyre lorsque les utilisateurs mettent à jour leur profil.
seo-description: Générez le ping de sorte que votre page fasse des pings Livefyre lorsque les utilisateurs mettent à jour leur profil.
seo-title: Création du ping
solution: Experience Manager
title: Création du ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Création du ping{#build-the-ping}

Générez le ping de sorte que votre page fasse des pings Livefyre lorsque les utilisateurs mettent à jour leur profil.

Lorsque Livefyre reçoit une notification de mise à jour avec le `networkName` et `user_id`, le système envoie une requête Pull à votre URL Ping for Pull.

>[!NOTE]
>
>403/Non autorisé en réponse à votre ping indique qu’un élément non valide `lftoken` a été ajouté à la requête Ping. Assurez-vous que le `lftoken` est destiné à un `user_id` disposant de droits de propriétaire réseau ou à l'utilisateur système. Si vous utilisez des bibliothèques Livefyre, utilisez la `buildLivefyreToken` méthode pour générer un jeton système valide pour la requête.

1. Ajoutez du code à votre page qui épingle Livefyre lorsque les utilisateurs mettent à jour leur profil. Créez l’URL de cette manière :

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Votre Livefyre a fourni un nom réseau.
* **[!UICONTROL user_id:]** ID de votre utilisateur.
* **[!UICONTROL token:]** Jeton système valide.

1. Extrayez la structure de requête.
