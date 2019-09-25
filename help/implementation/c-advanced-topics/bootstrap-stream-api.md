---
description: Utilisez Bootstrap et Stream API avec les applications Livefyre.
seo-description: Utilisez Bootstrap et Stream API avec les applications Livefyre.
seo-title: Utilisation de l’API de démarrage et de diffusion en continu avec les applications Livefyre
solution: Experience Manager
title: Affichage des détails d’un compte
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Utilisation de l’API de démarrage et de diffusion en continu avec les applications Livefyre {#bootstrap-stream-api}

## API d'amorçage {#bootstrap-api}

### Comment puis-je récupérer du contenu plus ancien que les 50 dernières pièces ? {#howcontentolder}

Bootstrap est tout le contenu d’une application Livefyre. Il s’agit des données mises en cache, qui datent généralement de 12 à 20 minutes. Il est livré en morceaux de 50 pièces et paginé afin que vous puissiez récupérer le contenu de plus de 50 pièces.

[Référence d’API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exemple de requête](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

L’exemple de requête ci-dessus charge la `init` page qui contient les paramètres de collection et le seul jeu initial d’environ 50 éléments de contenu le plus récent. Pour sonder un contenu plus ancien, vous devez charger les pages d’amorçage suivantes avec `N` le numéro de page :

Demande: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Par exemple, un exemple d’application comporte 120 éléments de contenu. Le contenu "1" est l’élément de contenu le plus ancien et le contenu "70" est l’élément de contenu le plus récent.

* `Init` chargera ~120 à 70 éléments de contenu dans l’ordre décroissant : [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` chargera ~ 1 à 50 éléments de contenu dans l’ordre croissant : [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` chargera entre 51 et 100 éléments de contenu dans l’ordre croissant : [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` chargera ~101 à 120 éléments de contenu dans un ordre croissant:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Cliquez ici pour voir l'organigramme du sondage Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de diffusion {#stream-api}

Qu’est-ce que l’API de diffusion en continu ?
Le flux est un long sondage qui, par dessein, doit rester ouvert pendant environ 30 secondes. Vous trouverez ici une description de la technique d’interrogation longue : [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Ce point de fin de sondage long diffuse du nouveau contenu (par exemple, un utilisateur publie un commentaire), des modifications d’état du contenu (par exemple, l’utilisateur supprime son commentaire, ses mentions J’aime) et des modifications de modération du contenu (par exemple, un modérateur approuve un élément de contenu) dans une application Livefyre.

La demande d’API de diffusion en continu doit être d’environ 30 secondes (interrogation longue) avec un délai d’attente attendu après 30 secondes lorsqu’aucun nouveau contenu n’est diffusé en flux continu.

Référence API : [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exemple de requête :

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Veuillez noter : La réponse `maxEventId` dans une API de diffusion en continu est l’ID d’événement le plus élevé des mises à jour de cette réponse. Utilisez cette valeur comme paramètre de `lastEventId` chemin lors de la création de l’URL de votre prochaine requête d’API de diffusion en continu pour obtenir des mises à jour survenant après toutes les mises à jour de cette réponse.

L’exemple ci-dessous est basé sur une application de commentaires :

Commentaire "Premier commentaire" a été publié en premier. "Deuxième commentaire" a été posté après.

Réponse de l’API de flux de commentaires initial :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La réponse `maxEventId` est "1520289700953369", qui sera utilisée `lastEventId` pour interroger le point de terminaison afin d’obtenir des mises à jour (deuxième commentaire) après toutes les mises à jour de cette réponse.

Réponse de l’API de flux de commentaires secondaire :

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Le `maxEventID` "1520289700953369" dans la réponse doit à son tour être utilisé comme `lastEventID` pour créer la réponse de l’API de diffusion en continu pour la prochaine mise à jour.