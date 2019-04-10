---
description: Utilisez les événements Javascript pour écouter les événements qui se
  produisent dans un mur multimédia et les envoyer à l'outil d'analyse de votre choix.
seo-description: Utilisez les événements Javascript pour écouter les événements qui
  se produisent dans un mur multimédia et les envoyer à l'outil d'analyse de votre
  choix.
seo-title: Événements javascript pour le mur multimédia
solution: Experience Manager
title: Événements javascript pour le mur multimédia
uuid: 8 afc 0529-4640-476 a-b 207-91 b 2 c 70101 f 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Événements javascript pour le mur multimédia{#javascript-events-for-media-wall}

Utilisez les événements Javascript pour écouter les événements qui se produisent dans un mur multimédia et les envoyer à l'outil d'analyse de votre choix.

Livefyre fournit des événements JavaScript pour effectuer le suivi de l'activité des utilisateurs dans vos applications Livefyre. Par exemple, vous pouvez mettre à jour la page lorsque des utilisateurs aiment ou partagent du contenu sur Twitter ou Facebook, ou lorsque du nouveau contenu est publié.

Voici un exemple de réception des événements. Remplacez `console.log` le code par votre code pour mapper et envoyez l'événement à votre intégration Analytics (gestion dynamique des balises, Adobe Analytics JS, Google Analytics, etc.) :

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Liste des événements de mur multimédia pris en charge :

## Événements du mur multimédia

| Evénement | Définition |
|---|---|
| `Init` | Lorsqu'un mur multimédia est inclus sur une page. |
| `Load` | Lorsque le mur multimédia a été chargé sur une page, quelle que soit sa position. |
| `PostButtonClick` | Lorsqu'un utilisateur clique sur un bouton de téléchargement sur un mur multimédia. |
| `RequestMore` | Lorsque l'utilisateur charge plus de contenu dans un mur multimédia. |
| `TwitterReplyClick` | Lorsqu'un utilisateur clique sur le bouton Réponse Twitter du mur multimédia. |
| `TwitterRetweetClick` | Lorsqu'un utilisateur clique sur le bouton Retweet Twitter à partir du mur multimédia. |
| `TwitterLikeClick` | Lorsqu'un utilisateur clique sur le bouton J'aime/favori Twitter à partir du mur multimédia. |
| `ModalView` | Lorsque l'utilisateur clique pour afficher le contenu du mur multimédia dans une fenêtre modale plus grande. |
| `Like` | Lorsqu'un utilisateur clique sur le bouton J'aime à partir du mur multimédia. |
| `ShareButtonClick` | Chaque fois qu'un utilisateur clique sur le bouton Partager sur une carte du mur multimédia. |
| `ShareURL` | Lorsque Partager sur l'URL est sélectionné/copié à partir du mur multimédia. |
| `ShareFacebook` | Lorsque vous cliquez sur Partager sur Facebook, cliquez sur le mur multimédia. |
| `ShareTwitter` | Lorsque Partager sur Twitter est cliqué à partir du mur multimédia. |
