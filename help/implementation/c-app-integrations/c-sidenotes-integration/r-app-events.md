---
description: Vous pouvez écouter les événements sur une instance de l'état de Sidenotes.
seo-description: Vous pouvez écouter les événements sur une instance de l'état de Sidenotes.
seo-title: Consignation des événements d'application
solution: Experience Manager
title: Consignation des événements d'application
uuid: afca 4 b 03-c 370-41 ca-aa 12-45 bc 357517 ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Consignation des événements d&#39;application {#sidenotes-app-events}

Vous pouvez écouter les événements sur une instance de l&#39;état de Sidenotes.

Les rappels peuvent être enregistrés avec `onmethod` la `removeListener` méthode et non enregistrés. Une `once` méthode est disponible à titre de commodité si le rappel ne doit être appelé qu&#39;une seule fois, puis non enregistré.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Pour plus d&#39;informations sur les événements Livefyre, voir la page Événements JavaScript dans la section Référence.

| Clé | Description |
|--- |--- |
| sidenotes. initialized | Déclenché lorsque l&#39;application est instanciée, comporte des données et se trouve sur la page. |
| sidenotes. commentflagged | Déclenché lorsqu&#39;un commentaire a été marqué. Les données contiennent : <br><ul><li>`targetId`: id du commentaire qui a été marqué</li><li>`type`: string type string `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Déclenché lorsqu&#39;un commentaire a été publié. Les données contiennent : <br><ul><li> `authorId`: ID de l&#39;auteur du commentaire </li><li>`bodyHtml`: corps du commentaire </li><li> `parent`: id du parent du commentaire ou null</li></ul> |
| `sidenotes.commentShared` | Déclenché lorsqu&#39;un commentaire a été partagé. Les données contiennent : <br><ul><li>`targetId`: id du commentaire partagé </li><li> `sharedToFacebook`: si le commentaire a été partagé sur Facebook </li><li>`sharedToTwitter`: si le commentaire a été partagé sur Twitter</li></ul> |
| `sidenotes.commentVoted` | Déclenché lorsqu&#39;un commentaire a été voté. Les données contiennent : <br><ul><li>`targetId`: id du commentaire qui a été voté </li><li> `targetAuthorId`: id de l&#39;auteur dont le commentaire a été voté</li><li> `type`: type de vote numérique : 0 : &#39; clear &#39;, 1 : &#39; upvote&#39;ou 2 : &#39; downvote &#39;</li></ul> |
| `sidenotes.userLoggedIn` | Déclenché lorsqu&#39;un utilisateur se connecte. Les données contiennent : <br><ul><li>`avatar`: URL de l&#39;avatar pour l&#39;utilisateur </li><li>`displayName`: nom d&#39;affichage de l&#39;utilisateur</li><li>`id`: id de l&#39;utilisateur</li><li> `isModerator`: si l&#39;utilisateur est un modérateur de la collection actuelle</li></ul> |
| `sidenotes.userLoggedOut` | Déclenché lorsqu&#39;un utilisateur se déconnecte |
