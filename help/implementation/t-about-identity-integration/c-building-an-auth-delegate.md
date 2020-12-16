---
description: L’objet AuthDelegate met en oeuvre le comportement souhaité pour l’exécution d’actions et de événements d’authentification afin que vous puissiez personnaliser l’intégration avec le système d’authentification existant de votre site.
seo-description: L’objet AuthDelegate met en oeuvre le comportement souhaité pour l’exécution d’actions et de événements d’authentification afin que vous puissiez personnaliser l’intégration avec le système d’authentification existant de votre site.
seo-title: AuthDelegate, objet
solution: Experience Manager
title: AuthDelegate, objet
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# AuthDelegate, objet{#authdelegate-object}

L’objet AuthDelegate met en oeuvre le comportement souhaité pour l’exécution d’actions et de événements d’authentification afin que vous puissiez personnaliser l’intégration avec le système d’authentification existant de votre site.

## Création d&#39;un délégué d&#39;authentification {#section_wmn_tv2_gz}

Le package d&#39;authentification doit être fourni avec un délégué d&#39;authentification pour pouvoir exécuter une action. Un délégué d’authentification est tout objet JavaScript qui implémente l’une des méthodes de cette rubrique.

## .login(endLogin) {#section_mpk_lv2_gz}

Connectez-vous à un utilisateur valide et appelez la fonction endLogin avec un objet Error en cas d’erreur ou les informations d’identification Livefyre de l’utilisateur. Les implémentations courantes de cette méthode redirigent l’utilisateur vers une page de connexion ou ouvrent une nouvelle fenêtre ou un nouveau module.

Cet exemple montre comment avertir automatiquement l&#39;auteur d&#39;un utilisateur Livefyre avec le jeton d&#39;authentification :

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

## {#section_uqz_2v2_gz}

Déconnectez un utilisateur et appelez la fonction endLogout avec un objet Error en cas d’erreur, ou null pour signaler à l’authentification que la déconnexion a réussi.

Par exemple :

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Prendre des mesures pour vue le profil d’un utilisateur.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Effectuez une action pour modifier le profil d’un utilisateur.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

En implémentant toutes les méthodes répertoriées ci-dessus, l’authentification peut être configurée avec un délégué d’authentification personnalisé. Une fois qu&#39;un délégué a été créé, il peut être fourni à l&#39;authentification à l&#39;aide de la méthode delegate.

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

