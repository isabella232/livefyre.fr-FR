---
description: Permettre aux clients d’évaluer et de consulter vos offres de produits.
seo-description: Permettre aux clients d’évaluer et de consulter vos offres de produits.
seo-title: Critiques
solution: Experience Manager
title: Critiques
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 0%

---


# Critiques {#reviews}

Permettre aux clients d’évaluer et de consulter vos offres de produits.

Les revues permettent aux membres de votre communauté de contribuer aux évaluations des étoiles et aux évaluations qualitatives de tout produit ou service.

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

Comme indiqué dans la section Création `CollectionMeta`, `CollectionMeta` est un objet JSON codé. Dans l’exemple ci-dessus, l’objet JSON utilise le format suivant avant d’être codé en JWT :

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

Si vous avez déjà terminé la section Prise en main, vous devez vous familiariser avec l’objet convConfig. Pour activer les révisions, mettez à jour convConfig avec les champs suivants :

* **** ** alwaysShowEditoroptionalboolean : Par défaut, l’éditeur de révisions n’apparaît qu’une fois que l’utilisateur a appuyé sur le bouton &quot;Ecrire la révision&quot;. Définissez ce paramètre sur true pour toujours afficher l’éditeur.

* **** ** apprequiredstring : Nom de l’application à utiliser pour les révisions. Doit être une &quot;révision&quot;.

* **** ** defaultSortoptionalstring : Permet de sélectionner l’option de tri par défaut pour les révisions. Les valeurs possibles sont les suivantes : mostHelpful, mostRated, lowerRated, plus récent et plus ancien.

* **** ** disableTitleoptionalboolean : Désactive et masque le champ de titre dans l’éditeur de révisions, qui est obligatoire et visible par défaut. La valeur par défaut est true.

* **** ** enableHalfRatingoptionalboolean : Utilisé pour activer les évaluations à moitié sur le module de sélection d’étoiles par défaut. La valeur par défaut est true.

* **** ** hideShowReviewButtonoptionalboolean: Contrôle si le  [!UICONTROL Show My Review] bouton s’affiche. Définissez cette variable sur true pour permettre aux utilisateurs d’afficher ou d’afficher leurs propres révisions.

* **** ** maxRatingoptionalinteger Utilisé pour définir le nombre d’étoiles affichées sur le module de sélection d’étoiles par défaut. La valeur par défaut est 5. Il peut être configuré jusqu’à 100.

* **** ** ratingSummaryEnabledoptionalboolean : Permet d’afficher la vue de résumé de note au-dessus de l’application de révisions. Ceci doit être activé pour utiliser la noteSummaryDelegate. La valeur par défaut est true.

## Vérifier les métadonnées de la collection {#section_k1s_sqb_c1b}

* **type:** ** required string : Définit le type de collection. Doit être `reviews`.

* **** ** ratingDimensionsoptionalarray : Tableau de chaînes pour chaque type de dimension que cette collection utilisera. Si cette valeur n’est pas spécifiée, seule 1 dimension est autorisée.

   Par exemple, pour permettre aux utilisateurs d&#39;évaluer votre produit en fonction de sa conception, de ses fonctionnalités et de ses performances, définissez la baie sur : `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsoptionalinteger : Nombre de partitions à afficher dans la zone de texte de la révision. Les étiquettes de sous-pièce sont transmises avec le paramètre, comme illustré ci-dessous.

   >[!NOTE]
   >Vous devez définir des étiquettes pour chaque sous-partie.

* **** ** ratingSubpartsIdsoptionalarray : Permet de définir un identifiant pour chaque sous-partie de votre collection de classifications, qui peut être utilisé pour cible de ces éléments de sous-parties dans votre CSS et votre code JavaScript. Lorsque les utilisateurs publient des révisions, chaque `ratingSubpart` comporte l’attribut &quot;`data-lf-subpart-id`&quot; sur lui, renseigné avec cet identifiant.

>[!NOTE]
>
>Pour utiliser `ratingSubpartsIds`, le paramètre `ratingSubparts` doit également être défini et la longueur des deux tableaux doit correspondre.

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
>Si vous utilisez `ratingDimensions`, vous DEVEZ utiliser `ratingSelectionDelegate`, `ratingDisplayDelegate` et `ratingSummaryDelegate` (si vous souhaitez afficher le résumé de la note).

## Reviews Customization {#section_khz_xmb_c1b}

### Configuration des images en étoile

Pour modifier l&#39;image pour les étoiles complètes, la classe est `goog-ratings-star`. Remplacez l’image d’arrière-plan par l’image de votre choix. Par défaut, les étoiles représentent 28 x 28 pixels.

### Configuration d’images en étoile avec demi-étoiles

Avec les demi-étoiles, il y a deux classes, une pour chaque côté de l&#39;étoile. Le côté gauche de la demi-étoile est `fyre-rating-half-odd` et le côté droit est `fyre-rating-half-even`. Par défaut, les demi-étoiles représentent 28 x 14 pixels.

### Configuration des valeurs d’info-bulle pour les étoiles

Pour configurer les valeurs d’info-bulle pour les étoiles, suivez le texte personnalisé décrit dans Personnalisations des chaînes. Une fois cette configuration effectuée, utilisez la clé `ratingValues` et la valeur d&#39;un tableau contenant les chaînes d&#39;info-bulle. Si la demi-étoile est désactivée, le nombre d&#39;éléments de la baie doit être le même que `maxRating` (ci-dessus). Si les demi-étoiles sont activées, le nombre d’éléments doit être de 2x `maxRating`. Le premier élément du tableau correspond à l&#39;élément étoile (ou demi-étoile) le plus à gauche et continue de gauche à droite.

### Active/désactive l&#39;option Afficher ma révision

Pour activer ou désactiver l&#39;option [!UICONTROL Show My Review], cible le paramètre `hideShowReviewButton` dans la configuration de l&#39;application.

### Afficher l’éditeur de texte par défaut

L’éditeur de révisions n’apparaît qu’après que l’utilisateur a appuyé sur le bouton [!UICONTROL write review]. Pour afficher ce formulaire par défaut, cible le paramètre `alwaysShowEditor` dans la configuration de l’application.
