---
description: valeur nulle
seo-description: valeur nulle
seo-title: Ajouter des identifiants à une page
solution: Experience Manager
title: Ajouter des identifiants à une page
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# Ajouter des identifiants à une page {#adding-sidenotes-to-a-page}

Livefyre propose plusieurs options de configuration pour positionner les Sidenotes sur votre page :

* L&#39;option Sélecteurs définit les éléments sur lesquels les Sidenotes doivent apparaître.
* Les ancres représentent des éléments qui peuvent être mis à l’écart.
* Le conteneur de thread personnalisé vous permet de définir l&#39;emplacement du thread Sidenotes par rapport au contenu mis en place.
* L&#39;option Nombre de Sidenotes vous permet d&#39;afficher le nombre de Sidenotes ajoutés à l&#39;emplacement indiqué.
* Utilisez plusieurs objets `ConvConfig` pour ajouter des identifiants à plusieurs articles sur une même page.

## Sélecteurs {#section_wyj_4sv_sy}

L’option sélecteurs permet aux Sidenotes de rechercher du contenu sur la page. La valeur de cette option vous permet de déterminer de manière dynamique les éléments qui seront utilisés. Il peut s’agir d’une chaîne de sélecteur (telle que &quot;#content p, #content img&quot;), d’un objet jQuery (tel que `$(‘#content’)`), d’un tableau d’éléments DOM ou d’un objet doté de deux propriétés : inclure et exclure. L’application Sidenotes utilise alors les éléments spécifiés ou les éléments correspondants sur la page. Si des propriétés d’inclusion et d’exclusion sont utilisées, les Sidenotes analysent d’abord la page pour rechercher tous les éléments de la propriété include, puis suppriment tous les éléments trouvés sur la propriété exclude.

## Ancrages {#section_ehq_psv_sy}

Les ancres représentent un élément dont le contenu peut être mis de côté. Un élément d’ancrage peut contenir du texte ou une image. L’option de sélecteurs transmise lors de la construction de l’application détermine les éléments d’ancrage.

## Identifiants d’ancrage {#section_rsb_rsv_sy}

Les ancres de la page sont identifiées à l’aide d’un `data-lf-anchor-id`.

Pour définir vous-même l’identifiant d’une ancre, ajoutez l’attribut `data-lf-custom-anchor-id` à l’élément que vous souhaitez mapper à une ancre. Cela s’avère utile dans les cas où la détection automatique des ancres échouerait.

Par exemple, si vous prévoyez d’utiliser une URL différente pour les versions pour ordinateur de bureau et mobile d’une image, deux URL différentes peuvent être mappées à des ancres différentes. Si, à la place, votre code HTML fournit un `data-lf-custom-anchor-id` identique sur les périphériques mobiles et les ordinateurs de bureau, l’élément d’image est traité comme une ancre unique.

Les ancres ont un type qui est déterminé dynamiquement, mais qui peut également être défini explicitement à l&#39;aide de l&#39;attribut `data-lf-custom-anchor-type`.

>[!NOTE]
>
>La valeur du numéro de énumération doit être utilisée.

Les types disponibles sont :

* **Texte:** 1
* **Image:** 2
* **Média:** 3
* **Rich:** 4

Voir [méthode updateAnchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) pour en savoir plus sur l&#39;utilisation de la méthode `updateAnchors` pour ajouter dynamiquement du contenu Sidenote à la page.

## Conteneur de thread personnalisé {#section_jdh_btv_sy}

Utilisez l&#39;option `threadContainerEl` pour spécifier un emplacement pour un thread Sidenotes, autre que la position par défaut. Par défaut, lorsqu’une ancre est activée, les Sidenotes apparaissent en regard ou en dessous du contenu pertinent. Pour modifier cette valeur par défaut, utilisez `threadContainerEl` pour spécifier l&#39;élément où le thread doit apparaître.

Cette valeur pour cette option fonctionne de la même manière que l’option de sélecteurs, sauf que seul le premier élément valide sera utilisé.

## Nombre de sidents {#section_pld_ntv_sy}

Utilisez l&#39;option `numSidenotesEl` pour incorporer un widget Sidenotes count facultatif sur votre page. Cette option accepte la même entrée que l&#39;option de sélecteurs mais n&#39;utilise que le premier élément valide du tableau d&#39;entrée.

Le widget décorera l’élément fourni ou correspondant et inclura l’icône d’entrée Sidenotes, le nombre de Sidenotes entrés à cet emplacement et une icône d’aide.

Un clic sur le widget affiche une fenêtre contextuelle contenant une brève explication des Sidenotes et de leur utilisation.

L&#39;explication et l&#39;exemple de texte sont configurables à l&#39;aide de chaînes personnalisées ( `questionExplanation` et `questionMockText`, respectivement). L’aspect du widget de comptage et de la fenêtre contextuelle peut également être configuré à l’aide de styles personnalisés ( `numSidenotes` et `numSidenotesPopover`, respectivement).

## Ajouter plusieurs collections Sidenotes à une seule page {#section_pjl_ptv_sy}

Livefyre vous permet d&#39;ajouter plusieurs collections Sidenotes à une seule page. Par exemple, si la page comporte trois articles d’actualité, vous pouvez inclure trois itérations distinctes de l’application Sidenotes. Pour ce faire, vous devez définir un objet `ConvConfig` distinct pour chaque instance de Sidenotes que vous souhaitez créer. Par exemple :

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
