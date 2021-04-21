---
description: Supprimez les composants standard de l’application Livefyre de votre application.
title: Masquer les éléments d’application
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# Masquer les éléments de l’application{#hide-app-elements}

Supprimez les composants standard de l’application Livefyre de votre application.

Utilisez CSS pour masquer les éléments par défaut de l’application Livefyre de votre page, ce qui vous permet de personnaliser l’expérience utilisateur en fonction de vos besoins.

Pour masquer des éléments de l’application, il vous suffit de définir display sur none.

Exemples :

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```
