---
description: Utilisez les classes CSS disponibles pour personnaliser l'affichage de vos applications.
seo-description: Utilisez les classes CSS disponibles pour personnaliser l'affichage de vos applications.
seo-title: Classes CSS
solution: Experience Manager
title: Classes CSS
uuid: 8714 e 7 e 5-3858-458 f-a 464-de 87 fd 2 f 0 ff 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Classes CSS{#css-classes}

Utilisez les classes CSS disponibles pour personnaliser l&#39;affichage de vos applications.

Disponible pour la messagerie instantanée, les commentaires, le blog en direct, les révisions et les tableaux de sidenom.

Utilisez CSS pour personnaliser vos applications Livefyre pour une intégration plus complète à votre page, en remplaçant simplement le CSS d&#39;application par défaut par votre propre feuille de style. Cette section décrit les personnalisations CSS disponibles.

* [Editeur CSS](#c_css_classes/section_edx_prh_xz)
* [Options de tri CSS](#c_css_classes/section_btq_4rh_xz)
* [Commentaires CSS](#c_css_classes/section_mlv_nrh_xz)
* [CSS Commentaires présentés](#c_css_classes/section_m2v_mrh_xz)
* [CSS de commentaires archivés](#c_css_classes/section_bs5_lrh_xz)
* [CSS Notification CSS](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editeur CSS {#section_edx_prh_xz}

Utilisez ces classes pour modifier l&#39;interface de l&#39;éditeur de publication.

| Classe | Description |
|---|---|
| . fyre-comment-count | Texte affichant le nombre de commentaires. |
| . fyre-login-bar | Cadre de sélection contenant la barre de connexion et les options. |
| . fyre-live-container | Cadre de sélection autour du nombre de personnes écoutant et de leurs avatars. |
| . fyre-editor | Cadre de sélection autour de. fyre-login-bar. fyre-live-container et zone de texte où les utilisateurs consignent leurs commentaires. |
| . fyre-stream-sort | Cadre de sélection autour des options de tri. |

Vous pouvez également modifier les styles dans la configuration de l&#39;application, y compris la couleur d&#39;arrière-plan du champ de l&#39;éditeur, ainsi que la couleur, la taille et la famille de la police du texte qui s&#39;affiche dans l&#39;éditeur.

Pour personnaliser l&#39;éditeur de commentaires, ajoutez le fichier editorcss : {} objet à fyre. conv. load () et incluez le style souhaité. Par exemple, pour mettre à jour l&#39;éditeur avec votre CSS personnalisée :

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## Options de tri CSS {#section_btq_4rh_xz}

| Classe | Description |
|---|---|
| . fyre-stream-sort | La totalité des options de tri div. |
| . fyre-stream-sort-newest | L&#39;option « Plus récent ». |
| . fyre-stream-sort-le | L&#39;option « Le plus ancien ». |
| . fyre-stream-bar-bar | Barre séparatrice entre les options. |
| . fyre-stream-selected-selected | Option de tri sélectionnée. |

Structure HTML :

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Masquer le|&#39; séparant les options de tri.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Commentaires CSS {#section_mlv_nrh_xz}

| Classe | Description |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | Livefyre crée une classe CSS dans ce format pour chaque balise utilisateur ajoutée via le studio Livefyre&#39;s Studio, [la synchronisation des profils](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Cette classe peut être utilisée pour mettre en forme l&#39;arrière-plan de tout contenu publié par des comptes utilisateur, y compris cette balise. |
| . fyre-tag-content-icon- *`tag name`* | Livefyre crée une classe CSS dans ce format pour chaque balise de contenu ajoutée via Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Cette classe peut être utilisée pour mettre en forme tout contenu auquel vous avez ajouté la balise. |
| . fyre-comment-user | Cadre de sélection contenant la photo du profil utilisateur. |
| . fyre-comment-username | Nom d&#39;utilisateur. |
| . fyre-modérator | Cadre de sélection du modérateur. |
| . fyre-comment | Cadre de sélection autour du texte/lien du commentaire. |
| . fyre-comment-article | Cadre de sélection pour tout le contenu du commentaire. |
| . fyre-comment-date | Balise associée à l&#39;élément « time since publié ». |
| . fyre-comment-media | Cadre de sélection autour du contenu multimédia. |
| . fyre-comments-actions | Cadre de sélection autour des actions disponibles pour prendre un commentaire. |
| . fyre-comment-like | Cadre de sélection autour du lien « J&#39;aime ». |
| . fyre-comment-reply | Cadre de sélection autour du lien « Répondre ». |

## CSS Commentaires présentés {#section_m2v_mrh_xz}

>[!NOTE]
>
>Toutes les classes de commentaires CSS peuvent également être appliquées au contenu incitatif.

| Classe | Description |
|---|---|
| . fyre-incitatif-content-wrapper | Balise div de conteneur pour le lecteur. |
| . fyre-feature-header | Barre de titre de début. |
| . fyre-feature-header-icon | Icône en forme de quill de l&#39;en-tête. |
| . fyre-feature-title | Texte d&#39;en-tête. |
| . fyre-feature-body | Balise div du conteneur pour le contenu phare dans le lecteur. |
| devis-devis | Icône de guillemets qui commence chaque élément de contenu. |

## CSS de commentaires archivés {#section_bs5_lrh_xz}

>[!NOTE]
>
>Toutes les classes CSS de contenu peuvent également être appliquées au contenu archivé.

| Classe | Description |
|---|---|
| . fyre-archive-stream-title | Le texte « À partir de l&#39;archive ». |
| . fyre-archive-stream-title-icon | Logo de l&#39;en-tête « Dans l&#39;archive ». |

## CSS Notification CSS {#section_dy4_krh_xz}

Ces classes vous permettent de personnaliser le notification de commentaire Livefyre.

| Classe | Description |
|---|---|
| . fyre-notification | Balise div de l&#39;élément de liste (nouveau contenu d&#39;archive et d&#39;archivage). |
| . fyre-notification | Enveloppe pour le contenu du notificateur. |
| . fyre-notification-archive | wrapper pour tout nouveau contenu autre que la publication la plus récente. |
| . fyre-notification-avatar | Image de l&#39;avatar. |
| . fyre-notification-avatar-container | Balise div de conteneur pour l&#39;avatar de l&#39;utilisateur. Permet de définir le positionnement. |
| . fyre-notification-avatar-shading | Ombrage de la balise div de l&#39;avatar. |
| . fyre-notification-banner | Conteneur pour le contenu d&#39;aperçu de la notification, qui affiche l&#39;avatar de l&#39;utilisateur et un extrait de contenu pour l&#39;article publié le plus récemment. |
| . fyre-notification-base | Conteneur pour la partie Informations de la notification, qui répertorie le nombre de nouveaux commentaires, la légende de notification et le bouton de fermeture. |
| . fyre-notification-base-close | Balise div du conteneur pour le bouton de fermeture (x) pour le notificateur. |
| . fyre-notification-base-shadow | Ombrage de la base Notifier. |
| . fyre-notification-caption | Texte affiché pour le notificateur. &#39; Nouveaux commentaires&#39;par défaut. |
| . fyre-notification-close | Bouton qui ferme le notificateur. |
| . fyre-notification-container | Le conteneur pour le notificateur comprend la bannière et la base. |
| . fyre-notification-counter | Conteneur pour le nombre répertorié dans le notificateur. |
| . fyre-notification-list | Conteneur pour l&#39;élément de contenu le plus récent. |
| . fyre-notification-message | Premier ~ 30 caractères du contenu affiché. |
| . fyre-notification-message-container | Balise div du conteneur pour le message d&#39;en-tête. |
