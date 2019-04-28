---
description: Générez le ping pour que vos pages Livefyre soient traitées lorsque les utilisateurs mettent à jour leur profil.
seo-description: Générez le ping pour que vos pages Livefyre soient traitées lorsque les utilisateurs mettent à jour leur profil.
seo-title: Créer le ping
solution: Experience Manager
title: Créer le ping
uuid: cb 8 cc 043-9 ea 5-407 c-b 70 f -3 f 1 e 37 accdae
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Créer le ping{#build-the-ping}

Générez le ping pour que vos pages Livefyre soient traitées lorsque les utilisateurs mettent à jour leur profil.

Lorsque Livefyre reçoit une notification de mise à jour avec `networkName` la, `user_id`le système envoie une demande Pull à votre Ping pour l&#39;URL Pull.

>[!NOTE]
>
>403/Non Autorisé en réponse à votre Ping signifie qu&#39;un ajout non valide `lftoken` à la demande Ping est ajouté. Assurez-vous que la `lftoken` valeur est affectée `user_id` aux privilèges de propriétaire réseau ou à l&#39;utilisateur système. Si vous utilisez des bibliothèques Livefyre, utilisez `buildLivefyreToken` la méthode pour générer un jeton système valide pour la requête.

1. Ajoutez du code à votre page qui déborde Livefyre lorsque les utilisateurs mettent à jour leur profil. Générez l&#39;URL de cette manière :

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Votre nom de réseau fourni par Livefyre.
* **[!UICONTROL user_id:]** ID de votre utilisateur.
* **[!UICONTROL token:]** Jeton système valide.

1. Extrayez la structure de requête.
