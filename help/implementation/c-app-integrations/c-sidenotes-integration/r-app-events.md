---
description: Vous pouvez écouter les événements sur une instance de Sidenotes.
title: Identifie les Événements d’application
exl-id: e341ca76-002d-425c-8d1a-35c3253fb254
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Identifie les Événements d&#39;application {#sidenotes-app-events}

Vous pouvez écouter les événements sur une instance de Sidenotes.

Les rappels peuvent être enregistrés avec la méthode `onmethod` et non enregistrés avec la méthode `removeListener`. Une méthode `once` est disponible à des fins pratiques si le rappel doit être appelé une seule fois, puis non enregistré.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Pour plus d’informations sur les événements Livefyre, voir la page Événements JavaScript dans la section Référence.

| Clé | Description |
|--- |--- |
| sidenotes.initialized | Déclenché lorsque l’application est instanciée, contient des données et se trouve sur la page. |
| sidenotes.commentFlagged | Déclenché lorsqu’un commentaire a été marqué. Les données contiennent : <br><ul><li>`targetId`: ID du commentaire marqué</li><li>`type`: chaîne de type indicateur  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Déclenché lorsqu’un commentaire a été publié. Les données contiennent : <br><ul><li> `authorId`: ID de l’auteur du commentaire </li><li>`bodyHtml`: corps du commentaire </li><li> `parent`: id du parent du commentaire ou null</li></ul> |
| `sidenotes.commentShared` | Déclenché lorsqu’un commentaire a été partagé. Les données contiennent : <br><ul><li>`targetId`: ID du commentaire partagé </li><li> `sharedToFacebook`: si le commentaire a été partagé avec Facebook </li><li>`sharedToTwitter`: si le commentaire a été partagé avec Twitter</li></ul> |
| `sidenotes.commentVoted` | Déclenché lorsqu&#39;un commentaire a été voté. Les données contiennent : <br><ul><li>`targetId`: id du commentaire sur lequel le vote a porté </li><li> `targetAuthorId`: ID de l&#39;auteur dont le commentaire a été voté</li><li> `type`: type de vote numérique : 0 : &quot;clear&quot;, 1 : &quot;upvote&quot;, ou 2 : &quot;vote négatif&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Déclenché lorsqu’un utilisateur se connecte. Les données contiennent : <br><ul><li>`avatar`: URL d’avatar de l’utilisateur </li><li>`displayName`: nom d’affichage de l’utilisateur</li><li>`id`: ID de l’utilisateur</li><li> `isModerator`: si l’utilisateur est un modérateur de la collection active</li></ul> |
| `sidenotes.userLoggedOut` | Déclenché lorsqu’un utilisateur se déconnecte |
