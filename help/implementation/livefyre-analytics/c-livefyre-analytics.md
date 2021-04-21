---
title: Utilisation de Livefyre avec d’autres outils Analytics
description: Utilisation de Livefyre avec d’autres outils Analytics
exl-id: da29e281-5095-4e99-a248-19390f2059a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Utilisation de Livefyre avec d’autres outils Analytics{#use-livefyre-with-other-analytics-tool}

Vous pouvez utiliser les outils d’analyse pour collecter des données sur les interactions des utilisateurs avec les applications Livefyre. Vous pouvez utiliser Adobe Analytics ou un outil de votre choix.

Pour utiliser Livefyre avec un outil de votre choix (pas l&#39;Adobe Analytics), suivez la procédure décrite sur cette page.

## Étape 1 : Configurer le gestionnaire de événements {#section_ngm_gzl_pdb}

Configurez un gestionnaire de événements sur les pages où vous utilisez les applications Livefyre. Cela vous permet de collecter des données des applications sur cette page que vous pouvez utiliser pour les analyses.

Ajoutez Livefyre.js sur une page pour configurer le gestionnaire de événements. Livefyre.js se charge de manière asynchrone. Pour réduire la taille du fichier et améliorer les performances de charge, les analyses ne sont pas disponibles immédiatement. Vous devez interroger l’objet analytics jusqu’à ce que les données soient disponibles. Placez ce script n’importe où sur la page ou assemblez-le dans vos propres scripts compilés.

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

## Étape 2 : Mise en oeuvre de la fonction de gestionnaire

Une fois la fonctionnalité Livefyre.analytics disponible sur la page, implémentez la fonction analyticsHandler pour envoyer les événements reçus au fournisseur d’analyses de votre choix.

1. Le gestionnaire d’analyses reçoit un tableau de événements qui doivent être itérés et envoyés individuellement ou en lot, si votre fournisseur le prend en charge.
1. Faites correspondre les données de événement reçues par le gestionnaire à un format requis par votre fournisseur d’analyses.
1. Envoyez les données à votre fournisseur d’analyses.
