---
description: Tous les tweets qui correspondent à une règle apparaissent dans un flux.
seo-description: Tous les tweets qui correspondent à une règle apparaissent dans un
  flux.
seo-title: Limitation et fréquence des tweets
solution: Experience Manager
title: Limitation et fréquence des tweets
uuid: b 9 edfb 1 e-e 6 cf -4 a 48-8756-05 f 5 f 18 d 8799
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Limitation et fréquence des tweets{#throttling-and-frequency-of-tweets}

Tous les tweets qui correspondent à une règle apparaissent dans un flux.

Les interruptions de règle Twitter et les interruptions de flux Twitter peuvent limiter le nombre de tweets visibles dans le flux.

>[!NOTE]
>
>Pour garantir l'inclusion de tweets spécifiques dans votre flux, utilisez l'option Télécharger le fichier de la page Tous les actifs.

* Les règles Twitter ralentissent le contenu, en extrayant 1 tweet par règle toutes les 5 secondes. Cela permet d'équilibrer le contenu apparaissant dans les applications Livefyre et de ne pas submerger les tweets. La limitation des tweets entrants de cette manière permet également d'empêcher le flux de devenir inactif ou illisible pendant les périodes à fort trafic.

   >[!NOTE]
   >
   >Pour vous assurer que le contenu des auteurs à forte valeur ajoutée apparaît dans vos applications, même dans les flux à vélocité élevée, les règles pour les auteurs spécifiques ne sont jamais ralenties.

* Des interruptions de flux Twitter peuvent se produire pour plusieurs raisons. Dans certains cas, Twitter ne transfère pas les tweets. Par conséquent, Livefyre ne reçoit pas de notification du nouveau contenu et ne peut pas être affiché. Les interruptions de service des API de Twitter ou le trafic sur des hashtags/mots-clés de volume élevé peuvent aussi entraîner l'absence de tweets.

