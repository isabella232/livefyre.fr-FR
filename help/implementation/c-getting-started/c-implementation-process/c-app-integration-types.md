---
description: Lorsque vous implémentez des applications Livefyre, le style de mise en oeuvre dépend de votre cas d’utilisation. Cette page explique les fonctionnalités des trois manières de créer une application.
seo-description: Lorsque vous implémentez des applications Livefyre, le style de mise en oeuvre dépend de votre cas d’utilisation. Cette page explique les fonctionnalités des trois manières de créer une application.
seo-title: Intégrations d’applications CMS
solution: Experience Manager
title: Intégrations d’applications CMS
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# Intégrations des applications CMS{#cms-app-integrations}

Lorsque vous implémentez des applications Livefyre, le style de mise en oeuvre dépend de votre cas d’utilisation. Cette page explique les fonctionnalités des trois manières de créer une application.

L’intégration de Livefyre est indépendante de tout CMS, Profil utilisateur et plate-forme Auth. Mettez en oeuvre Livefyre d’une ou de plusieurs manières, selon votre cas d’utilisation et vos exigences.

Vous pouvez utiliser l’intégration traditionnelle pour créer des composants AEM personnalisés.

## Présentation du type d’intégration d’application CMS

| Type | Besoins en matière de développement | Fonctionnalités | Avantages | Limites |
|--- |--- |--- |--- |--- |
| Concepteur d’applications | Très faible | Créez des incorporations JS dans Studio pour ajouter des pages sans développeur <br>Style et configurations limités disponibles </br>Cas d’utilisation : Pages à usage unique (couverture de événement, campagnes, concentrateurs) | Possibilité de mettre en service une application en cours d’exécution en peu de temps. <br>Les configurations peuvent être effectuées par un membre non technique. <br>Changements faciles à la volée des configurations | Vous devez d’abord créer une application à l’aide de Livefyre Studio <br>Non automatisé |
| Livefyre.js | Méthode | Intégrer les applications dans le code JavaScript de vos pages <br>Cas d’utilisation : Modèles réutilisables (contenu éditorial, révisions de produits) | Utiliser la suite complète de personnalisations et de configurations d&#39;application <br>Automatise le processus pour instancier dynamiquement les applications à partir de votre CMS sur vos pages | Il faut un développeur dès le départ. |
| API SDK | Advanced | Récupérez votre contenu de Livefyre pour l&#39;utiliser dans des applications personnalisées <br>Personnalisez le front-end au-delà de l&#39;offre prise en charge <br>Cas d&#39;utilisation : Intégrations des données/analyses et applications frontales personnalisées | Puissance totale sur l&#39;aspect et l&#39;aspect de l&#39;application | Nécessite le développement dès le départ. <br>Un niveau plus élevé d&#39;effort de développement à mettre en oeuvre. |
