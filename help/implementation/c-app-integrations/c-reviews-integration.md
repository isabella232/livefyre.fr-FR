---
description: Permettre aux clients d’évaluer et de consulter vos offres de produits.
seo-description: Permettre aux clients d’évaluer et de consulter vos offres de produits.
seo-title: Critiques
solution: Experience Manager
title: Critiques
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Critiques {#reviews}

Permettre aux clients d’évaluer et de consulter vos offres de produits.

Les revues permettent aux membres de votre communauté de contribuer aux évaluations par étoiles et aux évaluations qualitatives de tout produit ou service.

## Analytics {#section_kk5_15b_c1b}

Pour intégrer une application de révision, suivez la procédure d’intégration d’une application de conversation. Voir [Incorporation d’une application](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Voici un exemple d’application de révisions intégrée.

### Exemple

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

Comme indiqué dans la section Création `CollectionMeta` , `CollectionMeta` est un objet JSON codé. Dans l’exemple ci-dessus, l’objet JSON utilise le format suivant avant d’être codé JWT :

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig, objet {#section_pzv_ytb_c1b}

Si vous avez déjà terminé la section Prise en main, vous devez connaître l’objet convConfig. Pour activer les révisions, mettez à jour convConfig avec les champs suivants :

* **alwaysShowEditor** *facultative* booléenne : Par défaut, l’éditeur de révisions s’affiche uniquement lorsque l’utilisateur appuie sur le bouton "Ecrire la révision". Définissez ce paramètre sur true pour toujours afficher l’éditeur.

* **chaîne** obligatoire *de l’application* : Nom de l’application à utiliser pour les révisions. Doit être "révisions".

* **defaultSort** chaîne *facultative* : Permet de sélectionner l’option de tri par défaut pour les révisions. Les valeurs possibles sont les suivantes : mostHelpful, highRated, plus lowRated, plus récent et plus ancien.

* **disableTitle** *optional* boolean : Désactive et masque le champ de titre dans l’éditeur de révisions, qui est obligatoire et visible par défaut. La valeur par défaut est true.

* **enableHalfRating** *facultative* booléenne : Utilisé pour activer les demi-évaluations sur le module de sélection d’étoiles par défaut. La valeur par défaut est true.

* **hideShowReviewButton** *facultative* booléenne : Contrôle si le [!UICONTROL Show My Review] bouton doit être affiché. Définissez cette variable sur true pour permettre à vos utilisateurs de choisir d’afficher ou non leurs propres révisions.

* **maxRating** *optional* integer Utilisé pour définir le nombre d’étoiles affichées sur le module de sélection d’étoiles par défaut. La valeur par défaut est 5. Il peut être configuré jusqu’à 100.

* **ratingSummaryEnabled** *facultative* booléenne : Permet d’afficher la vue de synthèse de l’évaluation au-dessus de l’application de révisions. Ceci doit être activé pour utiliser la noteSummaryDelegate. La valeur par défaut est true.

## Vérifier les métadonnées de la collection {#section_k1s_sqb_c1b}

* **** type : Chaîne *requise* : Définit le type de collection. Ça doit être `reviews`.

* **ratingDimensions** tableau *facultatif* : Tableau de chaînes pour chaque type de dimension que cette collection utilisera. Si cette valeur n’est pas spécifiée, seule 1 dimension est autorisée.

   Par exemple, pour permettre aux utilisateurs d’évaluer votre produit sur "design", "fonctionnalités" et "performances", définissez la baie sur : `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **Entier** facultatif *des sous-parties* de notation : Nombre de partitions à afficher dans la zone de texte de la révision. Les libellés de sous-partie sont transmis avec le paramètre comme illustré ci-dessous.

   >[!NOTE]
   >Vous devez définir des libellés pour chaque sous-partie.

* **tableau** facultatif ** desID de sous-parties de notation: Vous permet de définir un ID pour chaque sous-partie de votre collection de notes, qui peut être utilisé pour cibler ces éléments de sous-partie dans votre CSS et JavaScript. Lorsque les utilisateurs publient des révisions, chacun `ratingSubpart` dispose de l’attribut " `data-lf-subpart-id`" dessus, renseigné par cet identifiant.

>[!NOTE]
>
>Pour l’utiliser `ratingSubpartsIds`, le `ratingSubparts` paramètre doit également être défini et la longueur des deux tableaux doit correspondre.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>Si vous utilisez `ratingDimensions`, vous DEVEZ utiliser `ratingSelectionDelegate`, `ratingDisplayDelegate`et `ratingSummaryDelegate` (si vous voulez afficher le résumé de la note).

## Personnalisation des révisions {#section_khz_xmb_c1b}

### Configuration des images en étoile

Pour changer l'image pour les étoiles complètes, la classe est `goog-ratings-star`. Remplacez l’image d’arrière-plan par l’image de votre choix. Par défaut, les étoiles font 28 x 28 pixels.

### Configuration d’images d’étoiles avec demi-étoiles

Avec les demi-étoiles, il y a deux classes, une pour chaque côté de l'étoile. Le côté gauche de la demi-étoile est `fyre-rating-half-odd` et le côté droit `fyre-rating-half-even`. Par défaut, les demi-étoiles représentent 28 x 14 pixels.

### Configuration des valeurs d’info-bulle pour les étoiles

Pour configurer les valeurs d’info-bulle pour les étoiles, suivez le texte personnalisé décrit dans Personnalisations des chaînes. Une fois cette configuration effectuée, utilisez la clé `ratingValues` et la valeur d’un tableau contenant les chaînes d’info-bulle. Si vous avez désactivé les demi-étoiles, le nombre d’éléments du tableau doit être le même que `maxRating` (ci-dessus). Si vous avez activé les demi-étoiles, le nombre d’éléments doit être de 2x `maxRating`. Le premier élément du tableau correspond à l’élément étoile (ou demi-étoile) le plus à gauche et continue de gauche à droite.

### Active/désactive l’option "Afficher ma révision"

Pour activer ou désactiver l’ [!UICONTROL Show My Review] option, ciblez le `hideShowReviewButton` paramètre dans la configuration de l’application.

### Afficher l’éditeur de texte par défaut

L’éditeur de révisions s’affiche uniquement lorsque l’utilisateur appuie sur le [!UICONTROL write review] bouton. Pour afficher ce formulaire par défaut, ciblez le `alwaysShowEditor` paramètre dans la configuration de l’application.
