---
description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur
  votre site.
seo-description: Bibliothèque Livefyre principale utilisée pour alimenter Livefyre
  sur votre site.
seo-title: Livefyre. js
solution: Experience Manager
title: Livefyre. js
uuid: 7 b 3 eca 57-d 5 e 8-416 d-badf-a 9 c 51 d 10 dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre. js {#livefyre-js}

Bibliothèque Livefyre principale utilisée pour alimenter Livefyre sur votre site.

`Livefyre.js` est la bibliothèque principale que vous pouvez installer sur chaque webpage Web Livefyre activée. Il définit l'objet global `window.Livefyre` et une méthode publique unique, `Livefyre.require`qui peuvent être utilisées pour charger d'autres bibliothèques JavaScript Livefyre qui facilitent [l'intégration des applications Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [l'intégration de votre fournisseur d'authentification avec Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) et plus encore.

## Ajouter à votre site {#section_cst_twg_xz}

Ajoutez la balise suivante `<script>` à votre page Web ou modèle de site Web. Si possible, ajoutez-la à la `<head>` section du document HTML pour qu'elle se charge rapidement.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Ce script incorpore un très petit fichier (~ 1 Ko) appelé le scout Livefyre. js qui chargera ensuite la dernière version de Livefyre. js sur le protocole avec lequel votre webpage Web a été consultée (HTTP ou HTTPS).

## Livefyre. require {#section_ipq_hwg_xz}

`Livefyre.require` est un chargeur de module JavaScript personnalisé comme [curl. js](https://github.com/cujojs/curl) ou [requirejs](https://requirejs.org/). Il permet de charger la plupart des packs publiés par Livefyre et présente un chemin d'intégration pratique et intuitif.

Les packs accessibles par le biais `Livefyre.require` du contrôle de version sémantique utilisent [le contrôle sémantique](https://semver.org/). Des packs peuvent être nécessaires à une version spécifique ou à une plage de versions afin que votre page Web puisse bénéficier automatiquement des nouvelles fonctionnalités de correctifs. Vous bénéficiez ainsi de toute latitude lors de l'intégration de Livefyre sur votre site. Vous pouvez utiliser trois niveaux de pinglage de version avec `Livefyre.require`.

* **package-name # 1 :** Epingler à la version majeure v 1. Vous obtiendrez toutes les nouvelles mises à jour qui conservent une API compatible ascendante. Épingler à une version majeure pour recevoir des correctifs et des améliorations mineures des fonctionnalités pour cette version.
* **package-name # 1.1 :** Epingler à la version mineure v 1.1. Vous obtiendrez tous les correctifs à cette version mineure. Livefyre Engineering empile toujours la version mineure d'un pack si son comportement par défaut ou la plage fonctionnelle change de manière à donner un nouveau comportement inattendu à votre webpage Web. Epinglez à une version mineure si vous souhaitez recevoir des correctifs automatisés, mais pas de fonctionnalité supplémentaire ni de modification du comportement par défaut.
* **package-name # 1.1.1 :** Epingler au correctif version 1.1.1. Le comportement de cette intégration ne change jamais, même s'il existe des correctifs. Épinglez à une version de correctif si vous disposez de personnalisations CSS étendues pour votre site qui dépendent de la structure d'annotation d'un package qui peut changer ou si vous avez d'autres raisons de préférer que la version Livefyre que vous exécutez ne change d'aucune manière.

Voici un exemple d'intégration à l'aide `Livefyre.require` de :

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

Vous vous demandez quels `Livefyre.require`paquets JavaScript Livefyre sont disponibles ? Vous pouvez toujours trouver une liste à jour des packages pris en charge et leurs dernières versions ici : [packages.html](https://cdn.livefyre.com/packages.html).

## Test des versions préliminaires des packages {#section_pgm_dpg_xz}

Il arrive que vous souhaitiez tester une version à venir d'un pack Livefyre pour vérifier qu'elle fonctionnera sur votre site Web ou que l'acceptation d'une fonctionnalité est en cours de développement à votre demande. Outre l'inclusion d'une plage de version sémantique, l'environnement UAT de pré-version peut être spécifié.

Par exemple, les éléments suivants nécessiteront la version UAT de `fyre.conv`, les commentaires, le blog en direct et les applications de Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
