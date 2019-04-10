---
description: Créez une collection en créant un jeton collectionmeta transmis à Livefyre.
seo-description: Créez une collection en créant un jeton collectionmeta transmis à
  Livefyre.
seo-title: Création d'une collection à l'aide du jeton collectionmeta
solution: Experience Manager
title: Création d'une collection à l'aide du jeton collectionmeta
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Création d'une collection à l'aide du jeton collectionmeta{#create-a-collection-using-the-collectionmeta-token}

Créez une collection en créant un jeton collectionmeta transmis à Livefyre.

1. Créez le jeton collectionmeta.
1. Créez la somme de contrôle.

   La somme de contrôle est requise si vous souhaitez avertir Livefyre des modifications apportées à votre collection. Livefyre met à jour votre collection uniquement si la somme de contrôle fournie est différente de la somme de contrôle précédemment envoyée. Creating a checksum is just like creating a `collectionMeta` token but instead of calling `buildCollectionMetaToken` you call `buildChecksum`.

Créez des jetons utilisateur pour l'authentification dans Livefyre.