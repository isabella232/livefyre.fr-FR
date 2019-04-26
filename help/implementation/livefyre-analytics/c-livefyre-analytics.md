---
description: valeur nulle
seo-description: valeur nulle
seo-title: Utiliser Livefyre avec d'autres outils Analytics
solution: Experience Manager
title: Utiliser Livefyre avec d'autres outils Analytics
uuid: 26 c 835 f 6-aced -41 f 7-aabe -418 afce 8 a 829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utiliser Livefyre avec d'autres outils Analytics{#use-livefyre-with-other-analytics-tool}

Vous pouvez utiliser des outils d'analyse pour collecter des données sur les interactions de l'utilisateur avec les applications Livefyre. Vous pouvez utiliser Adobe Analytics ou un outil de votre choix.

Pour utiliser Livefyre avec un outil de votre choix (et non Adobe Analytics), suivez la procédure décrite dans cette page.

## Étape 1 : Gestionnaire d'événements de configuration {#section_ngm_gzl_pdb}

Configurez un gestionnaire d'événements sur les pages où vous utilisez les applications Livefyre. Cela vous permet de collecter des données à partir des applications sur cette page que vous pouvez utiliser pour les analyses.

Ajoutez Livefyre. js à une page pour configurer le gestionnaire d'événements. Livefyre. js se charge de manière asynchrone. Les analyses ne sont pas immédiatement disponibles pour réduire la taille du fichier et améliorer les performances de chargement. Vous devez interroger l'objet Analytics jusqu'à ce que les données soient disponibles. Placez ce script n'importe où sur la page ou regroupez-le dans vos propres scripts compilés.

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## Étape 2 : Mise en œuvre de la fonction handler

Une fois la fonctionnalité Livefyre. analytics disponible sur la page, mettez en œuvre la fonction analyticshandler pour envoyer les événements reçus au fournisseur d'analyses de votre choix.

1. Le gestionnaire d'analyses reçoit un tableau d'événements qui doivent être itérés et envoyés individuellement ou par lot, si votre fournisseur le prend en charge.
1. Faites correspondre les données d'événement reçues par le gestionnaire à un format requis par votre fournisseur d'analyses.
1. Envoyez les données à votre fournisseur d'analyses.

