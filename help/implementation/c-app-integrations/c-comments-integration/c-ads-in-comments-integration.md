---
description: Insérez des publicités dans votre flux de commentaires.
seo-description: Insérez des publicités dans votre flux de commentaires.
seo-title: Publicités dans les commentaires
solution: Experience Manager
title: Publicités dans les commentaires
uuid: f 8 d 6372 f -4468-4884-a 384-116180 b 4 c 748
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Publicités dans les commentaires{#ads-in-comments}

Insérez des publicités dans votre flux de commentaires.

## Publicités dans les commentaires {#topic_CDD2ACF16AED4DE782725EE90089C04E}

Insérez des publicités dans votre flux de commentaires.

La fonction Publicités Livefyre de commentaires permet d'insérer des publicités dans votre flux de commentaires, de définir la fréquence à laquelle les publicités apparaissent dans le flux et de créer des délégués d'injection asynchrones et asynchrones.

Livefyre fournit le conteneur par lequel vous pouvez injecter une publicité à l'aide de votre fournisseur de solutions de gestion des publicités.

Pour insérer une publicité, transmettez deux valeurs Livefyre :

* Fréquence à laquelle la publicité doit être injectée dans le flux de commentaires
* Fonction qui diffuse la publicité appropriée.

>[!NOTE]
>
>Les publicités ne seront rendues que lorsque le placement de la publicité se trouve dans la fenêtre d'affichage. Les publicités ne s'afficheront qu'après des commentaires parents (et non dans des threads) et les utilisateurs ne pourront pas commenter ces publicités. Cette API ne vous permet pas de spécifier la taille de l'élément dans lequel vos publicités seront placées.

## Analytics{#concept_C99029E618EC49779E3117D2C303E4F1}

Pour utiliser cette fonctionnalité, créez un élément div sur la page dans laquelle les publicités seront placées, puis transmettez le code HTML de votre fournisseur de publicités.

Livefyre fournit deux types de placement publicitaire : synchrone et asynchrone. Les deux types ne chargent vos publicités que lorsque l'utilisateur fait défiler la page de telle sorte que sa position soit dans l'affichage. Vous devez également renvoyer un élément DOM (iframe ou div).

Pour obtenir la publicité, les appels de méthode synchrones sont appelés dans un référentiel local, alors qu'appels asynchrones à un service externe.

### Synchrone

Pour créer un placement synchrone, incluez la publicité dans le délégué et renvoyez l'élément publicitaire lui-même. La méthode synchrone appelle un référentiel local, ce qui vous permet de gérer votre propre génération de publicité.

### Asynchrone

La méthode asynchrone requiert que l'élément soit inséré dans le DOM avant d'appeler le fournisseur d'annonces. Votre fournisseur détermine ensuite la publicité à envoyer et la renvoie.

Pour implémenter des publicités asynchrones, créez un délégué qui renvoie un élément dans lequel la publicité sera placée, ainsi qu'un rappel qui exécutera le placement de la publicité. L'élément renvoyé dans le délégué doit avoir un identifiant unique pour que la publicité cible. Le rappel insère la publicité dans l'élément fourni par l'ID unique.

>[!NOTE]
>
>Selon votre fournisseur d'annonces, le rappel se comporte différemment.

Lorsque la page se charge, les publicités dans les commentaires atteignent le délégué, injectent l'élément, puis appelle le rappel qui met à jour l'élément (précédemment défini) avec la publicité.

## Paramètres {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

Les paramètres suivants peuvent être utilisés avec cet appel.

Pour l'objet ad :

* **delay :****(facultatif) integer** : définit le nombre de commentaires après lesquels la première publicité s'affiche. La valeur par défaut est 10.
* **fréquence : (facultatif) integer** : définit le nombre de commentaires après lesquels chaque publicité suivante sera affichée. Par exemple : Saisissez 2 pour afficher une publicité sous la forme de tous les trois commentaires. La valeur par défaut est 10.
* **delegate :*****fonction requise*** - Fonction appelée pour insérer des publicités dans le flux Commentaires.

L'objet délégué prend en charge les appels publicitaires asynchrones et asynchrones. Le paramètre attribué à la fonction déléguée, aux données, contiendra :

* **title :****string** - Titre de la collection.
* **balises :****tableau** - Liste des balises associées à la collection.
* **id :****chaîne** - Identifiant de l'article de la collection.
* **url :****chaîne** - URL de la collection.
* **Networkid :****string** - Identifiant réseau de la collection.
* **Siteid :****int** - Identifiant de site de la collection.

Ces éléments sont transmis par l'intermédiaire de l'objet convconfig dans notre exemple ; ils sont expliqués plus en détail dans la [section Prise en main](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) .

### Synchrone

Le délégué renvoie un objet contenant :

* **element :*****élément* DOM requis** : élément contenant la publicité à insérer dans l'application.

**Asynchrone**: Le délégué renvoie un objet contenant : Le délégué renvoie un objet contenant deux propriétés : élément et rappel :

* **element :*****élément* DOM requis** : élément contenant la publicité à insérer dans l'application.
* **rappel :*****fonction requise*** - Rappel qui traitera l'insertion de la publicité dans l'élément DOM ci-dessus.

Pour `Conv` l'objet, vous pouvez transmettre une chaîne pour représenter le titre de la section de publicité :

* **chaînes :****(facultatif)** - Utilisé pour personnaliser le texte d'en-tête de vos publicités. « Sponsorisé » par défaut.

## Exemple synchrone {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## Exemple asynchrone {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
