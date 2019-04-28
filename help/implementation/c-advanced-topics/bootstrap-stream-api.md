---
description: Utilisez l'API d'amorçage et de diffusion en continu avec les applications Livefyre.
seo-description: Utilisez l'API d'amorçage et de diffusion en continu avec les applications Livefyre.
seo-title: Utilisation de l'API de démarrage et de diffusion en continu avec les applications Livefyre
solution: Experience Manager
title: Affichage des détails du compte
uuid: bace 558 f-ade 8-49 d 6-abda -9 ee 754 ce 4 ac 0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Utilisation de l&#39;API de démarrage et de diffusion en continu avec les applications Livefyre {#bootstrap-stream-api}

## API Bootstrap {#bootstrap-api}

### Comment récupérer le contenu plus ancien que les 50 éléments les plus récents ? {#howcontentolder}

L&#39;amorçage est l&#39;ensemble du contenu d&#39;une application Livefyre. Il s&#39;agit des données mises en cache, généralement de 12-20 minutes. Il est livré sous forme de découpes de 50 éléments et est paginé afin que vous puissiez récupérer le contenu de plus de 50 parties.

[Référence API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exemple de requête](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

L&#39;exemple de requête ci-dessus charge la `init` page qui contient les paramètres de collection et le seul jeu initial de ~ 50 éléments de contenu le plus récent. Pour interroger le contenu plus ancien, vous devez charger les pages d&#39;amorçage suivantes avec `N` le numéro de page :

Demande : `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Par exemple, un exemple d&#39;application comporte 120 éléments de contenu. Le contenu « 1 » est le plus ancien élément de contenu et le contenu « 70 » est le plus récent.

* `Init` charge ~ 120-70 portions de contenu dans l&#39;ordre décroissant : [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` charge ~ 1-50 éléments de contenu dans l&#39;ordre croissant : [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` charge ~ 51-100 éléments de contenu dans l&#39;ordre croissant : [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` charge ~ 101-120 éléments de contenu dans l&#39;ordre croissant :[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Cliquez ici pour afficher l&#39;organigramme de sondage d&#39;amorçage.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de diffusion en continu {#stream-api}

Qu&#39;est-ce que l&#39;API de diffusion en continu ?
Le flux est un long sondage qui, par sa conception, est conçu pour rester ouvert pendant 30 secondes environ. Vous trouverez une description de la technique d&#39;interrogation longue ici : [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Ce point de fin d&#39;interrogation longue diffuse le nouveau contenu (par exemple, un utilisateur publie un commentaire), les modifications d&#39;état du contenu (par exemple, l&#39;utilisateur supprime son commentaire, ses mentions J&#39;aime) et les modifications de modération du contenu (par exemple, le modérateur approuve un élément de contenu) à une application Livefyre.

La requête de l&#39;API de diffusion en continu doit être de ~ 30 secondes (interrogation longue) avec un délai d&#39;attente attendu après 30 secondes lorsqu&#39;aucun nouveau contenu n&#39;est enchaîné.

Référence de l&#39;API : [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exemple de requête :

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Remarque : La réponse `maxEventId` d&#39;une API de diffusion en continu est l&#39;identifiant d&#39;événement le plus élevé des mises à jour dans cette réponse. Utilisez cette valeur comme `lastEventId` paramètre de chemin lors de la création de l&#39;URL de la demande de l&#39;API de diffusion en continu suivante pour obtenir des mises à jour qui se produisent après toutes les mises à jour de cette réponse.

L&#39;exemple ci-dessous repose sur une application de commentaires :

Le commentaire « Premier commentaire » a été publié en premier. « Second commentaire » a été publié après.

Réponse de l&#39;API de diffusion en continu du premier commentaire :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La `maxEventId` réponse est « 1520289700953369 » qui servira à interroger le `lastEventId` point de fin pour obtenir les mises à jour (c.-à-d. Second commentaire) se produisant après toutes les mises à jour de cette réponse.

Réponse de l&#39;API de diffusion en continu du second commentaire :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Le `maxEventID` « 1520289700953369 `lastEventID`  » de la réponse doit à son tour être utilisé comme création de la réponse de l&#39;API de diffusion en continu pour la prochaine mise à jour.