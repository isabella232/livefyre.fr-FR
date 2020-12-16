---
description: Effectuez le suivi des clics vers votre page à partir du trafic de référence.
seo-description: Effectuez le suivi des clics vers votre page à partir du trafic de référence.
seo-title: Suivi des renvois
solution: Experience Manager
title: Suivi des renvois
uuid: 5206cc16-9671-4b3d-a013-be1a3e8c029d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# Suivi des renvois{#referral-tracking}

Effectuez le suivi des clics vers votre page à partir du trafic de référence.

Livefyre ajoute une variable de référence à l’URL lorsqu’un commentaire est publié ou partagé sur un réseau social, ainsi que pour les liens permalins inclus dans les courriels Livefyre. Utilisez cette variable pour effectuer le suivi du trafic de référence depuis les applications Livefyre vers vos propriétés sociales ou détenues.

Les applications Livefyre vous permettent de suivre les flux de données résultant du trafic de référence, ce qui vous permet d’analyser le trafic de votre site.

## Suivi du trafic de référence Livefyre {#section_nsy_qp4_xz}

Le trafic de référence Livefyre provenant des réseaux sociaux et des courriers électroniques peut être suivi en examinant les paramètres de chaîne de requête dans les URL de vos pages et en implémentant du code sur votre page pour effectuer le suivi par l’intermédiaire de votre fournisseur d’analyses. Livefyre ajoute un lien de référence à l’URL lorsqu’un commentaire est publié ou partagé sur un réseau social, ainsi que pour les liens permalins inclus dans les courriels Livefyre.

## Exemple d’implémentation {#section_xvs_x44_xz}

Si le trafic provient d’une notification StreamHub, il y aura un paramètre de chaîne de requête hubRefSrc avec la valeur email, facebook, twitter, linkedin ou permalink. Le nom du paramètre hubRefSrc peut être configuré au niveau du réseau par votre équipe de diffusion Livefyre.

Pour l’intégrer à une plateforme d’analyse, votre page doit rechercher le hubRefSrc au chargement et enregistrer le trafic s’il est présent.

Par exemple :

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```

Applications qui utilisent cette fonctionnalité :

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Critiques](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)