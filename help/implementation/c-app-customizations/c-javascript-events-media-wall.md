---
description: Utilisez les événements Javascript pour écouter les événements qui se produisent dans un mur multimédia et les envoyer à l’outil d’analyse de votre choix.
seo-description: Utilisez les événements Javascript pour écouter les événements qui se produisent dans un mur multimédia et les envoyer à l’outil d’analyse de votre choix.
seo-title: Evénements JavaScript pour Media Wall
solution: Experience Manager
title: Evénements JavaScript pour Media Wall
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Evénements JavaScript pour Media Wall{#javascript-events-for-media-wall}

Utilisez les événements Javascript pour écouter les événements qui se produisent dans un mur multimédia et les envoyer à l’outil d’analyse de votre choix.

Livefyre fournit des événements JavaScript pour suivre l’activité des utilisateurs dans vos applications Livefyre. Par exemple, vous pouvez souhaiter mettre à jour la page lorsque les utilisateurs aiment ou partagent du contenu sur Twitter ou Facebook, ou lorsque du nouveau contenu est publié.

Voici un exemple de réception des événements. Remplacez `console.log` par votre code pour mapper et envoyer l’événement à votre intégration Analytics (gestion dynamique des balises, Adobe Analytics JS, Google Analytics, etc.) :

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Liste des événements Media Wall pris en charge :

## Evénements du mur multimédia

| Evénement | Définition |
|---|---|
| `Init` | Lorsqu’une paroi multimédia est incluse dans une page. |
| `Load` | Lorsque le mur multimédia était chargé sur une page, quelle que soit sa position. |
| `PostButtonClick` | Lorsqu’un utilisateur clique sur un bouton de téléchargement sur un mur multimédia. |
| `RequestMore` | Lorsque l’utilisateur charge davantage de contenu dans une zone de support. |
| `TwitterReplyClick` | Lorsqu’un utilisateur clique sur le bouton Répondre à Twitter à partir du mur multimédia. |
| `TwitterRetweetClick` | Lorsqu’un utilisateur clique sur le bouton Retweet Twitter dans le mur multimédia. |
| `TwitterLikeClick` | Lorsqu’un utilisateur clique sur le bouton J’aime/Favori de Twitter à partir du mur multimédia. |
| `ModalView` | Lorsque l’utilisateur clique pour afficher le contenu du mur multimédia dans une fenêtre modale plus grande. |
| `Like` | Lorsqu’un utilisateur clique sur le bouton J’aime du mur multimédia. |
| `ShareButtonClick` | Chaque fois qu’un utilisateur clique sur le bouton de partage d’une carte Mur des supports. |
| `ShareURL` | Lorsque la zone de texte Partager sur l’URL est sélectionnée/copiée à partir du mur multimédia. |
| `ShareFacebook` | Lorsque vous cliquez sur Partager sur Facebook à partir du mur multimédia. |
| `ShareTwitter` | Lorsque l’utilisateur clique sur Partager sur Twitter à partir du mur multimédia. |
