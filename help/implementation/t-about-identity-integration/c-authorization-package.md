---
description: Installez le package d’authentification pour activer l’authentification des utilisateurs afin que ces derniers puissent interagir avec vos applications.
title: Package d’authentification
exl-id: 639032ee-ed7d-4cb0-83ba-f11d3dc607b6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# Package d’authentification{#authentication-package}

Installez le package d’authentification pour activer l’authentification des utilisateurs afin que ces derniers puissent interagir avec vos applications.

Les applications Livefyre utilisent le package d’authentification global pour associer les utilisateurs aux actions de l’application. Le package d&#39;authentification est disponible via `Livefyre.require`.

Pour activer l’authentification sur votre page, ajoutez d’abord `Livefyre.js` à l’élément `<head>` de votre page Web ou modèle de site Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

L&#39;utilisation de Livefyre.require pour activer l&#39;authentification est similaire à l&#39;utilisation de require pour appeler d&#39;autres packages. Le code d’intégration pour lequel une authentification est requise ressemble à ceci :

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Méthodes {#section_ojx_1lz_fz}

Une fois inclus comme indiqué ci-dessus à l&#39;aide de `Livefyre.require`, le module Auth expose les méthodes suivantes que vous pouvez appeler pour avertir d&#39;autres applications sur la page des événements liés à l&#39;authentification.

| Méthode | Description |
|--- |--- |
| `.login(callback)` | Déclenchez le flux de connexion tel qu&#39;il est implémenté par AuthDelegate enregistré. En règle générale, seules les applications activées pour l’authentification appellent ce paramètre, et non la page hôte elle-même. |
| `.logout(callback)` | Avertissez l’authentification que l’utilisateur final s’est déconnecté par un moyen externe et que toutes les applications qui dépendent doivent effacer leur état d’authentification jusqu’à la prochaine connexion. Ceci effacera la session interne gérée par Auth. |
| `.authenticate(credentials)` | Avertissez Auth qu’un utilisateur s’est authentifié par un moyen externe et qu’un jeton d’authentification Livefyre a été acheté pour l’utilisateur final. Utilisez cette option si vous définissez un cookie avec le jeton Livefyre ou si vous disposez d’un jeton pour l’utilisateur et souhaitez le connecter explicitement. Par exemple: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Déléguez les détails d’implémentation de l’authentification (par exemple, votre flux d’authentification personnalisé) à un objet que vous définissez. Ceci doit être appelé par la page hôte pour activer les fonctionnalités interactives des applications Livefyre. |
