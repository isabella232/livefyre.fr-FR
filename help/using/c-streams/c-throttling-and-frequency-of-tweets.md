---
description: Tous les tweets correspondant à une règle n’apparaissent pas dans un flux.
seo-description: Tous les tweets correspondant à une règle n’apparaissent pas dans un flux.
seo-title: Limitation et fréquence des tweets
solution: Experience Manager
title: Limitation et fréquence des tweets
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Limitation et fréquence des tweets{#throttling-and-frequency-of-tweets}

Tous les tweets correspondant à une règle n’apparaissent pas dans un flux.

Le ralentissement des règles Twitter et les interruptions de flux Twitter peuvent limiter le nombre de tweets visibles dans le flux.

>[!NOTE]
>
>Pour vous assurer que des tweets spécifiques sont inclus dans votre flux, utilisez l’option Télécharger le fichier de la page Tous les actifs.

* Les règles Twitter réduisent le contenu, en extrayant 1 tweet par règle toutes les 5 secondes. Cela permet au contenu apparaissant dans les applications Livefyre d&#39;être plus équilibré et de ne pas être submergé de tweets. La limitation des tweets entrants de cette manière permet également d’éviter que la diffusion en continu ne devienne inondée ou illisible pendant les périodes de trafic élevé.

   >[!NOTE]
   >
   >Pour vous assurer que le contenu des auteurs de grande valeur s’affiche dans vos applications, même dans les flux à grande vitesse, les règles pour des auteurs spécifiques ne sont jamais réduites.

* Des interruptions de flux Twitter peuvent survenir pour plusieurs raisons. Dans certains cas, Twitter n’envoie pas de tweets, Livefyre ne reçoit donc pas de notification du nouveau contenu et ne peut pas être affiché. Les interruptions de service des API de Twitter, ou le trafic sur les hashtags/mots-clés de volume élevé, peuvent également entraîner l’absence de tweets.

