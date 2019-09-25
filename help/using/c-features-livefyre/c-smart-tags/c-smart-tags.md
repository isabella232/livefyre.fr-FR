---
description: valeur nulle
seo-description: valeur nulle
seo-title: Balises intelligentes
title: Balises intelligentes
uuid: f978fa83-e79b-46ae-bb3e-0f9449bd0440
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Balises intelligentes{#smart-tags}

Livefyre utilise la technologie de vision informatique d’Adobe Sensei pour baliser automatiquement les images et les vidéos que vous enregistrez ou téléchargez dans la bibliothèque.

Les balises intelligentes vous permettent de gagner du temps, de gérer, de rechercher et de traiter le contenu de manière significative. Avec les balises intelligentes, vous pouvez :

* Recherchez des images et des vidéos enregistrées et téléchargées pour obtenir un contenu précis en fonction du contenu de l’image et de la vidéo, plutôt que uniquement du texte.
* Collecte de contenu dans des flux en fonction de termes de recherche précis qui analysent l’image ou la vidéo, plutôt que de texte uniquement

Lorsque vous enregistrez ou téléchargez une image ou une vidéo, Adobe Sensei examine automatiquement le contenu et le balise avec 135 000 classificateurs répartis dans trois catégories :

* Fonctionnalités (chats, chiens, pyramides, repères)
* Catégories (par exemple, voyage, tourisme, beauté)
* Propriétés esthétiques (par exemple, qualité d'image, règles de troisième)
* SFW/NSFW (cela vous permet de filtrer automatiquement les images NSFW, améliorant la sécurité de vos flux et de la bibliothèque UGC.

L’algorithme de classement Balises dynamiques filtre le contenu à l’aide d’un score de confiance des balises actives, de la nouveauté du contenu et du nombre d’étoiles qu’un utilisateur a attribué au contenu.

**Balises intelligentes pour la vidéo**

Détails des fonctionnalités :

* Les balises actives sont appliquées aux formats vidéo MP4, .avi et .mov.
* La durée maximale des vidéos prises en charge est de 60 secondes ou 50 Mo
* Les balises actives sont disponibles dans les fichiers Recherche sociale, Flux et Vidéo téléchargée de la bibliothèque.

Types de balises :

* Balises de fonction : Fonctionne de la même manière que les balises feature pour les images (chats, chiens, pyramides, repères).
* Balises d’action : Identifiez les fonctionnalités qui surviennent sur plusieurs images au lieu d’une seule. Elles sont plus efficaces pour résumer le contenu d’une vidéo.

Pour plus d’informations sur les balises actives, voir Options des règles de [diffusion en continu pour toutes les règles](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de diffusion en continu.
