---
description: Créez une collection en créant un jeton collectionMeta qui est transmis à Livefyre.
seo-description: Créez une collection en créant un jeton collectionMeta qui est transmis à Livefyre.
seo-title: Création d’une collection à l’aide du jeton CollectionMeta
solution: Experience Manager
title: Création d’une collection à l’aide du jeton CollectionMeta
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Création d’une collection à l’aide du jeton CollectionMeta{#create-a-collection-using-the-collectionmeta-token}

Créez une collection en créant un jeton collectionMeta qui est transmis à Livefyre.

1. Créez le jeton collectionMeta.
1. Créez la somme de contrôle.

   La somme de contrôle est requise si vous souhaitez informer Livefyre de tout changement que vous avez apporté à votre collection. Livefyre met à jour votre collection uniquement si la somme de contrôle fournie est différente de la somme de contrôle précédemment envoyée. La création d’une somme de contrôle revient à créer un `collectionMeta` jeton, mais au lieu d’appeler `buildCollectionMetaToken` vous `buildChecksum`.

Créez des jetons d’utilisateur pour l’authentification dans Livefyre.