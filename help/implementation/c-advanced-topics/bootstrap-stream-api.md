---
description: Utilisez l’API Bootstrap et Stream avec les applications Livefyre.
title: Affichage des détails du compte
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Utilisation de l’API Bootstrap et Stream avec les applications Livefyre {#bootstrap-stream-api}

## API Bootstrap {#bootstrap-api}

### Comment récupérer du contenu plus ancien que les 50 dernières pièces ? {#howcontentolder}

Bootstrap est tout le contenu d’une application Livefyre. Il s’agit des données mises en cache, qui datent généralement de 12 à 20 minutes. Elle est distribuée en blocs de 50 éléments et est paginée afin que vous puissiez récupérer du contenu de plus de 50 éléments.

[Référence d’API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exemple de requête](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

L’exemple de requête ci-dessus charge la page `init` qui contient les paramètres de la collection et le seul ensemble initial de ~50 éléments de contenu le plus récent. Pour interroger un contenu plus ancien, vous devez charger les pages de bootstrap suivantes en indiquant que `N` est le numéro de page :

Demande: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Par exemple, un exemple d’application comporte 120 éléments de contenu. Le contenu &quot;1&quot; est l’élément de contenu le plus ancien et le contenu &quot;70&quot; est l’élément de contenu le plus récent.

* `Init` chargera ~120 à 70 éléments de contenu dans l’ordre décroissant :  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` chargera entre 1 et 50 éléments de contenu dans l’ordre croissant :  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json`
* `1.json` chargera entre 51 et 100 éléments de contenu dans l’ordre croissant :  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json`
* `2.json` chargera ~101-120 éléments de contenu dans l’ordre croissant :`https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json`

[Cliquez ici pour voir l’organigramme du sondage Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de diffusion {#stream-api}

Qu’est-ce que l’API de diffusion ?
Le flux est un long sondage qui, par conception, est conçu pour rester ouvert pendant environ 30 secondes. Description de la technique d’interrogation longue ici : [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Ce point de fin d’interrogation long diffuse du nouveau contenu (par exemple, un utilisateur publie un commentaire), des modifications d’état du contenu (par exemple, l’utilisateur supprime son commentaire, ses mentions J’aime) et des modifications de modération du contenu (par exemple, le modérateur approuve un élément de contenu) vers une application Livefyre.

L’API de demande de diffusion en continu doit être d’environ 30 secondes (interrogation longue) avec un délai d’attente attendu au bout de 30 secondes lorsqu’aucun nouveau contenu n’est diffusé en continu.

Référence d’API : [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:opérations:v3.1:collection:mises à jour:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exemple de requête :

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Remarque : `maxEventId` dans une réponse de l’API de diffusion en continu est l’identifiant d’événement le plus élevé des mises à jour de cette réponse. Utilisez cette valeur comme paramètre de chemin `lastEventId` lors de la création de l’URL de votre prochaine requête d’API de diffusion pour obtenir des mises à jour survenant après toutes les mises à jour de cette réponse.

L’exemple ci-dessous est basé sur une application Comments :

Commentaire &quot;Premier commentaire&quot; a été publié en premier. &quot;Second Comment&quot; a ensuite été publié.

Réponse de l’API First Comment Stream :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

`maxEventId` dans la réponse est &quot;1520289700953369&quot;, qui sera utilisé comme `lastEventId` pour interroger le point de terminaison afin d’obtenir des mises à jour (c’est-à-dire le deuxième commentaire) après toutes les mises à jour de cette réponse.

Deuxième réponse de l’API de diffusion de commentaires :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La balise `maxEventID` &quot;1520289700953369&quot; de la réponse doit à son tour être utilisée comme `lastEventID` pour créer la réponse de l’API de diffusion pour la prochaine mise à jour.
