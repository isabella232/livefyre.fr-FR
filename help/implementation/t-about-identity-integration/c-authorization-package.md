---
description: Installez le package d’authentification afin d’activer l’authentification des utilisateurs afin qu’ils puissent interagir avec vos applications.
seo-description: Installez le package d’authentification afin d’activer l’authentification des utilisateurs afin qu’ils puissent interagir avec vos applications.
seo-title: Package d’authentification
solution: Experience Manager
title: Package d’authentification
uuid: 4ec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Package d’authentification{#authentication-package}

Installez le package d’authentification afin d’activer l’authentification des utilisateurs afin qu’ils puissent interagir avec vos applications.

Les applications Livefyre utilisent le package d’authentification global pour associer les utilisateurs aux actions de l’application. Le package d’authentification est disponible via `Livefyre.require`.

Pour activer l’authentification sur votre page, ajoutez d’abord `Livefyre.js` à l’ `<head>` élément de votre page Web ou modèle de site Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

L’utilisation de Livefyre.require pour activer l’authentification est similaire à l’utilisation de require pour appeler d’autres packages. Le code d’intégration pour exiger une authentification se présente comme suit :

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Méthodes {#section_ojx_1lz_fz}

Une fois inclus comme indiqué ci-dessus `Livefyre.require`, le module Auth expose les méthodes suivantes que vous pouvez appeler pour avertir d’autres applications de la page des événements liés à l’authentification.

| Méthode | Description |
|--- |--- |
| `.login(callback)` | Déclenchez le flux de connexion tel qu’il est implémenté par AuthDelegate enregistré. En règle générale, seules les applications activées pour l’authentification appellent ce paramètre, et non la page hôte elle-même. |
| `.logout(callback)` | Avertissez l’utilisateur que l’utilisateur final s’est déconnecté par un moyen externe et que toutes les applications de confiance doivent effacer leur état d’authentification jusqu’à la prochaine connexion. Ceci effacera la session interne conservée par Auth. |
| `.authenticate(credentials)` | Avertissez Auth qu’un utilisateur s’est authentifié par un moyen externe et qu’un jeton d’authentification Livefyre a été acheté pour l’utilisateur final. Utilisez cette option si vous définissez un cookie avec le jeton Livefyre ou si vous disposez d’un jeton pour l’utilisateur et souhaitez le connecter explicitement. For example: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Déléguez les détails d’implémentation de l’authentification (par exemple, votre flux d’authentification personnalisé) à un objet que vous définissez. Ceci doit être appelé par la page hôte pour activer les fonctionnalités interactives des applications Livefyre. |

