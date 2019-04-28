---
description: Supprimez les composants standard de l'application Livefyre de votre application.
seo-description: Supprimez les composants standard de l'application Livefyre de votre application.
seo-title: Masquer les éléments d'application
solution: Experience Manager
title: Masquer les éléments d'application
uuid: ea 090 b 6 e -99 f 5-4 bd 7-aa 9 e-d 39 a 4 dff 1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Masquer les éléments d&#39;application{#hide-app-elements}

Supprimez les composants standard de l&#39;application Livefyre de votre application.

Utilisez CSS pour masquer les éléments d&#39;application Livefyre par défaut de votre page, ce qui vous permet de personnaliser l&#39;expérience utilisateur en fonction de vos besoins.

Pour masquer les éléments de l&#39;application, il suffit de les définir sur Aucun.

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

