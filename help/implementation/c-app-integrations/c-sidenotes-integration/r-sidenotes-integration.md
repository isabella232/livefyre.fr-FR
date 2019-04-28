---
description: Intégration d'une application Sidenotes en suivant un processus semblable aux applications principales.
seo-description: Intégration d'une application Sidenotes en suivant un processus semblable aux applications principales.
seo-title: Intégration des balises
solution: Experience Manager
title: Intégration des balises
uuid: 4 aa 14 ada -402 a -482 d-b 43 e -96 f 37 afa 6 c 53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Intégration des balises{#sidenotes-integration}

Intégration d&#39;une application Sidenotes en suivant un processus semblable aux applications principales.

En règle générale, si l&#39;intégration de l&#39;application principale est terminée, le code écrit pour générer l `collectionMeta` &#39;objet peut être réutilisé pour les caractères annexes.

Vous pouvez également réutiliser vos `auth` délégués existants en fournissant `auth` un délégué créé `fyre.conv` avec les caractères annexes dans `authDelegate` le champ (facultatif).

>[!NOTE]
>
>Les balises sidenotes vous permettent d&#39;inclure `network`, `siteId`et `articleId` dans un seul objet, plutôt que de les transmettre séparément dans d&#39;autres parties du constructeur.

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

Comme indiqué dans `collectionMeta` la section Building, `collectionMeta` est un objet JSON codé. Dans l&#39;exemple ci-dessus, l&#39;objet JSON adopte le format suivant avant son codage JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Pour plus d&#39;informations, consultez le `collectionMeta` jeton.

## Configuration mobile

Les commentaires de sidenotes ont été optimisés pour les périphériques mobiles. Pour obtenir de meilleurs résultats avec les versions mobiles de votre application Livefyre, définissez l&#39;option évolutive sur non. Par exemple :

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
