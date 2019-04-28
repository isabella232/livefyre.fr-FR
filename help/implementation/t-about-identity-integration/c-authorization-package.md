---
description: Installez le package d'authentification pour permettre l'authentification de l'utilisateur afin que les utilisateurs puissent interagir avec vos applications.
seo-description: Installez le package d'authentification pour permettre l'authentification de l'utilisateur afin que les utilisateurs puissent interagir avec vos applications.
seo-title: Package d'authentification
solution: Experience Manager
title: Package d'authentification
uuid: 4 eec 30 cf -66 b 6-408 d -985 d -3 e 23 b 8 b 70 d 01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Package d&#39;authentification{#authentication-package}

Installez le package d&#39;authentification pour permettre l&#39;authentification de l&#39;utilisateur afin que les utilisateurs puissent interagir avec vos applications.

Les applications Livefyre utilisent le package authentique global pour associer des utilisateurs aux actions de l&#39;application. The auth package is available through `Livefyre.require`.

Pour activer l&#39;authentification sur votre page, ajoutez `Livefyre.js` d&#39;abord à `<head>` l&#39;élément de votre page Web ou modèle de site Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

L&#39;utilisation de Livefyre. require pour activer l&#39;authenticité est similaire à l&#39;utilisation de l&#39;obligation d&#39;appeler d&#39;autres packages. Le code d&#39;intégration à exiger un aspect authentique comme :

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Méthodes {#section_ojx_1lz_fz}

Une fois inclus comme ci-dessus, `Livefyre.require`le module Authentic expose les méthodes suivantes que vous pouvez appeler pour avertir d&#39;autres applications sur la page au sujet des événements liés à l&#39;authentification.

| Méthode | Description |
|--- |--- |
| `.login(callback)` | Déclenchez le flux de connexion tel qu&#39;il est implémenté par l&#39;auteur authdelegate. En général, seules les applications activées pour l&#39;authentification l&#39;appellent, et non la page d&#39;hôtes elle-même. |
| `.logout(callback)` | Avertissez-vous que l&#39;utilisateur final a déconnecté par certains moyens externes et que toutes les applications dérivées doivent effacer leur état d&#39;authentification jusqu&#39;à la prochaine connexion. Cette opération effacera la session interne gérée par Authentic. |
| `.authenticate(credentials)` | Notifier Authentique qu&#39;un utilisateur s&#39;est authentifié par certains moyens externes et qu&#39;un jeton d&#39;authentification Livefyre a été acquis pour l&#39;utilisateur final. Utilisez-le si vous définissez un cookie avec le jeton Livefyre ou que vous avez un jeton pour l&#39;utilisateur et que vous souhaitez enregistrer explicitement l&#39;utilisateur dans. Par exemple : <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Déléguez les détails d&#39;implémentation de l&#39;authentification (par exemple, votre flux d&#39;authentification personnalisée) à un objet que vous définissez. Cette opération doit être appelée par la page hôte pour activer les fonctions interactives des applications Livefyre. |

