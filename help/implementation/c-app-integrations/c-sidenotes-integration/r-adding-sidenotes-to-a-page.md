---
description: valeur nulle
seo-description: valeur nulle
seo-title: Ajout de signets à une page
solution: Experience Manager
title: Ajout de signets à une page
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Ajout de signets à une page {#adding-sidenotes-to-a-page}

Livefyre propose plusieurs options de configuration pour positionner les Sidenotes sur votre page :

* L’option Sélecteurs définit les éléments sur lesquels les Sidenotes doivent apparaître.
* Les ancres représentent des éléments qui peuvent être mis à l’écart.
* Le conteneur de threads personnalisé vous permet de définir l’emplacement du thread Sidenotes par rapport au contenu sidenoting.
* L’option Nombre de Sidenotes vous permet d’afficher le nombre de Sidenotes ajoutés à l’emplacement indiqué.
* Utilisez plusieurs `ConvConfig` objets pour ajouter des Sidenotes à plusieurs articles sur une même page.

## Sélecteurs {#section_wyj_4sv_sy}

L’option sélecteurs permet aux Sidenotes de rechercher du contenu sur la page. La valeur de cette option vous permet de déterminer de manière dynamique les éléments qui seront utilisés. Il peut s’agir d’une chaîne de sélecteur (telle que "#content p", #content img), d’un objet jQuery (tel `$(‘#content’)`), d’un tableau d’éléments DOM ou d’un objet doté de deux propriétés : incluez et excluez. L’application Sidenotes utilise alors les éléments spécifiés ou les éléments correspondants sur la page. Si des propriétés d’inclusion et d’exclusion sont utilisées, les Sidenotes analysent d’abord la page pour rechercher tous les éléments de la propriété include, puis suppriment tous les éléments trouvés dans la propriété exclude.

## Ancrages {#section_ehq_psv_sy}

Les ancres représentent un élément dont le contenu peut être mis à l’écart. Un élément d’ancrage peut contenir du texte ou une image. L’option de sélecteur transmise lors de la construction de l’application détermine les éléments d’ancrage.

## ID d’ancre {#section_rsb_rsv_sy}

Les ancres de la page sont identifiées à l’aide d’une `data-lf-anchor-id`.

Pour définir vous-même l’ID d’une ancre, ajoutez l’attribut `data-lf-custom-anchor-id` à l’élément que vous souhaitez mapper à une ancre. Cela s’avère utile lorsque la détection automatique des ancres échoue.

Par exemple, si vous prévoyez d’utiliser une URL différente pour les versions pour ordinateur de bureau et mobile d’une image, deux URL différentes peuvent être mappées à des ancres différentes. Si, au lieu de cela, votre code HTML fournit un `data-lf-custom-anchor-id` code qui est identique sur le mobile et le bureau, l’élément d’image sera traité comme une ancre unique.

Les ancres ont un type qui est déterminé dynamiquement, mais qui peut également être défini explicitement à l’aide de l’ `data-lf-custom-anchor-type` attribut.

>[!NOTE]
>
>La valeur du numéro d'énumération doit être utilisée.

Les types disponibles sont :

* **** Texte : 1
* **** Image : 2
* **** Média : 3
* **** Riche : 4

Voir la méthode [updateAnchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) pour en savoir plus sur l’utilisation de la `updateAnchors` méthode pour ajouter du contenu Sidenote à la page de manière dynamique.

## Conteneur de threads personnalisé {#section_jdh_btv_sy}

Utilisez l’ `threadContainerEl` option pour spécifier un emplacement pour un thread Sidenotes, autre que la position par défaut. Par défaut, lorsqu’une ancre est activée, les Sidenotes apparaissent en regard ou en dessous du contenu pertinent. Pour modifier cette valeur par défaut, utilisez `threadContainerEl` pour spécifier l’élément dans lequel le thread doit apparaître.

Cette valeur de cette option fonctionne de la même manière que l’option des sélecteurs, sauf que seul le premier élément valide sera utilisé.

## Nombre de Sidenotes {#section_pld_ntv_sy}

Utilisez l’ `numSidenotesEl` option pour incorporer un widget Sidenotes count facultatif sur votre page. Cette option accepte la même entrée que l’option des sélecteurs, mais n’utilise que le premier élément valide du tableau d’entrée.

Le widget décorera l’élément fourni ou l’élément mis en correspondance et inclura l’icône d’entrée Sidenotes, le nombre de signets saisis à cet emplacement et une icône d’aide.

Cliquez sur le widget pour afficher une fenêtre contextuelle avec une brève explication des Sidenotes et de leur utilisation.

L’explication et l’exemple de texte sont configurables à l’aide de chaînes personnalisées ( `questionExplanation` et `questionMockText`, respectivement). L’aspect du widget de comptage et de la fenêtre contextuelle peuvent également être configurés à l’aide de styles personnalisés ( `numSidenotes` et `numSidenotesPopover`, respectivement).

## Ajout de collections Sidenotes multiples à une seule page {#section_pjl_ptv_sy}

Livefyre vous permet d’ajouter plusieurs collections Sidenotes à une seule page. Par exemple, si la page comprend trois articles d’actualité, vous souhaiterez peut-être inclure trois itérations distinctes de l’application Sidenotes. Pour ce faire, vous devez définir un `ConvConfig` objet distinct pour chaque instance de Sidenotes que vous souhaitez créer. Par exemple :

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
