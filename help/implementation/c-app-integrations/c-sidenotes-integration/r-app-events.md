---
description: Vous pouvez écouter les événements sur une instance de l'état de Sidenotes.
seo-description: Vous pouvez écouter les événements sur une instance de l'état de
  Sidenotes.
seo-title: Consignation des événements d'application
solution: Experience Manager
title: Consignation des événements d'application
uuid: afca 4 b 03-c 370-41 ca-aa 12-45 bc 357517 ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Consignation des événements d'application {#sidenotes-app-events}

Vous pouvez écouter les événements sur une instance de l'état de Sidenotes.

Les rappels peuvent être enregistrés avec `onmethod` la `removeListener` méthode et non enregistrés. Une `once` méthode est disponible à titre de commodité si le rappel ne doit être appelé qu'une seule fois, puis non enregistré.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Pour plus d'informations sur les événements Livefyre, voir la page Événements JavaScript dans la section Référence.

| Clé | Description |
|--- |--- |
| sidenotes. initialized | Déclenché lorsque l'application est instanciée, comporte des données et se trouve sur la page. |
| sidenotes. commentflagged | Déclenché lorsqu'un commentaire a été marqué. Les données contiennent : <br><ul><li>`targetId`: id du commentaire qui a été marqué</li><li>`type`: string type string `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Déclenché lorsqu'un commentaire a été publié. Les données contiennent : <br><ul><li> `authorId`: ID de l'auteur du commentaire </li><li>`bodyHtml`: corps du commentaire </li><li> `parent`: id du parent du commentaire ou null</li></ul> |
| `sidenotes.commentShared` | Déclenché lorsqu'un commentaire a été partagé. Les données contiennent : <br><ul><li>`targetId`: id du commentaire partagé </li><li> `sharedToFacebook`: si le commentaire a été partagé sur Facebook </li><li>`sharedToTwitter`: si le commentaire a été partagé sur Twitter</li></ul> |
| `sidenotes.commentVoted` | Déclenché lorsqu'un commentaire a été voté. Les données contiennent : <br><ul><li>`targetId`: id du commentaire qui a été voté </li><li> `targetAuthorId`: id de l'auteur dont le commentaire a été voté</li><li> `type`: type de vote numérique : 0 : ' clear ', 1 : ' upvote'ou 2 : ' downvote '</li></ul> |
| `sidenotes.userLoggedIn` | Déclenché lorsqu'un utilisateur se connecte. Les données contiennent : <br><ul><li>`avatar`: URL de l'avatar pour l'utilisateur </li><li>`displayName`: nom d'affichage de l'utilisateur</li><li>`id`: id de l'utilisateur</li><li> `isModerator`: si l'utilisateur est un modérateur de la collection actuelle</li></ul> |
| `sidenotes.userLoggedOut` | Déclenché lorsqu'un utilisateur se déconnecte |
