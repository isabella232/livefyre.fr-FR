---
description: Utilisez des événements JavaScript pour écouter les événements qui se produisent dans une paroi multimédia et les envoyer à l’outil d’analyse de votre choix.
title: Événements JavaScript pour la paroi multimédia
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Événements Javascript pour Media Wall{#javascript-events-for-media-wall}

Utilisez des événements JavaScript pour écouter les événements qui se produisent dans une paroi multimédia et les envoyer à l’outil d’analyse de votre choix.

Livefyre fournit des événements JavaScript pour suivre l’activité des utilisateurs dans vos applications Livefyre. Par exemple, vous pouvez mettre à jour la page lorsque les utilisateurs aiment ou partagent du contenu sur Twitter ou Facebook, ou lorsque du nouveau contenu est publié.

Voici un exemple de la façon de recevoir les événements. Remplacez `console.log` par votre code pour mapper et envoyer le événement à votre intégration d’analyse (gestion dynamique des balises, Adobe Analytics JS, Google Analytics, etc.) :

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Liste des événements de mur multimédia pris en charge :

## Événements de mur multimédia

| Evénement | Définition |
|---|---|
| `Init` | Lorsqu’une paroi multimédia est incluse sur une page. |
| `Load` | Lorsque le mur multimédia était chargé sur une page, quelle que soit sa position. |
| `PostButtonClick` | Lorsqu’un utilisateur clique sur un bouton de téléchargement sur un mur multimédia. |
| `RequestMore` | Lorsque l’utilisateur charge davantage de contenu dans une paroi multimédia. |
| `TwitterReplyClick` | Lorsqu’un utilisateur clique sur le bouton Répondre Twitter du mur multimédia. |
| `TwitterRetweetClick` | Lorsqu’un utilisateur clique sur le bouton Retweet Twitter du mur multimédia. |
| `TwitterLikeClick` | Lorsqu’un utilisateur clique sur le bouton J’aime/Favori de Twitter du mur multimédia. |
| `ModalView` | Lorsque l’utilisateur clique pour vue du contenu du mur multimédia dans une fenêtre modale plus grande. |
| `Like` | Lorsqu’un utilisateur clique sur le bouton J’aime du mur multimédia. |
| `ShareButtonClick` | Chaque fois qu’un utilisateur clique sur le bouton de partage d’une carte de mur multimédia. |
| `ShareURL` | Lorsque la zone de texte Partager sur l’URL est sélectionnée/copiée à partir du mur multimédia. |
| `ShareFacebook` | Lorsque vous cliquez sur Partager sur Facebook à partir du mur multimédia. |
| `ShareTwitter` | Lorsque vous cliquez sur Partager sur Twitter à partir du mur multimédia. |
