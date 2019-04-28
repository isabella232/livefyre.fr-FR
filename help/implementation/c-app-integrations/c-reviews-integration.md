---
description: Permettez aux clients d'évaluer et de consulter vos offres de produits.
seo-description: Permettez aux clients d'évaluer et de consulter vos offres de produits.
seo-title: Révisions
solution: Experience Manager
title: Révisions
uuid: b 740 ee 28-f 6 f 9-4 ae 7-9 fe 7-61 a 5 cde 97 bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Révisions {#reviews}

Permettez aux clients d&#39;évaluer et de consulter vos offres de produits.

Les révisions permettent aux membres de votre communauté de contribuer à des évaluations d&#39;étoiles et à des révisions qualitatives pour tout produit ou service.

## Analytics{#section_kk5_15b_c1b}

Pour intégrer une application de révision, suivez la procédure d&#39;intégration d&#39;une application de conversation. Voir [Incorporation d&#39;une application](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Voici un exemple d&#39;application de révision intégrée.

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

Comme indiqué dans `CollectionMeta` la section Building, `CollectionMeta` est un objet JSON codé. Dans l&#39;exemple ci-dessus, l&#39;objet JSON adopte le format suivant avant son codage JWT :

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Objet convconfig {#section_pzv_ytb_c1b}

Si vous avez déjà terminé la section Prise en main, vous devez vous familiariser avec l&#39;objet convconfig. Pour activer les révisions, mettez à jour convconfig avec les champs suivants :

* **Alwaysshoweditor** *optionnel* : Par défaut, l&#39;éditeur de révisions s&#39;affiche uniquement après que l&#39;utilisateur a appuyé sur le bouton « write review ». Définissez ce paramètre sur true pour toujours afficher l&#39;éditeur.

* **chaîne** *requise* pour l&#39;application : Nom de l&#39;application à utiliser pour les révisions. Il doit s&#39;agir de « révisions ».

* **Chaîne** *facultative* defaultsort : Permet de sélectionner l&#39;option de tri par défaut pour les révisions. Les valeurs possibles sont les suivantes : Mosthelpful, highestrated, lowestrated, newest et le plus ancien.

* **Disabletitle** *optional* boolean : Désactive et masque le champ Titre dans l&#39;éditeur de révisions, obligatoire et visible par défaut. La valeur par défaut est true.

* **Enablehalfrating** *optional* boolean : Utilisé pour activer la moitié des évaluations sur le module de sélection d&#39;étoile par défaut. La valeur par défaut est true.

* **Hideshowreviewbutton** *optionnel* : Contrôle si [!UICONTROL Show My Review] le bouton s&#39;affiche. Définissez cette variable sur true pour permettre aux utilisateurs de choisir d&#39;afficher ou d&#39;afficher leurs propres révisions.

* **Maxrating** *Optional* integer Used to set the number of stars that are shown on the default star selection. La valeur par défaut est 5. Cette valeur peut être configurée jusqu&#39;à 100.

* **Ratingsummaryenabled** *optional* boolean : Utilisé pour afficher la vue récapitulative de la note au-dessus de l&#39;application de révision. Cette opération doit être activée pour utiliser ratingsummarydelegate. La valeur par défaut est true.

## Vérification des métadonnées de la collection {#section_k1s_sqb_c1b}

* **type :***chaîne requise* : Définit le type Collection. `reviews`Doit être.

* **Ratingdimensions** *facultatif* : Tableau de chaînes pour chaque type de dimension utilisé par cette collection. Si cette valeur n&#39;est pas spécifiée, seule une dimension est autorisée.

   Par exemple, pour permettre aux utilisateurs d&#39;évaluer votre produit sur « conception », « fonctionnalités » et « performance », définissez le tableau sur : `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **Ratingsubpart** *optional* integer : Nombre de partitions à afficher dans la zone de texte de la révision. Les étiquettes de sous-partie sont transmises avec le paramètre comme illustré ci-dessous.

   >[!NOTE]
   >Vous devez définir des libellés pour chaque sous-partie.

* **Ratingsubpartsids** *facultatif* : Permet de définir un identifiant pour chaque sous-partie de votre collection d&#39;évaluations, qui peut être utilisée pour cibler ces éléments de sous-partie dans votre CSS et JavaScript. Lorsque les utilisateurs publient des révisions, chacun `ratingSubpart` d&#39;eux aura l&#39;attribut `data-lf-subpart-id`«  », renseigné avec cet ID.

>[!NOTE]
>
>A utiliser `ratingSubpartsIds`, le `ratingSubparts` paramètre doit également être défini et la longueur des deux tableaux doit correspondre.

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
>Si vous utilisez `ratingDimensions`, vous DEVEZ utiliser la `ratingSelectionDelegate`, `ratingDisplayDelegate`et `ratingSummaryDelegate` (si vous souhaitez afficher le résumé de la note).

## Révision de la personnalisation {#section_khz_xmb_c1b}

### Configuration des images d&#39;étoile

Pour modifier l&#39;image pour les étoiles complètes, la classe est `goog-ratings-star`. Remplacez l&#39;image d&#39;arrière-plan par l&#39;image de votre choix. Par défaut, les étoiles sont 28 x 28 pixels.

### Configuration des images etoiles avec des demi-étoiles

Avec les demi-étoiles, il existe deux classes, une pour chaque côté de l&#39;étoile. The left side of the half star is `fyre-rating-half-odd` and the right side is `fyre-rating-half-even`. Par défaut, la moitié des étoiles est de 28 x 14 pixels.

### Configuration des valeurs d&#39;info-bulle pour les étoiles

Pour configurer les valeurs d&#39;info-bulle des étoiles, suivez le texte personnalisé décrit dans la section Personnalisations de chaînes. Une fois cette configuration configurée, utilisez la clé `ratingValues` et la valeur un tableau contenant les chaînes d&#39;info-bulle. Si la moitié des étoiles est désactivée, le nombre d&#39;éléments du tableau doit être identique à `maxRating` celui de (ci-dessus). Si la moitié des étoiles est activée, le nombre d&#39;éléments doit être 2 x `maxRating`. Le premier élément du tableau correspond à l&#39;étoile la plus à gauche (ou à la moitié) et continue de gauche à droite.

### Activer/désactiver l&#39;option Afficher ma révision

Pour activer ou désactiver l&#39; [!UICONTROL Show My Review] option, ciblez `hideShowReviewButton` le paramètre dans la configuration de l&#39;application.

### Afficher l&#39;éditeur de texte par défaut

L&#39;éditeur des révisions s&#39;affiche uniquement lorsque l&#39;utilisateur appuie sur [!UICONTROL write review] le bouton. Pour afficher ce formulaire par défaut, ciblez le `alwaysShowEditor` paramètre dans la configuration de l&#39;application.
