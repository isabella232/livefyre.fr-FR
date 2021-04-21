---
description: Utilisez les classes CSS disponibles pour personnaliser l’affichage de vos applications.
title: Classes CSS
exl-id: 605f2c47-13f7-4535-90b1-c53cbf548534
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 1%

---

# Classes CSS{#css-classes}

Utilisez les classes CSS disponibles pour personnaliser l’affichage de vos applications.

Disponible pour la discussion, les commentaires, le blog en direct, les commentaires et les identifiants.

Utilisez le format CSS pour personnaliser vos applications Livefyre afin de bénéficier d’une intégration plus complète à votre page, en remplaçant simplement l’application CSS par défaut par votre propre feuille de style. Cette section décrit les personnalisations CSS disponibles.

* [Editeur CSS](#c_css_classes/section_edx_prh_xz)
* [Options de tri CSS](#c_css_classes/section_btq_4rh_xz)
* [Commenter CSS](#c_css_classes/section_mlv_nrh_xz)
* [Commentaires CSS présentés](#c_css_classes/section_m2v_mrh_xz)
* [Commentaires CSS archivés](#c_css_classes/section_bs5_lrh_xz)
* [CSS de notification de commentaires](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editeur CSS {#section_edx_prh_xz}

Utilisez ces classes pour modifier l’interface de l’éditeur de publication.

| Classe | Description |
|---|---|
| .fyre-comment-count | Texte présentant le nombre de commentaires. |
| .fyre-login-bar | Cadre de sélection contenant la barre de connexion et les options. |
| .fyre-live-conteneur | Le cadre de sélection autour du nombre de personnes qui écoutent et leurs avatars. |
| .fyre-editor | Cadre de sélection autour de la barre de connexion .fyre, .fyre-live-conteneur et de la zone de texte dans laquelle les utilisateurs écrivent leurs commentaires. |
| .fyre-stream-sort | Cadre de sélection autour des options de tri. |

Vous pouvez également modifier les styles dans la configuration de l’application elle-même, y compris la couleur d’arrière-plan du champ de l’éditeur, ainsi que la couleur, la taille et la famille de la police du texte qui s’affiche dans l’éditeur.

Pour personnaliser l’éditeur de commentaires, ajoutez l’objet editorCss:{} à fyre.conv.load() et incluez le style de votre choix. Par exemple, pour mettre à jour l’éditeur avec votre page CSS personnalisée :

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
| .fyre-stream-sort | Toutes les options de tri div. |
| .fyre-stream-sort-newest | L’option &quot;Plus récent&quot;. |
| .fyre-stream-sort-plus ancien | L’option &quot;Plus ancien&quot;. |
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

Masquez l’icône &quot;|&quot; qui sépare les options de tri.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Commenter CSS {#section_mlv_nrh_xz}

| Classe | Description |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre va créer une classe CSS dans ce format pour chaque balise d&#39;utilisateur ajoutée via Livefyre&#39;s Studio, [Profil Sync](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Cette classe peut être utilisée pour mettre en forme l’arrière-plan de tout contenu publié par les comptes d’utilisateurs, y compris cette balise. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre va créer une classe CSS dans ce format pour chaque balise de contenu ajoutée via Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Cette classe peut être utilisée pour mettre en forme tout contenu auquel vous avez ajouté la balise . |
| .fyre-comment-user | Cadre de sélection contenant l’image du profil utilisateur. |
| .fyre-comment-nom-utilisateur | Nom d’utilisateur. |
| .fyre-modérator | Cadre de sélection du modérateur. |
| .fyre-commentaire | Cadre de sélection autour du texte/lien du commentaire. |
| .fyre-commentaire-article | Cadre de sélection pour l’ensemble du contenu du commentaire. |
| .fyre-comment-date | Balise associée à l’élément &quot;Heure depuis la publication&quot;. |
| .fyre-comment-media | Cadre de sélection autour du contenu multimédia. |
| .fyre-comment-actions | Cadre de sélection entourant les actions disponibles à effectuer sur un commentaire. |
| .fyre-comment-like | Cadre de sélection autour du lien &quot;J’aime&quot;. |
| .fyre-commentaire-réponse | Cadre de sélection autour du lien &quot;Répondre&quot;. |

## Commentaires CSS présentés {#section_m2v_mrh_xz}

>[!NOTE]
>
>Toutes les classes CSS Comment peuvent également être appliquées au contenu proposé.

| Classe | Description |
|---|---|
| .fyre-featured-content-wrapper | Le conteneur div pour le lecteur. |
| .fyre-featured-header | Barre de titre en haut. |
| .fyre-featured-header-icon | Icône Quill de l’en-tête. |
| .fyre-featured-title | Texte de l’en-tête. |
| .fyre-featured-body | Div conteneur du contenu incitatif dans le lecteur. |
| .fyre-featured-quote | Icône de devis qui commence chaque élément de contenu. |

## Commentaires archivés CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>Toutes les classes CSS de contenu peuvent également être appliquées au contenu archivé.

| Classe | Description |
|---|---|
| .fyre-archive-stream-title | Texte &quot;De l&#39;archive&quot;. |
| .fyre-archive-stream-title-icon | Logo de l&#39;en-tête &quot;De l&#39;archive&quot;. |

## CSS de notification de commentaires {#section_dy4_krh_xz}

Ces classes vous permettent de personnaliser l&#39;utilitaire de notification des commentaires Livefyre.

| Classe | Description |
|---|---|
| .fyre-notification | Div pour l’élément de liste (contenu nouveau et d’archive). |
| .fyre-notifiant | Enveloppe du contenu du notificateur. |
| .fyre-notifiant-archive | wrapper pour tout nouveau contenu autre que la publication la plus récente. |
| .fyre-notifiant-avatar | Image de l’avatar. |
| .fyre-notifiant-avatar-conteneur | Div conteneur de l’avatar de l’utilisateur. Permet de définir le positionnement. |
| .fyre-notifiant-avatar-shading | L&#39;ombrage de l&#39;avatar div. |
| .fyre-notifiant-bannière | Conteneur du contenu de la prévisualisation du notificateur, qui affiche l’avatar de l’utilisateur et un extrait de contenu pour le dernier élément publié. |
| .fyre-notifiant-base | Conteneur de la partie d’informations du notificateur, qui liste le nombre de nouveaux commentaires, la légende du notificateur et le bouton de fermeture. |
| .fyre-notifiant-base-close | Div conteneur du bouton de fermeture (x) de l&#39;utilitaire de notification. |
| .fyre-notifiant-base-shadow | Ombrage de la base du notificateur. |
| .fyre-notifiant-caption | Texte affiché pour le notifiant. &quot;Nouveaux commentaires&quot; par défaut. |
| .fyre-notifiant-close | Bouton qui ferme le notifiant. |
| .fyre-notifiant-conteneur | Le conteneur de l’utilitaire de notification comprend la bannière et la base. |
| .fyre-notifiant-compteur | Conteneur du numéro indiqué dans le notificateur. |
| .fyre-notifiant-liste | Conteneur de l’élément de contenu le plus récent. |
| .fyre-notifiant-message | Les premiers ~30 caractères du contenu s’affichaient. |
| .fyre-notifiant-message-conteneur | Div conteneur du message d’en-tête. |
