---
description: Rendre le contenu de la communauté disponible pour les moteurs de recherche.
seo-description: Rendre le contenu de la communauté disponible pour les moteurs de recherche.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap HTML

Rendre le contenu de la communauté disponible pour les moteurs de recherche.

Pour obtenir la liste complète des points de fin disponibles, consultez la section Référence [de l’](https://api.livefyre.com/docs) API Livefyre.

Les applications Livefyre exigent que vous exécutiez du code JavaScript sur votre page pour afficher le contenu de vos collections. La plupart des moteurs de recherche ne pouvant pas exécuter JavaScript, ils ne peuvent pas voir le contenu publié par votre communauté. Utilisez l'API HTML d'amorçage pour ajouter des fragments de ce contenu pouvant faire l'objet de recherches à la réponse HTTP initiale de votre page, ce qui permet à votre contenu et à vos mots-clés d'améliorer l'optimisation de votre moteur de recherche.

>[!NOTE]
>
>Cette API est disponible uniquement pour les types de commentaires et de collection de blogs en direct.

## Intégration

L’API HTML d’amorçage de Livefyre renvoie un fragment HTML du contenu de l’utilisateur, qui peut être inclus dans la réponse HTTP de la page. Cette réponse sera lisible par les moteurs de recherche sans exécuter de code JavaScript. Une fois la page activée dans le navigateur d’un utilisateur, le fragment HTML est remplacé par le widget interactif complet et l’utilisateur peut publier du contenu.

Pour mettre en oeuvre l’API HTML d’amorçage :

1. Effectuez une requête d’API serveur à serveur vers le point de terminaison HTML Bootstrap décrit ci-dessous.

   >[!NOTE]
   >
   >Si vous essayez d’attraper le code HTML d’amorçage pour une conversation qui n’existe pas encore (c’est-à-dire si vous n’avez pas encore intégré l’application ou créé la collection), vous recevrez un 200, mais avec un contenu qui ressemble à quelque chose comme : `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Si votre déclaration ne contient pas de contenu comportant un "404", enregistrez-le dans une chaîne. Vous pouvez mettre en cache cette réponse pour une utilisation ultérieure afin d’éviter de demander l’API HTML d’amorçage sur chaque charge de page.
1. Insérez la chaîne HTML Bootstrap dans votre page Web où vous souhaitez que le contenu apparaisse.
1. Servez votre page Web dans le navigateur (ou le moteur de recherche).

## Ressource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Paramètres

* **networkName** Votre Livefyre a fourni le nom réseau. Par exemple : Des *labos* `labs.fyre.co`.
* **siteId** Identifiant du site de la collection.
* **b64articleId** ID d’article de la collection utilisant le codage base64url.

## Exemple

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Réponse

```
https://gist.github.com/ec5c2457322faf9cf515 
```
