---
description: Implémenter Sidenotes à l’aide de l’implémentation .js.
title: Implémentation de Sidenotes
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 22%

---

# Implémentation de Sidenotes{#sidenotes-implementation}

## Implémenter Sidenotes à l’aide de l’implémentation .js

Pour mettre en oeuvre cette fonctionnalité, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration JavaScript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

### Exemple

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
