---
description: valeur nulle
seo-description: valeur nulle
seo-title: Ajout de lignes annexes à une page
solution: Experience Manager
title: Ajout de lignes annexes à une page
uuid: 6499 c 45 a -3773-4 adb-a 6 c 7-22 a 628309 afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Ajout de lignes annexes à une page {#adding-sidenotes-to-a-page}

Livefyre propose plusieurs options de configuration pour positionner les commentaires sur votre page :

* L'option Sélecteurs définit les éléments sur lesquels les commentaires doivent apparaître.
* Les ancres représentent les éléments qui peuvent être identifiés.
* Le conteneur de threads personnalisé vous permet de définir l'emplacement du thread de consignation par rapport au contenu sidenoté.
* L'option de comptabilisation des commentaires de sidenotes vous permet d'afficher le nombre de commentaires ajoutés à l'emplacement donné.
* Utilisez plusieurs `ConvConfig` objets pour ajouter des guillemets à plusieurs articles sur une seule page.

## Sélecteurs {#section_wyj_4sv_sy}

L'option Sélecteurs permet aux tableaux de données de rechercher du contenu sur la page. La valeur de cette option permet de déterminer dynamiquement les éléments qui seront utilisés. Il peut s'agir d'une chaîne de sélecteur (par exemple '# content p, # content img '), d'un objet jquery (tel `$(‘#content’)`que), d'un tableau d'éléments DOM ou d'un objet avec deux propriétés : inclure et exclure. L'application Sidenotes utilise alors les éléments spécifiés ou les éléments correspondants de la page. Si l'inclusion et l'exclusion de propriétés sont utilisées, les graphiques annexes analysent d'abord la page afin de rechercher tous les éléments de la propriété Inclure, puis suppriment les éléments trouvés sur la propriété Exclure.

## Ancrages {#section_ehq_psv_sy}

Les ancres représentent un élément dont le contenu peut être enregistré. Un élément d'ancrage peut contenir du texte ou une image. L'option de sélecteurs transmise lors de la construction de l'application détermine les éléments d'ancrage.

## Identifiants d'ancre {#section_rsb_rsv_sy}

Les ancrages sur la page sont identifiés à l'aide d'un `data-lf-anchor-id`.

Pour définir l'identifiant d'un ancrage vous-même, ajoutez l'attribut `data-lf-custom-anchor-id` à l'élément que vous souhaitez mapper à un ancrage. Cela s'avère utile lorsque la détection automatique des ancrages échoue.

Par exemple, si vous prévoyez d'utiliser une URL différente pour les versions de bureau et mobiles d'une image, deux URL différentes peuvent être mises en correspondance avec différents ancres. Si, au lieu de cela, HTML fournit une `data-lf-custom-anchor-id` valeur identique sur le bureau comme sur le bureau, l'élément image sera traité comme une ancre unique.

Les ancrages ont un type déterminé de manière dynamique, mais ils peuvent également être définis explicitement à l'aide de `data-lf-custom-anchor-type` l'attribut.

>[!NOTE]
>
>La valeur du numéro d'énumération doit être utilisée.

Les types disponibles sont les suivants :

* **Texte :** 1
* **Image :** 2
* **Media :** 3
* **Riche :** 4

Voir [la méthode updateanchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) pour plus d'informations sur l'utilisation de `updateAnchors` la méthode pour ajouter du contenu Sidenote à la page dynamiquement.

## Conteneur de thread personnalisé {#section_jdh_btv_sy}

Utilisez l' `threadContainerEl` option permettant de spécifier un emplacement pour un thread de consignation, autre que la position par défaut. Par défaut, lorsqu'une ancre est activée, les blocs annexes apparaissent en regard ou en dessous du contenu pertinent. Pour modifier cette valeur par défaut, utilisez l'élément `threadContainerEl` pour spécifier l'élément dans lequel le thread doit apparaître.

Cette valeur est identique à celle des sélecteurs, sauf que seul le premier élément valide est utilisé.

## Nombre de mentions de sidenotes {#section_pld_ntv_sy}

Utilisez `numSidenotesEl` l'option permettant d'incorporer un widget de nombre de mentions annexe facultatif sur votre page. Cette option accepte la même entrée que l'option selectors, mais utilise uniquement le premier élément valide dans le tableau d'entrée.

Le widget met en décoration l'élément fourni ou mis en correspondance et inclut l'icône d'entrée Indique le nombre de Sidenotes saisi à cette position et une icône d'aide.

Cliquez sur le widget pour afficher une fenêtre contextuelle contenant brièvement des commentaires sur les tableaux de sidenom et sur leur utilisation.

L'explication et l'exemple de texte sont configurables à l'aide de chaînes personnalisées ( `questionExplanation` et `questionMockText`, respectivement). L'aspect du widget de décompte et du sous-clic peut également être configuré à l'aide de styles personnalisés ( `numSidenotes` et `numSidenotesPopover`, respectivement).

## Ajout de plusieurs collections de colonnes à une seule page {#section_pjl_ptv_sy}

Livefyre vous permet d'ajouter plusieurs collections de titres à une page unique. Par exemple, si la page comprend trois actualités, vous pouvez inclure trois itérations distinctes de l'application Sidenotes. Pour ce faire, vous devez définir un objet distinct `ConvConfig` pour chaque instance des commentaires que vous souhaitez construire. Par exemple :

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
