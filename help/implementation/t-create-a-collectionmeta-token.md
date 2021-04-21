---
description: Créez une nouvelle collection en créant un jeton collectionMeta transmis à Livefyre.
title: Création d’une collection à l’aide du jeton CollectionMeta
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Création d’une collection à l’aide de CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}

Créez une nouvelle collection en créant un jeton collectionMeta transmis à Livefyre.

1. Créez le jeton collectionMeta.
1. Créez la somme de contrôle.

   La somme de contrôle est requise si vous souhaitez informer Livefyre de tout changement que vous avez apporté à votre collection. Livefyre met à jour votre collection uniquement si la somme de contrôle fournie est différente de la somme de contrôle précédemment envoyée. Créer une somme de contrôle revient à créer un jeton `collectionMeta`, mais au lieu d&#39;appeler `buildCollectionMetaToken`, vous appelez `buildChecksum`.

Créez des jetons d’utilisateur pour l’authentification dans Livefyre.
