---
description: Utilisez les classes CSS disponibles pour personnaliser l’affichage de vos applications.
seo-description: Utilisez les classes CSS disponibles pour personnaliser l’affichage de vos applications.
seo-title: Classes CSS
solution: Experience Manager
title: Classes CSS
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Classes CSS{#css-classes}

Utilisez les classes CSS disponibles pour personnaliser l’affichage de vos applications.

Disponible pour la messagerie instantanée, les commentaires, le blog en direct, les commentaires et les mentions.

Utilisez CSS pour personnaliser vos applications Livefyre afin d’une intégration plus complète à votre page, en remplaçant simplement la page CSS par défaut par votre propre feuille de style. Cette section décrit les personnalisations CSS disponibles.

* [CSS de l’éditeur](#c_css_classes/section_edx_prh_xz)
* [Options de tri CSS](#c_css_classes/section_btq_4rh_xz)
* [Commenter CSS](#c_css_classes/section_mlv_nrh_xz)
* [CSS des commentaires proposés](#c_css_classes/section_m2v_mrh_xz)
* [CSS des commentaires archivés](#c_css_classes/section_bs5_lrh_xz)
* [CSS du notifications de commentaires](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## CSS de l’éditeur {#section_edx_prh_xz}

Utilisez ces classes pour modifier l’interface de l’éditeur de publication.

| Classe | Description |
|---|---|
| .fyre-comment-count | Texte affichant le nombre de commentaires. |
| .fyre-login-bar | Cadre de sélection contenant la barre de connexion et les options. |
| .fyre-live-container | Le cadre de sélection autour du nombre de personnes qui écoutent et de leurs avatars. |
| .fyre-editor | Le cadre de sélection autour de la barre de connexion .fyre, .fyre-live-container et la zone de texte dans laquelle les utilisateurs écrivent leurs commentaires. |
| .fyre-stream-sort | Cadre de sélection autour des options de tri. |

Vous pouvez également modifier les styles dans la configuration de l’application elle-même, y compris la couleur d’arrière-plan du champ de l’éditeur, ainsi que la couleur, la taille et la famille de la police du texte qui apparaît dans l’éditeur.

Pour personnaliser l’éditeur de commentaires, ajoutez l’objet editorCss:{} à fyre.conv.load() et incluez le style souhaité. Par exemple, pour mettre à jour l’éditeur avec votre page CSS personnalisée :

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
| .fyre-stream-sort | L'ensemble des options de tri div. |
| .fyre-stream-sort-newest | L’option "Plus récent". |
| .fyre-stream-sort-plus ancien | L’option "Plus ancien". |
| .fyre-stream-sort-bar | Barre de séparation entre les options. |
| .fyre-stream-sort-selected | Option de tri actuellement sélectionnée. |

Structure HTML :

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Masquez l’icône "|" qui sépare les options de tri.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Commenter CSS {#section_mlv_nrh_xz}

| Classe | Description |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre crée une classe CSS dans ce format pour chaque balise utilisateur ajoutée par le biais de Livefyre Studio, [Profile Sync](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Cette classe peut être utilisée pour mettre en forme l’arrière-plan de tout contenu publié par les comptes d’utilisateurs, y compris cette balise. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre crée une classe CSS dans ce format pour chaque balise de contenu ajoutée via Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Cette classe peut être utilisée pour mettre en forme tout contenu auquel vous avez ajouté la balise . |
| .fyre-comment-user | Cadre de sélection contenant l’image du profil utilisateur. |
| .fyre-comment-nom-utilisateur | Nom d’utilisateur. |
| .fyre-modérateur | Cadre de sélection du modérateur. |
| .fyre-comment | Cadre de sélection autour du texte/lien du commentaire. |
| .fyre-comment-article | Cadre de sélection pour l’ensemble du contenu du commentaire. |
| .fyre-comment-date | Balise jointe à l’élément "Heure depuis la publication". |
| .fyre-comment-media | Cadre de sélection autour du contenu multimédia. |
| .fyre-comment-actions | Cadre de sélection autour des actions disponibles pour effectuer un commentaire. |
| .fyre-comment | Cadre de sélection autour du lien "J’aime". |
| .fyre-commentaire-réponse | Cadre de sélection autour du lien "Répondre". |

## CSS des commentaires proposés {#section_m2v_mrh_xz}

>[!NOTE]
>
>Toutes les classes CSS de commentaires peuvent également être appliquées au contenu proposé.

| Classe | Description |
|---|---|
| .fyre-featured-content-wrapper | Conteneur div pour le lecteur. |
| .fyre-featured-header | Barre de titre en haut. |
| .fyre-featured-header-icon | Icône de l’en-tête composée. |
| .fyre-featured-title | Texte de l’en-tête. |
| .fyre-featured-body | Div de conteneur pour le contenu incitatif dans le lecteur. |
| .fyre-featured-quote | Icône de devis qui commence chaque élément de contenu. |

## CSS des commentaires archivés {#section_bs5_lrh_xz}

>[!NOTE]
>
>Toutes les classes CSS de contenu peuvent également être appliquées au contenu archivé.

| Classe | Description |
|---|---|
| .fyre-archive-stream-title | Texte "De l'archive". |
| .fyre-archive-stream-title-icon | Le logo de l'en-tête "De l'archive". |

## CSS du notifications de commentaires {#section_dy4_krh_xz}

Ces classes vous permettent de personnaliser l’utilitaire de notification des commentaires Livefyre.

| Classe | Description |
|---|---|
| .fyre-notification | La balise div de l’élément de liste (nouveau contenu et contenu d’archive). |
| .fyre-notifiant | wrapper pour le contenu du notificateur. |
| .fyre-notifiant-archive | wrapper pour tout nouveau contenu autre que la publication la plus récente. |
| .fyre-notifiant-avatar | Image de l’avatar. |
| .fyre-notifiant-avatar-container | Conteneur div pour l’avatar de l’utilisateur. Permet de définir le positionnement. |
| .fyre-notifiant-avatar-shading | L'ombrage de l'avatar div. |
| .fyre-notifiant-bannière | Conteneur du contenu d’aperçu du notificateur, qui affiche l’avatar de l’utilisateur et un extrait de contenu pour le dernier élément publié. |
| .fyre-notifiant-base | Conteneur de la partie information du notificateur, qui répertorie le nombre de nouveaux commentaires, la légende du notificateur et le bouton de fermeture. |
| .fyre-notifiant-base-close | Conteneur div pour le bouton de fermeture (x) pour le notificateur. |
| .fyre-notifiant-base-shadow | Ombrage de la base du notificateur. |
| .fyre-notifier-caption | Texte affiché pour le notifiant. "Nouveaux commentaires" par défaut. |
| .fyre-notifiant-close | Bouton qui ferme le notifiant. |
| .fyre-notifiant-conteneur | Le conteneur de l’utilitaire de notification comprend la bannière et la base. |
| .fyre-notifiant-compteur | Conteneur correspondant au nombre indiqué dans le notificateur. |
| .fyre-notifiant-liste | Conteneur de l’élément de contenu le plus récent. |
| .fyre-notifiant-message | Les 30 premiers caractères du contenu s’affichaient. |
| .fyre-notifiant-message-conteneur | Conteneur div pour le message d’en-tête. |
