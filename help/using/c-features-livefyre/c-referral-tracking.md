---
description: Effectuez un suivi sur les clics vers votre page à partir du trafic de référence.
seo-description: Effectuez un suivi sur les clics vers votre page à partir du trafic de référence.
seo-title: Suivi des références
solution: Experience Manager
title: Suivi des références
uuid: 7 daf 615 d -0 c 07-49 d 1-adb 2-1 ac 67 ea 563 e 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Suivi des références{#referral-tracking}

Effectuez un suivi sur les clics vers votre page à partir du trafic de référence.

Livefyre ajoute une variable de référence à l&#39;URL lorsqu&#39;un commentaire est publié ou partagé sur un réseau social, ainsi que pour les permalinks inclus dans les courriers électroniques Livefyre. Utilisez cette variable pour effectuer le suivi du trafic de renvoi des applications Livefyre vers vos propriétés sociales ou détenues.

Les applications Livefyre vous permettent de suivre les flux de données résultant du trafic de référencement, ce qui vous permet d&#39;analyser le trafic de votre site.

## Suivi du trafic de renvoi Livefyre {#section_nsy_qp4_xz}

Le trafic de référent Livefyre à partir des réseaux sociaux et des courriels peut être suivi en examinant les paramètres de chaîne de requête dans les URL de vos pages et en implémentant le code sur votre page pour le suivre via votre fournisseur d&#39;analyses. Livefyre ajoute un lien de référence à l&#39;URL lorsqu&#39;un commentaire est publié ou partagé sur un réseau social, ainsi que pour les permalinks inclus dans les courriers électroniques Livefyre.

## Exemple de mise en œuvre {#section_xvs_x44_xz}

Si le trafic provient d&#39;une notification Push streamhub, un paramètre de chaîne de requête hubrefsrc s&#39;affiche avec la valeur e-mail, facebook, twitter, linkedin ou permalink. Le nom du paramètre hubrefsrc peut être configuré au niveau réseau par votre équipe Livefyre.

Pour intégrer une plateforme d&#39;analyse, votre page doit rechercher la variable hubrefsrc au chargement et enregistrer le trafic s&#39;il est présent.

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

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Révisions](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Commentaires de sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

