---
description: Utilisez l’API Bootstrap et Stream avec les applications Livefyre.
title: Affichage des détails du compte
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Utilisation de l’API Bootstrap et Stream avec les applications Livefyre {#bootstrap-stream-api}

## API du Bootstrap {#bootstrap-api}

### Comment puis-je récupérer du contenu plus ancien que les 50 dernières pièces ? {#howcontentolder}

Le Bootstrap est tout le contenu d’une application Livefyre. Il s’agit des données mises en cache, qui datent généralement de 12 à 20 minutes. Il est livré en morceaux de 50 pièces et est paginé afin que vous puissiez récupérer du contenu plus ancien que 50 pièces.

[Référence d’API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exemple de demande](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

L’exemple de requête ci-dessus charge la page `init` qui contient les paramètres de collection et le seul jeu initial d’environ 50 éléments de contenu le plus récent. Pour interroger un contenu plus ancien, vous devez charger les pages d&#39;amorçage suivantes avec `N` comme numéro de page :

Demande: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Par exemple, un exemple d’application comporte 120 éléments de contenu. Le contenu &quot;1&quot; est l’élément de contenu le plus ancien et le contenu &quot;70&quot; est l’élément de contenu le plus récent.

* `Init` chargera ~120 à 70 éléments de contenu dans l’ordre décroissant :  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` chargera ~ 1 à 50 éléments de contenu dans l’ordre croissant :  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` chargera environ 51 à 100 éléments de contenu dans l’ordre croissant :  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` chargera ~101 à 120 éléments de contenu dans l’ordre croissant :[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Cliquez ici pour voir l&#39;organigramme du sondage Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de diffusion en continu {#stream-api}

Qu’est-ce que l’API de diffusion en continu ?
Le flux est un long sondage qui, par conception, est destiné à rester ouvert pendant environ 30 secondes. Vous trouverez ici une description de la technique d&#39;interrogation longue : [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Ce point de terminaison d’interrogation long diffuse du nouveau contenu (par exemple, un utilisateur publie un commentaire), des modifications d’état du contenu (par exemple, l’utilisateur supprime son commentaire, ses mentions J’aime) et des modifications de modération du contenu (par exemple, le modérateur approuve un élément de contenu) dans une application Livefyre.

La demande d’API de diffusion en continu doit être d’environ 30 secondes (interrogation longue) avec le délai d’attente attendu après 30 secondes lorsqu’aucun nouveau contenu n’est diffusé en continu.

Référence de l&#39;API : [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exemple de demande :

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Remarque : La réponse `maxEventId` d&#39;une API de diffusion en continu est l&#39;ID de Événement le plus élevé des mises à jour de cette réponse. Utilisez cette valeur comme paramètre de chemin d’accès `lastEventId` lors de la création de l’URL de votre prochaine requête d’API de diffusion en continu pour obtenir des mises à jour survenant après toutes les mises à jour de cette réponse.

L’exemple ci-dessous est basé sur une application de commentaires :

Commentaire &quot;Premier commentaire&quot; a été publié en premier. &quot;Deuxième commentaire&quot; a été publié après.

Réponse de l’API de flux de commentaires :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Le `maxEventId` de la réponse est &quot;1520289700953369&quot; qui sera utilisé comme `lastEventId` pour interroger le point de terminaison afin d’obtenir des mises à jour (c.-à-d. le deuxième commentaire) après toutes les mises à jour de cette réponse.

Deuxième réponse de l’API de flux de commentaires :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La réponse `maxEventID` &quot;1520289700953369&quot; doit à son tour être utilisée comme `lastEventID` réponse de l’API de diffusion en continu pour la prochaine mise à jour.
