---
description: Tous les tweets correspondant à une règle n’apparaissent pas dans un flux.
title: Limitation et fréquence des tweets
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Limitation et fréquence des tweets{#throttling-and-frequency-of-tweets}

Tous les tweets correspondant à une règle n’apparaissent pas dans un flux.

Le ralentissement des règles twitter et les interruptions de flux Twitter peuvent limiter le nombre de tweets visibles dans le flux.

>[!NOTE]
>
>Pour vous assurer que des tweets spécifiques sont inclus dans votre flux, utilisez l’option Télécharger le fichier de la page Tous les actifs.

* Les règles twitter réduisent le contenu, en extrayant 1 tweet par règle toutes les 5 secondes. Cela permet au contenu apparaissant dans les applications Livefyre d&#39;être plus équilibré et de ne pas être submergé de tweets. La limitation des tweets entrants de cette manière permet également d’éviter que la diffusion en continu ne devienne inondée ou illisible pendant les périodes de trafic élevé.

   >[!NOTE]
   >
   >Pour vous assurer que le contenu des auteurs de grande valeur s’affiche dans vos applications, même dans les flux à grande vitesse, les règles pour des auteurs spécifiques ne sont jamais réduites.

* Les interruptions de flux twitter peuvent survenir pour plusieurs raisons. Dans certains cas, Twitter n’envoie pas de tweets, Livefyre ne reçoit donc pas de notification du nouveau contenu et ne peut pas être affiché. Les interruptions de service des API de Twitter, ou le trafic sur les hashtags/mots-clés de volume élevé, peuvent également entraîner l’absence de tweets.
