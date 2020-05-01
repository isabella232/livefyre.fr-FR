---
description: Créez le ping de sorte que votre page enregistre Livefyre lorsque les utilisateurs mettent à jour leur profil.
seo-description: Créez le ping de sorte que votre page enregistre Livefyre lorsque les utilisateurs mettent à jour leur profil.
seo-title: Création du ping
solution: Experience Manager
title: Création du ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516

---


# Création du ping{#build-the-ping}

Créez le ping de sorte que votre page enregistre Livefyre lorsque les utilisateurs mettent à jour leur profil.

Lorsque Livefyre reçoit une notification de mise à jour avec le `networkName` et `user_id`, le système envoie une requête Pull à votre URL Ping for Pull.

>[!NOTE]
>
>403/Non autorisé en réponse à votre Ping indique qu’un élément non valide `lftoken` a été ajouté à la demande Ping. Assurez-vous que la variable `lftoken` est destinée à un `user_id` utilisateur disposant de droits de propriétaire réseau ou de l&#39;utilisateur système. Si vous utilisez des bibliothèques Livefyre, utilisez la `buildLivefyreToken` méthode pour générer un jeton système valide pour la requête.

1. Ajouter le code sur votre page qui pèse Livefyre lorsque les utilisateurs mettent à jour leur profil. Créez l’URL de cette manière :

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Votre Livefyre a fourni un nom de réseau.
   * **[!UICONTROL user_id:]** ID de votre utilisateur.
   * **[!UICONTROL token:]** Jeton système valide.

1. Extrayez la structure de la requête.
