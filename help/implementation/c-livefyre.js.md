---
description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Livefyre.js {#livefyre-js}

Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.

`Livefyre.js` est la bibliothèque principale que vous pouvez installer sur chaque page Web compatible Livefyre. Il définit l’objet global `window.Livefyre` et une méthode publique unique, `Livefyre.require`, qui peut être utilisée pour charger d’autres bibliothèques JavaScript Livefyre qui aident à [incorporer des applications Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [intégrer votre fournisseur d’authentification à Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) et plus encore.

## Ajouter à votre site {#section_cst_twg_xz}

Ajoutez la balise `<script>` suivante à votre page Web ou modèle de site Web. Si possible, ajoutez-le à la section `<head>` de votre document HTML afin qu’il se charge rapidement.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Ce script incorporera un très petit fichier (~1 Ko) appelé le scout Livefyre.js qui chargera ensuite la dernière version de Livefyre.js via le protocole avec lequel votre page Web a été consultée (HTTP ou HTTPS).

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` est un chargeur de module JavaScript personnalisé comme  [curl.](https://github.com/cujojs/curl) jsor  [RequireJS](https://requirejs.org/). Il peut être utilisé pour charger la plupart des paquets publiés par Livefyre et présente un chemin d&#39;intégration pratique et intuitif.

Les packages accessibles via `Livefyre.require` sont versionnés à l’aide de [Versioning sémantique](https://semver.org/). Les paquets peuvent être requis dans une version spécifique ou dans une gamme de versions afin que votre page Web puisse automatiquement bénéficier des nouvelles fonctionnalités de correctifs de bogues. Vous disposez ainsi d’une flexibilité lors de l’intégration de Livefyre sur votre site. Il existe trois niveaux d&#39;épinglage de version que vous pouvez utiliser avec `Livefyre.require`.

* **nom-package#1:** Epingler à la version majeure v1. Vous obtiendrez toutes les nouvelles mises à jour qui conservent une API rétrocompatible. Epinglez une version majeure pour recevoir des correctifs de bogues et des améliorations mineures de fonctionnalités pour cette version.
* **nom-package#1.1 :** Epinglage vers la version mineure v1.1. Vous obtiendrez tous les correctifs de bogues dans cette version mineure. Livefyre Engineering repousse toujours la version mineure d&#39;un paquet si son comportement par défaut ou son étendue fonctionnelle change d&#39;une manière qui peut provoquer un nouveau comportement inattendu sur votre page Web. Epinglez une version mineure si vous souhaitez recevoir des correctifs de bogues automatisés, mais aucune fonctionnalité supplémentaire ou modification du comportement par défaut.
* **nom-package#1.1.1 :** Epinglage de la version 1.1.1 du correctif. Le comportement de cette intégration ne changera jamais, même s’il y a des correctifs de bogues. Epinglez une version de correctif si vous avez d’importantes personnalisations CSS pour votre site qui dépendent de la structure d’annotation d’un pack qui peut changer ou si vous avez d’autres raisons de préférer que la version de Livefyre que vous exécutez ne change en rien.

Voici un exemple d’intégration utilisant `Livefyre.require` :

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## Packages disponibles {#section_ygd_dwg_xz}

Vous vous demandez quels paquets JavaScript Livefyre sont disponibles via `Livefyre.require` ? Vous trouverez toujours ici une liste à jour des packs pris en charge et de leurs dernières versions : [packages.html](https://cdn.livefyre.com/packages.html).

## Test des versions préliminaires des packages {#section_pgm_dpg_xz}

Il peut arriver que vous souhaitiez tester une prochaine version d’un pack Livefyre pour vous assurer qu’il fonctionnera sur votre site Web ou pour accepter de tester une fonction en cours de développement à votre demande. Outre l&#39;inclusion d&#39;une plage de versions sémantiques, l&#39;environnement UAT de pré-version peut être spécifié.

Par exemple, ce qui suit nécessite la version UAT des applications `fyre.conv`, Comments, Live Blog et Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
