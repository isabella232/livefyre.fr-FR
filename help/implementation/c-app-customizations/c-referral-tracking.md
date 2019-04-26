---
description: Effectuez un suivi sur les clics vers votre page à partir du trafic de
  référence.
seo-description: Effectuez un suivi sur les clics vers votre page à partir du trafic
  de référence.
seo-title: Suivi des références
solution: Experience Manager
title: Suivi des références
uuid: 5206 cc 16-9671-4 b 3 d-a 013-be 1 a 3 e 8 c 029 d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Suivi des références{#referral-tracking}

Effectuez un suivi sur les clics vers votre page à partir du trafic de référence.

Livefyre ajoute une variable de référence à l'URL lorsqu'un commentaire est publié ou partagé sur un réseau social, ainsi que pour les permalinks inclus dans les courriers électroniques Livefyre. Utilisez cette variable pour effectuer le suivi du trafic de renvoi des applications Livefyre vers vos propriétés sociales ou détenues.

Les applications Livefyre vous permettent de suivre les flux de données résultant du trafic de référencement, ce qui vous permet d'analyser le trafic de votre site.

## Suivi du trafic de renvoi Livefyre {#section_nsy_qp4_xz}

Le trafic de référent Livefyre à partir des réseaux sociaux et des courriels peut être suivi en examinant les paramètres de chaîne de requête dans les URL de vos pages et en implémentant le code sur votre page pour le suivre via votre fournisseur d'analyses. Livefyre ajoute un lien de référence à l'URL lorsqu'un commentaire est publié ou partagé sur un réseau social, ainsi que pour les permalinks inclus dans les courriers électroniques Livefyre.

## Exemple de mise en œuvre {#section_xvs_x44_xz}

Si le trafic provient d'une notification Push streamhub, un paramètre de chaîne de requête hubrefsrc s'affiche avec la valeur e-mail, facebook, twitter, linkedin ou permalink. Le nom du paramètre hubrefsrc peut être configuré au niveau réseau par votre équipe Livefyre.

Pour intégrer une plateforme d'analyse, votre page doit rechercher la variable hubrefsrc au chargement et enregistrer le trafic s'il est présent.

Par exemple :

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

Applications utilisant cette fonctionnalité :

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Révisions](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Commentaires de sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)