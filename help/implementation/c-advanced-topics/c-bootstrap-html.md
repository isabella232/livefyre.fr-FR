---
description: Mettez le contenu de la communauté à la disposition des moteurs de recherche.
seo-description: Mettez le contenu de la communauté à la disposition des moteurs de recherche.
seo-title: HTML Bootstrap
solution: Experience Manager
title: HTML Bootstrap
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 1%

---


# HTML Bootstrap

Mettez le contenu de la communauté à la disposition des moteurs de recherche.

Pour obtenir la liste complète des points de terminaison disponibles, consultez la section Livefyre [Référence API](https://api.livefyre.com/docs).

Les applications Livefyre exigent que vous exécutiez du code JavaScript sur votre page pour afficher le contenu de vos collections. La plupart des moteurs de recherche ne pouvant pas exécuter JavaScript, ils ne peuvent pas voir le contenu publié par votre communauté. Utilisez l&#39;API HTML du Bootstrap pour ajouter des fragments de ce contenu pouvant faire l&#39;objet de recherches à la réponse HTTP initiale de votre page, ce qui permet à votre contenu et à vos mots-clés d&#39;améliorer l&#39;optimisation de votre moteur de recherche.

>[!NOTE]
>
>Cette API est disponible uniquement pour les types Commentaires et Collecte de blogs en direct.

## Intégration

L’API HTML Bootstrap de Livefyre renvoie un fragment HTML du contenu de l’utilisateur, qui peut être inclus dans la réponse HTTP de la page. Cette réponse sera lisible par les analyseurs de moteurs de recherche sans exécuter de code JavaScript. Une fois la page activée dans le navigateur d’un utilisateur, le fragment HTML est remplacé par le widget interactif complet et l’utilisateur peut publier du contenu.

Pour mettre en oeuvre l’API HTML du Bootstrap :

1. Faites une demande d’API serveur à serveur au point de terminaison HTML Bootstrap, comme indiqué ci-dessous.

   >[!NOTE]
   >
   >Si vous essayez d’attraper le code HTML Bootstrap pour une conversation qui n’existe pas encore (c’est-à-dire si vous n’avez pas encore incorporé l’application ou créé la collection), vous recevrez un 200, mais avec un contenu qui ressemble à quelque chose comme : `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Si votre déclaration ne contient pas de contenu comportant un &quot;404&quot;, enregistrez-le dans une chaîne. Vous pouvez mettre en cache cette réponse pour une utilisation ultérieure afin d’éviter de demander l’API HTML du Bootstrap à chaque chargement de page.
1. Insérez la chaîne HTML du Bootstrap dans votre page Web où vous souhaitez que le contenu s’affiche.
1. Servez votre page Web au navigateur (ou au moteur de recherche).

## Ressource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Paramètres

* **** networkNameVotre Livefyre a fourni le nom réseau. Par exemple : *labs* dans `labs.fyre.co`.
* **** siteIdIdentifiant du site de la collection.
* **b64** articleIdID d’article de la collection utilisant le codage base64url.

## Exemple

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Réponse

```
https://gist.github.com/ec5c2457322faf9cf515 
```
