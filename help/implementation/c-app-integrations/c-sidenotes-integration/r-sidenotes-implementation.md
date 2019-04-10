---
description: Mise en œuvre de Sidenotes à l’aide de la mise en œuvre du fichier .js.
seo-description: Mise en œuvre de Sidenotes à l’aide de la mise en œuvre du fichier .js.
seo-title: Mise en œuvre des tableaux de sidenom
solution: Experience Manager
title: Mise en œuvre des tableaux de sidenom
uuid: aa 13852 e-e 2 b 0-4 a 86-97 cd-d 08 ab 5 e 2 cfab
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Mise en œuvre des tableaux de sidenom{#sidenotes-implementation}

## Mise en œuvre de Sidenotes à l’aide de la mise en œuvre du fichier .js

Pour mettre en œuvre cette fonction, transmettez un mappage d'objet 1-1 des chaînes que vous souhaitez remplacer par l'objet de configuration Javascript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

### Exemple

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
