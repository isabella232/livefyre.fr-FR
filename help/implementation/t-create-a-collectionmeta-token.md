---
description: Créez une nouvelle collection en créant un jeton collectionMeta transmis à Livefyre.
seo-description: Créez une nouvelle collection en créant un jeton collectionMeta transmis à Livefyre.
seo-title: Création d’une collection à l’aide du jeton CollectionMeta
solution: Experience Manager
title: Création d’une collection à l’aide du jeton CollectionMeta
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Création d’une collection à l’aide de CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}

Créez une nouvelle collection en créant un jeton collectionMeta transmis à Livefyre.

1. Créez le jeton collectionMeta.
1. Créez la somme de contrôle.

   La somme de contrôle est requise si vous souhaitez informer Livefyre de tout changement que vous avez apporté à votre collection. Livefyre met à jour votre collection uniquement si la somme de contrôle fournie est différente de la somme de contrôle précédemment envoyée. Créer une somme de contrôle revient à créer un jeton `collectionMeta`, mais au lieu d&#39;appeler `buildCollectionMetaToken`, vous appelez `buildChecksum`.

Créez des jetons d’utilisateur pour l’authentification dans Livefyre.