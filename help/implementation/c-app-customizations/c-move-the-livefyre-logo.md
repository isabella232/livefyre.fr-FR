---
description: Repositionnez le logo Livefyre sur votre page.
title: Déplacer le logo Livefyre
exl-id: dc6c26cf-e0b9-4af3-8a3c-e58ea4ecbc44
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Déplacer le logo Livefyre{#move-the-livefyre-logo}

Repositionnez le logo Livefyre sur votre page.

Si votre accord avec Livefyre le permet, vous pouvez déplacer le logo de Livefyre du haut du flux de contenu vers le bas.

Par exemple, ajoutez le code HTML suivant à votre page immédiatement après l’élément qui contient l’application Livefyre :

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Ajoutez ensuite les éléments suivants à la feuille de style de votre page :

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```
