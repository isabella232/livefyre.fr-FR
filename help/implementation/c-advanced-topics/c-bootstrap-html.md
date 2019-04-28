---
description: Rendre le contenu de la communauté accessible aux moteurs de balayage des moteurs de recherche.
seo-description: Rendre le contenu de la communauté accessible aux moteurs de balayage des moteurs de recherche.
seo-title: Code HTML d'amorçage
solution: Experience Manager
title: Code HTML d'amorçage
uuid: 137 e 4382-4 e 7 b -4124-9 d 35-1 d 872 a 497 bc 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Code HTML d&#39;amorçage

Rendre le contenu de la communauté accessible aux moteurs de balayage des moteurs de recherche.

Pour obtenir la liste complète des points de fin disponibles, consultez la section [Référence](https://api.livefyre.com/docs) de l&#39;API Livefyre.

Les applications Livefyre requièrent que vous exécutiez JavaScript sur votre page pour afficher le contenu de vos collections. Comme la plupart des moteurs de balayage des moteurs de recherche ne peuvent pas exécuter JavaScript, ils ne peuvent pas voir le contenu que vos publications ont publié. Utilisez l&#39;API HTML d&#39;amorçage pour ajouter des fragments indexables de ce contenu à la réponse HTTP initiale de votre page, ce qui permet d&#39;améliorer l&#39;optimisation du moteur de recherche dans votre contenu et vos mots-clés.

>[!NOTE]
>
>Cette API est disponible uniquement pour les types Commentaires et Collection de blog en direct.

## Analytics

L&#39;API HTML d&#39;amorçage Livefyre renvoie un fragment HTML de votre contenu utilisateur qui peut être inclus dans la réponse HTTP de la page. Cette réponse sera lisible par les moteurs de balayage des moteurs de recherche sans exécuter de code JavaScript. Une fois que la page est active dans le navigateur d&#39;un utilisateur, le fragment HTML est remplacé par le widget interactif complet et l&#39;utilisateur pourra publier du contenu.

Pour mettre en œuvre l&#39;API HTML d&#39;amorçage :

1. Faites d&#39;un serveur la demande d&#39;API serveur au endpoint de terminaison HTML Bootstrap documenté ci-dessous.

   >[!NOTE]
   >
   >Si vous essayez de saisir le code HTML d&#39;amorçage pour une conversation qui n&#39;existe pas encore (c&#39;est-à-dire si vous n&#39;avez pas encore incorporé l&#39;application ou créez la collection), vous recevrez un 200, mais avec un contenu qui ressemble à ceci : `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Si votre retour n&#39;inclut pas de contenu avec un « 404 », enregistrez-le dans une chaîne. Vous pouvez mettre en cache cette réponse pour une utilisation ultérieure afin d&#39;éviter de demander l&#39;API HTML Bootstrap sur chaque pageload.
1. Insérez la chaîne HTML Bootstrap dans votre webpage Web dans laquelle le contenu doit apparaître.
1. Diffusez votre page Web au navigateur (ou moteur de recherche du moteur de recherche).

## Ressource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Paramètres

* **Networkname** Votre nom de réseau fourni. Par exemple : *labs* in `labs.fyre.co`.
* **ID de site** ID de site de la collection.
* **b 64 articleid** ID d&#39;article de la collection à l&#39;aide du codage d&#39;URL base 64.

## Exemple

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Réponse

```
https://gist.github.com/ec5c2457322faf9cf515 
```
