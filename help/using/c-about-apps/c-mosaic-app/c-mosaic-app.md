---
description: Ajoutez un mur dynamique de couleurs, de photos et de vidéos sur votre site à l’aide d’une application Mosaic.
seo-description: Ajoutez un mur dynamique de couleurs, de photos et de vidéos sur votre site à l’aide d’une application Mosaic.
seo-title: Mosaïque
solution: Experience Manager
title: Mosaïque
uuid: 331c5f80-7440-4b91-8ac6-4f56a8a5befe
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 1%

---


# Mosaïque{#mosaic}

Ajoutez un mur dynamique de couleurs, de photos et de vidéos sur votre site à l’aide d’une application Mosaic.

Mosaic transforme le contenu généré par l’utilisateur en un mur dynamique de couleurs et de photos, en affichant les derniers contenus téléchargés et les médias sociaux dans un format de grille uniforme.

Les visiteurs du site peuvent placer le pointeur de la souris sur une carte en mosaïque pour afficher du texte et d’autres informations sur le contenu. Les utilisateurs mobiles et non mobiles peuvent développer une carte pour afficher une image plus grande, partager du contenu et lire de la vidéo. À mesure que de nouveaux éléments deviennent disponibles, les anciens éléments sont supprimés et placés à nouveau dans la file d’attente pour former la grille parfaite.

## À propos de Mosaic {#section_tng_slj_yy}

Mosaic affiche le contenu le plus récent de Livefyre et de Stream dans une grille uniforme. Pour créer une expérience visuelle plus transparente, les informations sur le contenu s’affichent uniquement lorsque vous passez la souris dessus. À mesure que de nouveaux éléments deviennent disponibles, les anciens éléments sont supprimés et replacés dans la file d’attente.

## Quel type de contenu puis-je publier dans une mosaïque ? {#section_b5h_qlj_yy}

Contenu pris en charge contenant :

* Photos
* Vidéos
* Audio

Sources de contenu prises en charge :

* Twitter
* Instagram
* Facebook
* YouTube
* RSS
* Tumblr
* Livefyre
* Weibo

Vous ne pouvez publier du contenu contenant du texte que sur une mosaïque, sauf s’il fait partie d’une publication de photo ou de vidéo.

## Comment un visiteur de site voit-il le contenu dans une mosaïque ? {#section_w5c_plj_yy}

Un visiteur de site voit le contenu renseigné dans une mosaïque à partir de Studio à partir d’un flux Studio ou d’une recherche sur les réseaux sociaux. Si un nouveau contenu est publié dans l’application alors qu’un visiteur de site se trouve sur la page, le nouveau contenu s’affiche immédiatement et réduit l’ancien contenu en temps réel sans qu’un utilisateur ait à actualiser sa page.

## Que se passe-t-il lorsqu’un visiteur de site clique sur un élément d’une mosaïque ? {#section_cvz_nlj_yy}

* Sur un ordinateur de bureau, vous pouvez placer le pointeur de la souris sur la carte pour la retourner et afficher une icône de développement. Cliquez sur l’icône Développer pour vue d’une image plus grande, regarder une vidéo ou voir plusieurs éléments multimédias dans le contenu.
* Sur un périphérique mobile, vous pouvez cliquer sur une carte pour vue d’une image plus grande, regarder une vidéo ou voir plusieurs éléments multimédias dans le contenu.

## Un visiteur de site peut-il partager du contenu d’une mosaïque ? {#section_zzz_mlj_yy}

Oui. Un visiteur de site peut partager tous les types de contenu sur une mosaïque :

* Sur un bureau, passez la souris sur la carte, puis cliquez sur l’icône de partage.
* Sur un périphérique mobile, cliquez sur une carte pour l’ouvrir et cliquez sur l’icône de partage.

## À quelle fréquence les pièces tournent-elles à travers les cartes ? {#section_hpx_llj_yy}

Un nouveau contenu est ajouté toutes les 10 secondes.

## Comment le nouveau contenu est-il ajouté à une mosaïque ? {#section_f4w_klj_yy}

Ajouter du contenu à une mosaïque en :

* Publication manuelle à partir de la bibliothèque.
* Configuration d’un flux pour une publication automatique.
* Utilisation du bouton de téléchargement, s’il est activé.

## Comment le contenu textuel uniquement s’affiche-t-il dans l’application ? {#section_h31_klj_yy}

Mosaic n’affiche pas de contenu texte uniquement. Mosaic affiche uniquement les images et les vidéos.

## Pourquoi est-ce que je vois parfois des boîtes grises dans une mosaïque ? {#section_i5c_jlj_yy}

Mosaic fonctionne mieux avec une collection qui a constamment un nouveau contenu. Si votre application comporte moins de 25 éléments de contenu, des zones grises s’affichent pour constituer les zones supplémentaires. Remplissez la mosaïque avec plus de contenu pour empêcher l’affichage des zones grises. Prévoyez de placer au moins 32 éléments de contenu dans l’application pour qu’elle s’affiche comme prévu.

## Pourquoi une partie de mon contenu ne s’affiche-t-elle pas sur mon site même si le contenu s’affiche dans Studio ? {#section_upr_hlj_yy}

Mosaïque affiche le contenu dans une grille parfaite. Si vous disposez de 25 éléments de contenu, la largeur de votre conteneur doit tenir compte de cinq éléments de contenu pour que les 25 éléments de contenu s’affichent : cinq à la fois et cinq à la baisse.

Si la largeur de votre conteneur ne tient que sur quatre pour créer une grille parfaite, mais que vous avez 25 éléments de contenu, Mosaic classe le contenu supplémentaire comme une exception et ne l’affiche pas dans l’application. L’élément de contenu aberrant n’est pas pivoté car, techniquement, il se trouve sur l’application, mais n’est pas affiché. Si la largeur de votre conteneur correspond à sept, seulement 21 s&#39;afficheront, puisque quatre sont des valeurs aberrantes et ne formeront pas la grille parfaite.

Parfois, le contenu ne s’affiche pas, car vous avez activé **[!UICONTROL Require rights]**. Si vous activez cette option, vous devez disposer de droits pour tout le contenu de l’application. Si l’état des droits n’est pas &quot;accordé&quot; pour un élément de contenu, il ne s’affiche pas dans l’application.

## Création de mosaïque à l’aide de Studio {#section_dwb_glj_yy}

Vous pouvez créer toutes les applications dans Livefyre Studio de la même manière. Voir Création d’applications pour en savoir plus sur la création d’une application Mosaic dans Studio à l’aide du processus standard.

## Localisation d’une mosaïque {#section_lnv_clj_yy}

La localisation est disponible pour Mosaïque. Vous pouvez :

* Changer les chaînes disponibles pour Mosaic
* Création et modification d’un jeu de traduction pour Mosaic
* Application d’une visionneuse de conversions à un site
* Application d’une visionneuse de traduction à un réseau

