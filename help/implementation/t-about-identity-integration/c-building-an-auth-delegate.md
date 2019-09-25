---
description: L’objet AuthDelegate met en oeuvre le comportement souhaité pour exécuter des actions et des événements d’authentification afin de personnaliser l’intégration au système d’authentification existant de votre site.
seo-description: L’objet AuthDelegate met en oeuvre le comportement souhaité pour exécuter des actions et des événements d’authentification afin de personnaliser l’intégration au système d’authentification existant de votre site.
seo-title: AuthDelegate, objet
solution: Experience Manager
title: AuthDelegate, objet
uuid: a6ac4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# AuthDelegate, objet{#authdelegate-object}

L’objet AuthDelegate met en oeuvre le comportement souhaité pour exécuter des actions et des événements d’authentification afin de personnaliser l’intégration au système d’authentification existant de votre site.

## Création d’un délégué d’authentification {#section_wmn_tv2_gz}

Le package d’authentification doit être fourni avec un délégué d’authentification avant de pouvoir effectuer une action. Un délégué auth est tout objet JavaScript qui implémente l’une des méthodes de cette rubrique.

## .login(finLogin) {#section_mpk_lv2_gz}

Connectez-vous à un utilisateur valide et appelez la fonction boutLogin avec un objet Error en cas d’erreur ou les informations d’identification Livefyre de l’utilisateur. Les implémentations courantes de cette méthode redirigent l’utilisateur vers une page de connexion ou ouvrent une nouvelle fenêtre ou un nouveau mode.

Cet exemple informe automatiquement l’auteur d’un utilisateur Livefyre avec le jeton d’authentification :

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Le délégué de connexion le plus simple peut demander à l’utilisateur final son jeton d’authentification Livefyre.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## .logout(finLogout) {#section_uqz_2v2_gz}

Déconnectez un utilisateur et appelez la fonction finendLogout avec un objet Error en cas d’erreur, ou null pour informer l’authentification que la déconnexion a réussi.

Par exemple :

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Prenez des mesures pour afficher le profil d’un utilisateur.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Prenez des mesures pour modifier le profil d’un utilisateur.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

En implémentant toutes les méthodes répertoriées ci-dessus, l’authentification peut être configurée avec un délégué d’authentification personnalisé. Une fois qu'un délégué a été créé, il peut être fourni à l'authentification à l'aide de la méthode déléguée.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

