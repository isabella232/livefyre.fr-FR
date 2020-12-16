---
description: valeur nulle
seo-description: valeur nulle
seo-title: Balises actives
title: Balises actives
uuid: f978fa83-e79b-46ae-bb3e-0f9449bd0440
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Balises dynamiques{#smart-tags}

Livefyre utilise la technologie de vision informatique Adobe Sensei pour baliser automatiquement les images et les vidéos que vous enregistrez ou téléchargez dans la bibliothèque.

Les balises actives vous permettent de gagner beaucoup de temps, de gérer, de rechercher et de traiter du contenu. Avec les balises actives, vous pouvez :

* Rechercher dans les images et les vidéos enregistrées et téléchargées du contenu précis en fonction de l’image et du contenu vidéo, plutôt que uniquement du texte
* Collecte de contenu dans des flux basés sur des termes de recherche précis qui analysent l’image ou la vidéo, plutôt que sur du texte uniquement

Lorsque vous enregistrez ou téléchargez une image ou une vidéo, Adobe Sensei examine automatiquement le contenu et le balise avec 135 000 classificateurs répartis sur trois catégories :

* Caractéristiques (chats, chiens, pyramides, repères)
* Catégories (par exemple, voyage, tourisme, beauté)
* Propriétés esthétiques (par exemple, qualité d&#39;image, règles de troisième)
* SFW/NSFW (cela vous permet de filtrer automatiquement les images NSFW, ce qui améliore la sécurité de vos flux et de la bibliothèque UGC.

L’algorithme de classement Balises dynamiques filtres le contenu à l’aide d’un score de confiance des balises actives, de la nouveauté du contenu et du nombre d’étoiles qu’un utilisateur a attribué au contenu.

**Balises dynamiques pour la vidéo**

Détails des fonctionnalités :

* Les balises actives sont appliquées aux formats vidéo MP4, .avi et .mov.
* La durée maximale pour les vidéos prises en charge est de 60 secondes ou 50 Mo
* Les balises actives sont disponibles dans les fichiers de recherche sociale, de flux et de vidéo téléchargée de la bibliothèque.

Types de balises :

* Balises de fonction : Fonctionne de la même manière que les balises de fonction pour les images (par exemple, chats, chiens, pyramides, repères).
* Balises d’action : Identifiez les fonctionnalités qui surviennent sur plusieurs images au lieu d’une seule. Elles sont plus efficaces pour résumer le contenu d’une vidéo.

Pour plus d’informations sur les balises actives, voir [Options des règles de flux pour toutes les règles de flux](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
