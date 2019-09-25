---
description: Enregistrez le point de fin d’URL afin que Livefyre puisse utiliser l’URL pour extraire les informations de profil mises à jour.
seo-description: Enregistrez le point de fin d’URL afin que Livefyre puisse utiliser l’URL pour extraire les informations de profil mises à jour.
seo-title: Enregistrement du point de fin avec Studio
solution: Experience Manager
title: Enregistrement du point de fin avec Studio
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Enregistrement du point de fin avec Studio{#register-the-endpoint-with-studio}

Enregistrez le point de fin d’URL afin que Livefyre puisse utiliser l’URL pour extraire les informations de profil mises à jour.

Enregistrez l’URL Ping pour Pull une seule fois par réseau. Une fois définie, cette valeur ne doit pas changer, sauf si le point de terminaison de la récupération des données de profil utilisateur de votre système de gestion des utilisateurs change.

1. Utilisez Studio pour enregistrer ce point de fin d’URL auprès de Livefyre.
1. Enregistrez l’URL à partir de laquelle Livefyre récupérera les informations de profil utilisateur mises à jour, accédez à **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**, puis saisissez-la dans le **[!UICONTROL Ping for Pull URL]** champ.

   Par exemple, l’URL peut ressembler à : `https://example.yoursite.com/some_path/?id={id}`

