---
description: Vous pouvez écouter les événements sur une instance de Sidenotes.
seo-description: Vous pouvez écouter les événements sur une instance de Sidenotes.
seo-title: Evénements d’application Sidenotes
solution: Experience Manager
title: Evénements d’application Sidenotes
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Evénements d’application Sidenotes {#sidenotes-app-events}

Vous pouvez écouter les événements sur une instance de Sidenotes.

Les rappels peuvent être enregistrés avec la `onmethod` méthode et non enregistrés avec la `removeListener` méthode. Une `once` méthode est disponible à des fins pratiques si le rappel doit être appelé une seule fois puis non enregistré.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Pour plus d’informations sur les événements Livefyre, voir la page Evénements JavaScript dans la section Référence.

| Clé | Description |
|--- |--- |
| sidenotes.initialized | Déclenché lorsque l’application est instanciée, contient des données et se trouve sur la page. |
| sidenotes.commentFlagged | Déclenché lorsqu’un commentaire a été marqué. Les données contiennent : <br><ul><li>`targetId`: ID du commentaire marqué</li><li>`type`: chaîne de type indicateur `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Déclenché lorsqu’un commentaire a été publié. Les données contiennent : <br><ul><li> `authorId`: ID de l’auteur du commentaire </li><li>`bodyHtml`: corps du commentaire </li><li> `parent`: id du parent du commentaire ou null</li></ul> |
| `sidenotes.commentShared` | Déclenché lorsqu’un commentaire a été partagé. Les données contiennent : <br><ul><li>`targetId`: ID du commentaire partagé </li><li> `sharedToFacebook`: si le commentaire a été partagé sur Facebook </li><li>`sharedToTwitter`: si le commentaire a été partagé sur Twitter</li></ul> |
| `sidenotes.commentVoted` | Déclenché lorsqu’un commentaire a été voté. Les données contiennent : <br><ul><li>`targetId`: id du commentaire qui a été voté </li><li> `targetAuthorId`: ID de l'auteur dont le commentaire a été voté</li><li> `type`: type de vote numérique:0 : "clear", 1: "upvote", ou 2: "vote négatif"</li></ul> |
| `sidenotes.userLoggedIn` | Déclenché lorsqu’un utilisateur se connecte. Les données contiennent : <br><ul><li>`avatar`: url avatar de l’utilisateur </li><li>`displayName`: nom d’affichage de l’utilisateur</li><li>`id`: ID de l’utilisateur</li><li> `isModerator`: si l’utilisateur est un modérateur de la collection active</li></ul> |
| `sidenotes.userLoggedOut` | Déclenché lorsqu’un utilisateur se déconnecte |
