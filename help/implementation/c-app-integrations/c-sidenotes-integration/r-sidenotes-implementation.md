---
description: Implémenter Sidenotes à l’aide de l’implémentation .js.
seo-description: Implémenter Sidenotes à l’aide de l’implémentation .js.
seo-title: Implémentation de Sidenotes
solution: Experience Manager
title: Implémentation de Sidenotes
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 28%

---


# Implémentation de Sidenotes{#sidenotes-implementation}

## Implémenter Sidenotes à l’aide de l’implémentation .js

Pour mettre en oeuvre cette fonctionnalité, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration JavaScript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

### Exemple

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
