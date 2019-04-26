---
description: Enregistrez le point de fin URL de sorte que Livefyre puisse utiliser
  l'URL pour extraire les informations de profil mises à jour.
seo-description: Enregistrez le point de fin URL de sorte que Livefyre puisse utiliser
  l'URL pour extraire les informations de profil mises à jour.
seo-title: Enregistrement du point de fin avec studio
solution: Experience Manager
title: Enregistrement du point de fin avec studio
uuid: 4 eb 816 ee-d 743-43 bf-bfee-d 9 b 9 fd 98 b 482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Enregistrement du point de fin avec studio{#register-the-endpoint-with-studio}

Enregistrez le point de fin URL de sorte que Livefyre puisse utiliser l'URL pour extraire les informations de profil mises à jour.

Enregistrez l'option Ping pour l'URL Pull une fois par réseau. Une fois défini, cette valeur ne doit pas changer, sauf si le point de fin permet de récupérer les données de profil utilisateur de votre système de gestion des utilisateurs.

1. Utilisez Studio pour enregistrer ce point de fin URL avec Livefyre.
1. Enregistrez l'URL à partir de laquelle Livefyre récupère les informations de profil utilisateur mises à jour, accédez **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**à, puis saisissez-la dans **[!UICONTROL Ping for Pull URL]** le champ.

   Par exemple, l'URL peut ressembler à : `https://example.yoursite.com/some_path/?id={id}`

