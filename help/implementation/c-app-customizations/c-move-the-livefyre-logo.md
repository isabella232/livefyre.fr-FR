---
description: Repositionnez le logo Livefyre sur votre page.
seo-description: Repositionnez le logo Livefyre sur votre page.
seo-title: Déplacer le logo Livefyre
solution: Experience Manager
title: Déplacer le logo Livefyre
uuid: 807304 ae -6070-4505-87 db -169 a 925 f 714 c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Déplacer le logo Livefyre{#move-the-livefyre-logo}

Repositionnez le logo Livefyre sur votre page.

Si votre accord avec Livefyre vous autorise, vous pouvez déplacer le logo Livefyre du haut du flux de contenu vers le bas.

Par exemple, ajoutez le code HTML suivant à votre page immédiatement après l&#39;élément qui contient l&#39;application Livefyre :

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Ajoutez ensuite la feuille de style suivante à la feuille de style :

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

