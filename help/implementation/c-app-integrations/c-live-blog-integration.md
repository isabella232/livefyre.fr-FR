---
description: Le blog en direct vous permet de présenter des mises à jour et des images
  en temps réel des éditeurs de votre site lors de la couverture d'un événement en
  direct.
seo-description: Le blog en direct vous permet de présenter des mises à jour et des
  images en temps réel des éditeurs de votre site lors de la couverture d'un événement
  en direct.
seo-title: Blog en direct
solution: Experience Manager
title: Blog en direct
uuid: 5 ca 373 f 1-2008-45 ab -9 ec 2-1 e 295 af 4 e 368
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Blog en direct{#live-blog}

Le blog en direct vous permet de présenter des mises à jour et des images en temps réel des éditeurs de votre site lors de la couverture d'un événement en direct.

## Blog en direct {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

Le blog en direct vous permet de présenter des mises à jour et des images en temps réel des éditeurs de votre site lors de la couverture d'un événement en direct.

## Analytics{#c_live_blog_integration}

Le blog en direct vous permet de présenter des mises à jour et des images en temps réel des éditeurs de votre site lors de la couverture d'un événement en direct.

Pour incorporer une application de blog en direct, suivez la procédure d'incorporation d'une application. Voir [Incorporation d'une application](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Voici un exemple de ce à quoi ressemble une application de blog Live intégrée.

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
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(blogWidget) {}); 
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

Collectionmeta est un objet JSON codé. Dans l'exemple ci-dessus, l'objet JSON adopte le format suivant avant son codage JWT :

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## Objet networkconfig {#c-networkconfig-object}

`NetworkConfig` L'objet est un objet JSON qui personnalise le système d'authentification pour les utilisateurs du réseau.

`NetworkConfig` L'objet est un objet JSON contenant les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| **Authdelegate** | *required* object | Utilisé pour personnaliser le système d'authentification pour les utilisateurs réseau personnalisés. |
| **réseau** | *chaîne requise* A Livefyre-provided name name. Par exemple : *yourname. fyre. co.* |
| **Attachmentdelegate** | *optional* object | Utilisé pour spécifier les types de pièces jointes visibles dans le flux de l'application. Pour plus d'informations, voir [Limitation du support](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **chaînes** | *optional* object | Utilisé pour personnaliser les chaînes de texte des éléments HTML dans l'une des applications de base Livefyre. Pour plus d'informations, voir [Personnalisations de chaînes](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Objet convconfig {#c-convconfig-object}

`convConfig` L'objet est un objet JSON utilisé pour spécifier le contenu généré par l'application Livefyre sur la page.

>[!NOTE]
>
>Les paramètres `convConfig` d'objet répertoriés ici ne s'appliquent pas à l'application Reviews. Pour obtenir des informations sur l'intégration à l'application Révision à l'aide de `convConfig` l'objet, voir Révision de l'intégration.

`ConvConfig` L'objet contient les paramètres requis suivants :

| Paramètre | Type | Description |
|--- |--- |--- |
| **Articleid** | *required* string | Identifie de manière unique une collection sur votre site. Habituellement, cela correspond à une clé principale de base de données ou à un ID de publication dans votre CMS. Par exemple : « post -42 ». 255 caractères maximum. Remarque : Si vous utilisez l'URL de l'article comme articleid, assurez-vous que la chaîne est codée MD 5 ou SHA -1. |
| **Collectionmeta** | *required* string | Métadonnées codées JWT relatives à la collection. Voir collectionmeta Object pour plus d'informations. |
| **el** | *required* string | ID d'un élément DOM auquel le flux de contenu sera rendu. |
| **Siteid** | *required* string | Identifiant fourni par Livefyre pour le site Web ou l'application auquel la collection appartient. Par exemple : « 303617 ». |

>[!NOTE]
>
>`app` Le paramètre n'est pas requis pour une implémentation de l'application de commentaires.

L `ConvConfig` 'objet peut également contenir les paramètres facultatifs suivants :

| Paramètre | Type | Description |
|--- |--- |--- |
| **Actionbutton** | *optional* array | Tableau des boutons d'action personnalisés à ajouter à un élément de contenu en regard des boutons Partager et Marquer. Pour plus d'informations, voir Ajout de boutons personnalisés. |
| **animations** | *optional* boolean | Indique si les animations s'exécutent dans l'application Livefyre. Définissez cette valeur sur false pour désactiver les animations. Par défaut, true. |
| **Anonymousflaggingenabled** | booléenne | Indique si les utilisateurs invités ont la possibilité de marquer le contenu. La valeur par défaut est true. |
| Browsertype | *optional* String | Définit le périphérique pour lequel le contenu d'affichage doit être généré. La feuille de style CSS, ainsi que certaines fonctionnalités, changent pour s'adapter au type de périphérique d'entrée. Options are desktop, mobile, or tablet. (Si rien n'est renseigné, par défaut, la détermination de l'agent Google pour le format d'affichage est déterminée.) |
| **checksum** | *chaîne facultative* (recommandée) | Identifie l'état actuel de collectionmeta. Si vous modifiez cette valeur, Livefyre met à jour les données du serveur avec les nouvelles valeurs de collectionmeta. |
| **Datetimeformat** | *chaîne facultative* , fonction d'objet | Indique le format de date de données du contenu en flux continu. Pour plus d'informations, voir Personnalisation des horodatages et heure. |
| Disableavatars | *optional* boolean | Empêche le rendu des avatars dans le flux d'application et réduit ainsi le nombre d'éléments chargés dans le navigateur. La valeur par défaut est false. |
| disableIE8Shim | *optional* boolean | Désactive la valeur shiv par défaut utilisée par Livefyre pour le polyremplissage Internet Explorer 8 afin que les éléments HTML 5 soient pris en charge. Livefyre utilise le projet suivant : [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . La valeur par défaut est false. Remarque : Si cette valeur est false, le polyremplissage d'un tri doit être utilisé avant l'appel de Livefyre Chat pour la prise en charge d'Internet Explorer 8. |
| **Disablethirdpartyanalytics** | *optional* boolean | Désactive les systèmes d'analyse tiers (Quantserve et Google Analytics) que Livefyre peut utiliser pour les mesures internes. La valeur par défaut est false. |
| **Editorcss** | *optional* object | Utilisé pour personnaliser le style de l'éditeur de commentaires. Vous pouvez mettre en forme la couleur d'arrière-plan du champ de l'éditeur ainsi que la couleur, la taille et la famille de la police du texte qui s'affiche dans l'éditeur. Par exemple : {background : ' # ccc ', color : ' rouge ', police : ' 30 px "Helvetica Neue », Helvetica, Arial, Geneva, sans-serif '} |
| **Initialnumvisible** | *optional* integer | Permet de définir le nombre par défaut de commentaires visibles dans votre application au chargement. Il peut s'agir d'un entier compris entre 1 et 50. |
| **Initialnumvisiblelegacy** | *optional* integer | Permet de définir le nombre par défaut d'éléments de contenu hérités visibles dans votre application au chargement. Il peut s'agir d'un entier compris entre 1 et 50. Si ce paramètre n'est pas spécifié, la valeur par défaut est initialnumvisible. Par exemple : Si votre collection comprend 100 commentaires actifs et 100 commentaires hérités, définissez initalnumvisible : 10 et initialnumvisiblelegacy : 5, pour afficher 10 commentaires actifs (avec un bouton Afficher plus) + 5 commentaires d'archive (avec un bouton Afficher plus). |
| **Maxvisible** | *optional* integer | Définit le nombre maximal de parties visibles du contenu de niveau supérieur dans l'application de Chat. Si de nouvelles parties du flux de contenu dans, le contenu au bas du flux est supprimé de la page. Si vous cliquez sur le bouton Afficher plus…, le paramètre est ignoré et l'utilisateur peut afficher autant de contenu que vous le souhaitez. (Utilisez ce paramètre pour contrôler le nombre d'éléments qui apparaissent sur la page dans des flux de vélocité élevée.) |
| **Posttobuttons** | *optional* array | Utilisé pour configurer les fournisseurs qui s'affichent lors de l'intégration de l'application de blog en direct. Les options disponibles sont tw (Twitter), fb (Facebook) et li (linkedin). Defaults to [ tw, fb ]. |
| **Readonly** | *optional* boolean | Désactive toute interactivité pour la collection. Lorsque la valeur est true, les utilisateurs ne pourront pas se connecter au flux et ne peuvent pas publier, modifier, répondre ou aimer un contenu. Lorsque la valeur est true, les utilisateurs peuvent marquer et partager du contenu. La valeur par défaut est false. |
| **stream** | *optional* object | Contient des options permettant de configurer la diffusion en continu de l'application. |
| stream. catchup | *optional* integer | Indique le nombre de secondes précédant le moment actuel auquel le flux doit être chargé. Par défaut, Livefyre charge 50 éléments de contenu, puis charge tout le contenu envoyé entre ces deux éléments. Dans des cas d'utilisation très rapides, le contenu peut être publié trop rapidement pour permettre à l'application de prendre le relais. Utilisez ce paramètre pour définir le nombre de secondes précédant le contenu qui sera publié (après le chargement initial du contenu). |
| **stream. delay** | *optional* integer | Indique le nombre de secondes entre les demandes de flux. Utilisez ce paramètre pour contrôler le flux du contenu et retarder la fréquence de mise à jour du DOM. Remarque : Si elle est trop grande, le flux risque d'être derrière. |


>[!NOTE]
>
>Vous pouvez transmettre un ou plusieurs `convConfig` objets lors de l'initialisation de l'application pour afficher plusieurs applications sur la même page. Notez que les applications supplémentaires utilisent les ressources et les performances du navigateur peuvent se dégrader lorsque le nombre augmente.

## Collectionmeta Object {#c-collectionmeta-object}

`CollectionMeta` L'objet est un objet JSON qui spécifie les métadonnées à stocker dans la collection.

`CollectionMeta` est toujours codée avant d'être transmise à Livefyre pour sécurité. La valeur codée est transmise à `ConvConfig` l'objet illustré ci-dessus.

>[!NOTE]
>
>Vous devez ajouter un code côté serveur pour coder l'objet `CollectionMeta` JSON. Pour plus d'informations, voir Création de jetons côté serveur.

| Paramètre | Type | Description |
|--- |--- |--- |
| **Articleid** | *required* string | Identifiant unique de la collection. |
| **titre** | *required* string | Titre que vous souhaitez appliquer à la collection. Cela correspond souvent au titre de la page qui affiche l'application. Par exemple : « L'intégration est tellement fun !  » » Remarque : La longueur maximale du titre est de 255 caractères. Le champ title ne prend pas en charge les entités HTML. Veuillez coder des caractères spéciaux à l'aide de UTF -8. |
| **url** | *required* string | URL absolue canonique que vous souhaitez joindre à cette collection. Cette URL est utilisée pour générer des liens renvoyant à l'application depuis le contenu partagé sur Facebook et Twitter, les notifications par courrier électronique et Livefyre Studio. Remarque : Livefyre nécessite l'utilisation complète d'un nom de domaine qualifié ; le numéro de port ou un rappel pour résoudre la configuration locale n'est pas requis. Si vous testez localement, veillez à utiliser un domaine d'URL de base valide. (Par exemple : `https://customer.com` est valide, mais `https://localhost:5995` pas.) Une fois que vous avez configuré votre serveur Web local pour accepter complètement un nom de domaine qualifié, aucun rappel ni aucune résolution n'est nécessaire et le développement local peut se poursuivre comme prévu. |
| **type** | *required* String | Type Collection. Doit être livechat. |

L `CollectionMeta` 'objet peut également contenir le paramètre facultatif suivant :

| Paramètre | Type | Description |
|---|---|---|
| **balises** | *optional* string | Liste de mots-clés ou d'expressions séparés par des virgules. Rechercher des collections par balises dans Studio ou avec l'API de recherche. **Remarque :** Bien que les balises ajoutées via Studio puissent contenir des espaces, les balises saisies via l'API ne le peuvent pas. Utilisez des traits de soulignement pour définir des balises qui afficheront les espaces dans l'interface utilisateur. (Par exemple : use Monday_ Quarterback to display Monday Quarterback in Studio.) |

## Ajout d'un gestionnaire d'événements {#concept_D835C710A7214F6D921571E0770B6BC5}

Pour enregistrer les gestionnaires d'événements, utilisez l'appel widget. on au sein de la fonction de rappel de l'application.

Par exemple :

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

