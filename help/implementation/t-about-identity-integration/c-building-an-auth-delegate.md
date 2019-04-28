---
description: L'objet authdelegate implémente le comportement souhaité pour effectuer des actions et des événements d'authentification afin que vous puissiez personnaliser l'intégration au système d'authentification existant de votre site.
seo-description: L'objet authdelegate implémente le comportement souhaité pour effectuer des actions et des événements d'authentification afin que vous puissiez personnaliser l'intégration au système d'authentification existant de votre site.
seo-title: Authdelegate Object
solution: Experience Manager
title: Authdelegate Object
uuid: a 6 acc 4 ef-d 442-4782-9 bfa-bbe 494547 c 2 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Authdelegate Object{#authdelegate-object}

L&#39;objet authdelegate implémente le comportement souhaité pour effectuer des actions et des événements d&#39;authentification afin que vous puissiez personnaliser l&#39;intégration au système d&#39;authentification existant de votre site.

## Création d&#39;un délégué authentique {#section_wmn_tv2_gz}

Le pack authentique doit être fourni avec un délégué authentique avant de pouvoir effectuer une action. Un délégué authentique est un objet JavaScript qui implémente l&#39;une des méthodes de cette rubrique.

## . login (finishlogin) {#section_mpk_lv2_gz}

Connectez un utilisateur valide et appelez la fonction finishlogin avec un objet Error en cas d&#39;erreur ou les informations d&#39;identification Livefyre de l&#39;utilisateur. Les implémentations courantes de cette méthode redirigent l&#39;utilisateur vers une page de connexion ou ouvrent une nouvelle fenêtre ou un nouveau modal.

Cet exemple avertit automatiquement l&#39;authenticité d&#39;un utilisateur Livefyre avec le jeton d&#39;authentification, jeton :

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Le délégué de connexion le plus simple peut demander à l&#39;utilisateur final de se servir de son jeton d&#39;authentification Livefyre.

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

## . déconnexion (finishlogout) {#section_uqz_2v2_gz}

Déconnectez un utilisateur et appelez la fonction finishlogout avec un objet Error en cas d&#39;erreur ou null pour avertir l&#39;authenticité de la déconnexion.

Par exemple :

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . Viewprofile (utilisateur) {#section_kkv_dv2_gz}

Prenez les mesures nécessaires pour afficher le profil d&#39;un utilisateur.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . Editprofile (utilisateur) {#section_bkx_pq2_gz}

Prenez une décision pour modifier le profil d&#39;un utilisateur.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

En implémentant toutes les méthodes répertoriées ci-dessus, il est possible de configurer authentique avec un délégué authentique personnalisé. Une fois qu&#39;un délégué a été construit, il peut être fourni à l&#39;authentique à l&#39;aide de la méthode déléguée.

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

