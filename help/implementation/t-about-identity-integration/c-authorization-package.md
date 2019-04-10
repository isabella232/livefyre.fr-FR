---
description: Installez le package d'authentification pour permettre l'authentification
  de l'utilisateur afin que les utilisateurs puissent interagir avec vos applications.
seo-description: Installez le package d'authentification pour permettre l'authentification
  de l'utilisateur afin que les utilisateurs puissent interagir avec vos applications.
seo-title: Package d'authentification
solution: Experience Manager
title: Package d'authentification
uuid: 4 eec 30 cf -66 b 6-408 d -985 d -3 e 23 b 8 b 70 d 01
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Package d'authentification{#authentication-package}

Installez le package d'authentification pour permettre l'authentification de l'utilisateur afin que les utilisateurs puissent interagir avec vos applications.

Les applications Livefyre utilisent le package authentique global pour associer des utilisateurs aux actions de l'application. The auth package is available through `Livefyre.require`.

Pour activer l'authentification sur votre page, ajoutez `Livefyre.js` d'abord à `<head>` l'élément de votre page Web ou modèle de site Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

L'utilisation de Livefyre. require pour activer l'authenticité est similaire à l'utilisation de l'obligation d'appeler d'autres packages. Le code d'intégration à exiger un aspect authentique comme :

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Méthodes {#section_ojx_1lz_fz}

Une fois inclus comme ci-dessus, `Livefyre.require`le module Authentic expose les méthodes suivantes que vous pouvez appeler pour avertir d'autres applications sur la page au sujet des événements liés à l'authentification.

| Méthode | Description |
|--- |--- |
| `.login(callback)` | Déclenchez le flux de connexion tel qu'il est implémenté par l'auteur authdelegate. En général, seules les applications activées pour l'authentification l'appellent, et non la page d'hôtes elle-même. |
| `.logout(callback)` | Avertissez-vous que l'utilisateur final a déconnecté par certains moyens externes et que toutes les applications dérivées doivent effacer leur état d'authentification jusqu'à la prochaine connexion. Cette opération effacera la session interne gérée par Authentic. |
| `.authenticate(credentials)` | Notifier Authentique qu'un utilisateur s'est authentifié par certains moyens externes et qu'un jeton d'authentification Livefyre a été acquis pour l'utilisateur final. Utilisez-le si vous définissez un cookie avec le jeton Livefyre ou que vous avez un jeton pour l'utilisateur et que vous souhaitez enregistrer explicitement l'utilisateur dans. Par exemple : <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Déléguez les détails d'implémentation de l'authentification (par exemple, votre flux d'authentification personnalisée) à un objet que vous définissez. Cette opération doit être appelée par la page hôte pour activer les fonctions interactives des applications Livefyre. |

