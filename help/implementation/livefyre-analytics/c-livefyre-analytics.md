---
description: valeur nulle
seo-description: valeur nulle
seo-title: Utilisation de Livefyre avec un autre outil Analytics
solution: Experience Manager
title: Utilisation de Livefyre avec un autre outil Analytics
uuid: 26c835f6-aced-41f7-aabe-418afce8a829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilisation de Livefyre avec un autre outil Analytics{#use-livefyre-with-other-analytics-tool}

Vous pouvez utiliser les outils d’analyse pour collecter des données sur les interactions des utilisateurs avec les applications Livefyre. Vous pouvez utiliser Adobe Analytics ou un outil de votre choix.

Pour utiliser Livefyre avec un outil de votre choix (et non Adobe Analytics), suivez la procédure décrite sur cette page.

## Étape 1 : Configuration du gestionnaire d’événements {#section_ngm_gzl_pdb}

Configurez un gestionnaire d’événements sur les pages où vous utilisez les applications Livefyre. Cela vous permet de collecter des données des applications sur cette page que vous pouvez utiliser pour les analyses.

Ajoutez Livefyre.js à une page pour configurer le gestionnaire d’événements. Livefyre.js se charge de manière asynchrone. Pour réduire la taille du fichier et améliorer les performances de charge, les analyses ne sont pas disponibles immédiatement. Vous devez interroger l’objet analytics jusqu’à ce que les données soient disponibles. Placez ce script n’importe où sur la page ou incluez-le dans vos propres scripts compilés.

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

## Étape 2 : Fonction du gestionnaire de mise en oeuvre

Une fois la fonctionnalité Livefyre.analytics disponible sur la page, implémentez la fonction analyticsHandler pour envoyer les événements reçus au fournisseur d’analyses de votre choix.

1. Le gestionnaire d’analyses reçoit un tableau d’événements qui doivent être itérés et envoyés individuellement ou sous forme de lot, si votre fournisseur le prend en charge.
1. Faites correspondre les données d’événement reçues par le gestionnaire à un format requis par votre fournisseur d’analyses.
1. Envoyez les données à votre fournisseur d’analyses.

