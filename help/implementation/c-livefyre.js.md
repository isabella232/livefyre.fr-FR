---
description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre.js {#livefyre-js}

Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.

`Livefyre.js` est la bibliothèque principale que vous pouvez installer sur chaque page Web Livefyre. Il définit l’ `window.Livefyre` objet global et une méthode publique unique, `Livefyre.require`, qui peut être utilisée pour charger d’autres bibliothèques JavaScript Livefyre qui aident à [incorporer des applications Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), à [intégrer votre fournisseur d’authentification à Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) et bien plus encore.

## Ajouter à votre site {#section_cst_twg_xz}

Ajoutez la `<script>` balise suivante à votre page Web ou modèle de site Web. Si possible, ajoutez-le à la `<head>` section de votre document HTML afin qu’il se charge rapidement.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Ce script incorporera un très petit fichier (~1 Ko) appelé scout Livefyre.js qui chargera ensuite la dernière version de Livefyre.js via le protocole avec lequel votre page Web a été consultée (HTTP ou HTTPS).

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` est un chargeur de module JavaScript personnalisé comme [curl.js](https://github.com/cujojs/curl) ou [RequireJS](https://requirejs.org/). Il peut être utilisé pour charger la plupart des paquets publiés par Livefyre et présente un chemin d'intégration pratique et intuitif.

Les packages accessibles via `Livefyre.require` sont versionnés à l’aide de la version [sémantique](https://semver.org/). Les packs peuvent être requis dans une version spécifique ou dans une plage de versions afin que votre page Web puisse bénéficier automatiquement des nouvelles fonctionnalités de correctifs de bogues. Vous bénéficiez ainsi d’une flexibilité lors de l’intégration de Livefyre sur votre site. Vous pouvez utiliser trois niveaux d’épinglage de version avec `Livefyre.require`.

* **** package-name#1 : Epingler à la version majeure v1. Vous obtiendrez toutes les nouvelles mises à jour qui conservent une API rétrocompatible. Epinglez une version majeure pour recevoir des correctifs et des améliorations mineures de fonctionnalités pour cette version.
* **** package-name#1.1 : Epingler à la version mineure v1.1. Vous obtiendrez tous les correctifs de cette version mineure. Livefyre Engineering repoussera toujours la version mineure d'un paquet si son comportement par défaut ou son étendue fonctionnelle change d'une manière susceptible de provoquer un nouveau comportement inattendu sur votre page Web. Epinglez une version mineure si vous souhaitez recevoir des correctifs automatisés, mais pas de fonctionnalités supplémentaires ni de modifications du comportement par défaut.
* **** package-name#1.1.1 : Epinglez le correctif version 1.1.1. Le comportement de cette intégration ne changera jamais, même en cas de correctifs. Epinglez une version de correctif si vous avez des personnalisations CSS étendues pour votre site qui dépendent de la structure d’annotation d’un pack susceptible de changer, ou si vous avez d’autres raisons de préférer que la version de Livefyre que vous exécutez ne change en rien.

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

Vous vous demandez quels paquets JavaScript Livefyre sont disponibles via `Livefyre.require`? Vous trouverez toujours une liste à jour des packages pris en charge et de leurs dernières versions à l’adresse suivante : [packages.html](https://cdn.livefyre.com/packages.html).

## Test des versions préliminaires des packages {#section_pgm_dpg_xz}

Il peut arriver que vous souhaitiez tester une prochaine version d’un pack Livefyre pour vous assurer qu’il fonctionnera sur votre site Web ou pour accepter de tester une fonctionnalité en cours de développement à votre demande. Outre l’inclusion d’une plage de versions sémantiques, l’environnement UAT de pré-version peut être spécifié.

Par exemple, les applications suivantes nécessitent la version UAT des applications `fyre.conv`, Comments, Live Blog et Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
