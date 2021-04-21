---
description: Intégrez une application Sidenotes en suivant un processus similaire à celui des applications de base.
title: Intégration de Sidenotes
exl-id: 368951b1-fef2-46d8-b89c-68c46962e937
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Intégration de Sidenotes{#sidenotes-integration}

Intégrez une application Sidenotes en suivant un processus similaire à celui des applications de base.

En règle générale, si l’intégration de l’application principale est terminée, le code écrit pour générer l’objet `collectionMeta` peut être réutilisé pour les Sidenotes.

Vous pouvez également réutiliser vos délégués `auth` existants en fournissant un délégué `auth` créé avec `fyre.conv` aux Sidenotes dans le champ (facultatif) `authDelegate`.

>[!NOTE]
>
>Sidenotes vous permet d&#39;inclure `network`, `siteId` et `articleId` dans un seul objet, plutôt que de les transmettre séparément dans d&#39;autres parties du constructeur.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Comme indiqué dans la section Création `collectionMeta`, `collectionMeta` est un objet JSON codé. Dans l’exemple ci-dessus, l’objet JSON utilise le format suivant avant d’être codé JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Pour plus d&#39;informations, consultez le jeton `collectionMeta`.

## Configuration mobile

Sidenotes a été optimisé pour être utilisé sur les périphériques mobiles. Pour obtenir de meilleurs résultats avec les versions mobiles de votre application Livefyre, définissez l’option évolutive de l’utilisateur sur Non. Par exemple :

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
