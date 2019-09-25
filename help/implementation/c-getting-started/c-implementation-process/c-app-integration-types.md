---
description: Lorsque vous implémentez des applications Livefyre, le style de mise en oeuvre dépend du cas d’utilisation. Cette page explique les fonctionnalités des trois manières de créer une application.
seo-description: Lorsque vous implémentez des applications Livefyre, le style de mise en oeuvre dépend du cas d’utilisation. Cette page explique les fonctionnalités des trois manières de créer une application.
seo-title: Intégrations des applications CMS
solution: Experience Manager
title: Intégrations des applications CMS
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Intégrations des applications CMS{#cms-app-integrations}

Lorsque vous implémentez des applications Livefyre, le style de mise en oeuvre dépend du cas d’utilisation. Cette page explique les fonctionnalités des trois manières de créer une application.

L’intégration de Livefyre est indépendante de tout CMS et profil utilisateur et plateforme Auth. Mettez en oeuvre Livefyre d’une ou de plusieurs manières, selon votre cas d’utilisation et vos besoins.

Vous pouvez utiliser l’intégration traditionnelle pour créer des composants AEM personnalisés.

## Présentation du type d’intégration d’application CMS

| Type | Besoin de développement | Fonctionnalités | Avantages | Limites |
|--- |--- |--- |--- |--- |
| Concepteur d’applications | Très faible | Créez des incorporations JS dans Studio pour les ajouter aux pages sans avoir recours à un développeur <br>Limited Styling and Configurations (Style et configurations </br>limités disponibles) Cas d’utilisation : Pages à usage unique (couverture d’événements, campagnes, centres) | Possibilité d’exécuter une application rapidement. <br>Les configurations peuvent être effectuées par un membre non technique. <br>Changements faciles à la volée des configurations | Création d’une application à l’aide de Livefyre Studio <br>non automatisée |
| Livefyre.js | Méthode | Intégrer les applications dans le code JavaScript de vos pages Cas d’ <br>utilisation : Modèles réutilisables (contenu éditorial, révisions de produits) | Utiliser la suite complète de personnalisations et de configurations d’application <br>Automatise le processus pour instancier dynamiquement les applications depuis votre CMS sur vos pages | Il faut un développeur dès le départ. |
| API SDK | Advanced | Récupérez votre contenu de Livefyre afin de l’utiliser pour des applications personnalisées <br>Personnalisez le frontal au-delà de l’offre prise en charge Cas d’ <br>utilisation : Intégrations des données/analyses et applications frontales personnalisées | Pleine puissance sur l'apparence de l'application | Nécessite un développement initial. <br>Un niveau plus élevé d'effort de développement pour implémenter. |
