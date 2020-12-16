---
description: Activez les commentaires en direct sur votre page.
seo-description: Activez les commentaires en direct sur votre page.
seo-title: Commentaires
solution: Experience Manager
title: Commentaires
uuid: decad9b0-2074-4748-bd77-914008817bfa
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 3%

---


# Commentaires{#comments}

Activez les commentaires en direct sur votre page. Les commentaires vous permettent de remplacer votre système de commentaires par défaut par des conversations en temps réel sur votre page.

## Analytics {#concept_4093E8BAA96A464BA74D263DA031C0B0}

L’incorporation de l’application de commentaires suit le processus d’incorporation d’une application principale décrite dans Prise en main > Incorporation d’une application.

### Exemple

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Comme indiqué dans la section Building CollectionMeta, CollectionMeta est un objet JSON codé. Dans l’exemple ci-dessus, l’objet JSON utilise le format suivant avant d’être codé JWT :

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## Objet NetworkConfig {#c-networkconfig-object}

L&#39;objet `NetworkConfig` est un objet JSON qui personnalise le système d&#39;authentification pour les utilisateurs du réseau.
L&#39;objet `NetworkConfig` est un objet JSON contenant les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| **authDelegate** | **  requiredobject | Utilisé pour personnaliser le système d&#39;authentification pour les utilisateurs réseau personnalisés. |
| **network** | Chaîne *requise* | Nom réseau fourni par Livefyre. Par exemple : *yourname.fyre.co.* |
| **attachementDelegate** | ** optionalobject | Permet de spécifier les types de pièces jointes visibles dans le flux d’application. Pour plus d’informations, voir [Restriction des médias](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **chaînes** | ** optionalobject | Permet de personnaliser les chaînes de texte des éléments HTML dans n’importe quelle application principale Livefyre. Pour plus d’informations, voir [Personnalisations des chaînes](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Objet ConvConfig {#c-convconfig-object}

L’objet `convConfig` est un objet JSON utilisé pour spécifier le contenu rendu par l’application Livefyre sur la page.

>[!NOTE]
>
>Les paramètres d&#39;objet `convConfig` répertoriés ici ne s&#39;appliquent pas à l&#39;application Reviews. Pour plus d’informations sur l’intégration de l’application Reviews à l’aide de l’objet `convConfig`, voir Intégration Reviews.

L&#39;objet `ConvConfig` contient les paramètres requis suivants :

| Paramètre | Type | Description |
|--- |--- |--- |
| **articleId** | *chaîne* requise | Identifie de manière unique une collection de votre site. En règle générale, cela correspond à une clé Principale de base de données ou à un ID de publication dans votre CMS. Par exemple : &quot;post-42&quot;. 255 caractères maximum.  Remarque :  Si vous utilisez l’URL de l’article en tant qu’articleId, assurez-vous que la chaîne est codée au format MD5 ou SHA-1. |
| **authPageReload** | **  optionalboolean | Application pour l’application de commentaires : Permet de contrôler si le commentaire d’un utilisateur est stocké localement pendant le processus d’authentification. Si la valeur est true, si un utilisateur saisit un commentaire, puis se connecte à l’application, le commentaire est stocké localement et réentré dans le champ de contenu après la connexion et l’actualisation de la page. Si elle est définie sur false, le contenu saisi est effacé pendant le processus de connexion et doit être saisi à nouveau. |
| **collectionMeta** | *chaîne* requise | Métadonnées codées JWT sur la collection. Voir [Objet CollectionMeta](#c_collectionmeta_object) pour plus d’informations. |
| **el** | *chaîne* requise | ID d’un élément DOM auquel le flux de contenu sera rendu. |
| **siteId** | *chaîne* requise | Identifiant fourni par Livefyre pour le site Web ou l’application auquel appartient la collection. Par exemple : &quot;303617&quot;. |

>[!NOTE]
>
>Le paramètre `app` n&#39;est pas requis pour une implémentation de l&#39;application de commentaires.

L&#39;objet `ConvConfig` peut également contenir les paramètres facultatifs suivants :

| Paramètre | Type | Description |
|--- |--- |--- |
| **actionButtons** | *tableau* facultatif | Tableau de boutons d’action personnalisés à ajouter à un élément de contenu en regard des boutons Partager et Marquer. Pour plus d’informations, voir Ajouter des boutons personnalisés. |
| **animations** | ** optionalboolean | Définit si les animations s’exécuteront dans l’application Livefyre. Définissez cette variable sur false pour désactiver les animations. La valeur par défaut est true. |
| **anonymousFlaggingEnabled** | ** optionalboolean | Définit si les utilisateurs invités ont la possibilité d’marquer le contenu. La valeur par défaut est true. |
| **browserType** | ** optionalstring | Définit le périphérique pour lequel le contenu d’affichage doit être généré. Cela provoquera la modification du CSS et de certaines fonctionnalités pour qu’il s’adapte au type de périphérique d’entrée. Les options sont Bureau, Mobile ou Tablette. (Si rien n’est indiqué, la détermination de l’agent Google pour le format d’affichage est définie par défaut.) |
| **checksum** | *chaîne* recommandée | Identifie l’état actuel de CollectionMeta. Si vous modifiez cette valeur, Livefyre mettra à jour les données sur le serveur avec les nouvelles valeurs dans CollectionMeta. |
| **datetimeFormat** | **  optionalstring, fonction d’objet | Indique le format datetime du contenu diffusé en continu. Pour plus d’informations, voir Personnalisation des tampons de date et d’heure. |
| **disableAvatars** | ** optionalboolean | Empêche le rendu des avatars dans le flux d’application et réduit ainsi le nombre d’éléments chargés dans le navigateur. La valeur par défaut est false. |
| **disableIE8Shim** | ** optionalboolean | Désactive la shiv par défaut utilisée par Livefyre pour polyremplir Internet Explorer 8 afin que les éléments HTML5 soient pris en charge. Livefyre utilise le projet suivant :  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). La valeur par défaut est false.  Remarque :  Si cette valeur est définie sur false, le polyremplissage d’une sorte ou d’une autre doit être utilisé avant que Livefyre Chat ne soit appelé pour la prise en charge d’Internet Explorer 8. |
| **disableThirdPartyAnalytics** | ** optionalboolean | Désactive les systèmes d’analyse tiers (Quantserve et Google Analytics) que Livefyre peut utiliser pour les mesures internes. La valeur par défaut est false. |
| **editorCss** | ** optionalobject | Permet de personnaliser la mise en forme de l’éditeur de commentaires. Vous pouvez mettre en forme la couleur d’arrière-plan du champ de l’éditeur, ainsi que la couleur, la taille et la famille de la police du texte qui s’affiche dans l’éditeur.  Par exemple: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | ** optionalinteger | Permet de définir le nombre de commentaires par défaut visibles dans votre application au chargement. Il peut s’agir d’un entier compris entre 1 et 50. |
| **initialNumVisibleLegacy** | ** optionalinteger | Permet de définir le nombre par défaut d’éléments de contenu hérités visibles dans votre application au chargement. Il peut s’agir d’un entier compris entre 1 et 50. Si ce paramètre n’est pas spécifié, initialNumVisible est défini par défaut.  Par exemple : Si votre collection comprend 100 commentaires principaux et 100 commentaires hérités, définissez initalNumVisible:10 et initialNumVisibleLegacy:5, pour afficher 10 commentaires principaux (avec un bouton Afficher plus) + 5 commentaires d&#39;archive (avec un bouton Afficher plus). |
| **maxVisible** | ** optionalinteger | Définit le nombre maximal d’éléments visibles du contenu de niveau supérieur dans l’application de messagerie instantanée. Si de nouveaux éléments de contenu sont diffusés dans, le contenu au bas du flux est supprimé de la page. Si vous cliquez sur le bouton Afficher plus..., le paramètre est ignoré et l’utilisateur est libre d’afficher autant de contenu que vous le souhaitez. (Utilisez ce paramètre pour contrôler le nombre d’éléments qui apparaissent sur la page dans les flux à grande vitesse.) |
| **postToButtons** | *tableau* facultatif | Permet de configurer les fournisseurs qui s&#39;affichent lors de l&#39;incorporation de l&#39;application Live Blog. Les options disponibles sont deux (Twitter), fb (Facebook) et li (LinkedIn). Par défaut, [ tw, fb ]. |
| **readOnly** | ** optionalboolean | Désactive toute interactivité pour la collection. Lorsque la valeur est true, les utilisateurs ne peuvent pas se connecter au flux et ne peuvent pas publier, modifier, répondre ou aimer du contenu. Lorsque la valeur est true, les utilisateurs peuvent marquer et partager du contenu. La valeur par défaut est false. |
| **stream** | ** optionalobject | Contient des options de configuration de la diffusion en continu de l’application. |
| **stream.catchup** | ** optionalinteger | Indique le nombre de secondes avant le moment actuel de chargement du flux. Par défaut, Livefyre charge 50 éléments de contenu, puis charge tout le contenu envoyé entre ceux-ci et le moment présent. Dans les cas d’utilisation très rapide, le contenu peut être publié trop rapidement pour permettre à l’application de &quot;rattraper&quot; le temps écoulé. Utilisez ce paramètre pour définir le nombre de secondes avant aujourd’hui pour lequel le contenu sera publié (après le chargement initial du contenu). |
| **stream.delay** | ** optionalinteger | Indique le nombre de secondes entre les demandes de diffusion en continu. Utilisez ce paramètre pour contrôler le flux du contenu et retarder la fréquence de mise à jour du DOM.  Remarque :  S’il est trop grand, le flux peut être en retard. |


>[!NOTE]
>
>Vous pouvez transmettre un ou plusieurs objets `convConfig` lors de l’initialisation de l’application afin d’afficher plusieurs applications sur la même page. Gardez à l’esprit que les applications supplémentaires utilisent les ressources et les performances du navigateur peuvent se dégrader à mesure que le nombre augmente.

## CollectionMeta, objet {#c-collectionmeta-object}

L’objet `CollectionMeta` est un objet JSON qui spécifie les métadonnées à stocker dans la collection.

`CollectionMeta` est toujours codée avant d’être transmise à Livefyre pour des raisons de sécurité. La valeur codée est transmise à l’objet `ConvConfig` illustré ci-dessus.

>[!NOTE]
>
>Vous devez ajouter du code côté serveur pour coder l’objet JSON `CollectionMeta`. Voir Création de jetons côté serveur pour plus d’informations.

| Paramètre | Type | Description |
|--- |--- |--- |
| **articleId** | *chaîne* requise | Identifiant unique de la collection. |
| **titre** | *chaîne* requise | Titre que vous souhaitez appliquer à la collection. Cela correspond souvent au titre de la page qui affiche l’application.  Par exemple : &quot;L&#39;intégration est tellement amusante !&quot; <br>**Remarque :**  La longueur maximale des caractères pour le titre est de 255 caractères. Le champ de titre ne prend pas en charge les entités HTML. Veuillez coder des caractères spéciaux au format UTF-8. |
| **url** | *chaîne* requise | URL absolue canonique que vous souhaitez joindre à cette collection. Cette URL sera utilisée pour générer des liens vers l’application à partir du contenu partagé sur Facebook et Twitter, des notifications par courrier électronique et Livefyre Studio.  <br>**** NoteLivefyre requiert l&#39;utilisation d&#39;un nom de domaine complet ; le numéro de port ou un rappel pour résoudre la configuration locale n&#39;est pas requis. Si le test est effectué localement, veillez à utiliser un domaine d’URL de base valide. <br>Par exemple :  `https://customer.com` est valide, alors qu’ `https://localhost:5995` il ne l’est pas. Une fois que vous avez configuré votre serveur Web local pour accepter un nom de domaine complet, aucun rappel ou aucune résolution n’est nécessaire et le développement local peut se poursuivre comme prévu. |
| **type** | *chaîne* requise | Type de collection. Doit être `livechat`. |

L&#39;objet `CollectionMeta` peut également contenir le paramètre facultatif suivant :

| Paramètre | Type | Description |
|---|---|---|
| **balises** | ** optionalstring | Liste de mots-clés ou d’expressions séparés par des virgules. Rechercher des collections par balises dans Studio ou avec l&#39;API de recherche. <br> **Remarque :** Bien que les balises ajoutées via Studio puissent contenir des espaces, les balises saisies via l’API ne le peuvent pas. Utilisez des traits de soulignement pour définir des balises qui afficheront des espaces dans l’interface utilisateur. (Par exemple : utilisez `Monday_Quarterback` pour afficher le rapport du lundi dans Studio.) |

## Ajouter un gestionnaire de Événements {#concept_06D8B811C98B4CC6B38C6340EBA176E5}

Pour enregistrer les gestionnaires de événement, utilisez l’appel widget.on dans la fonction de rappel de l’application.

### Par exemple

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
