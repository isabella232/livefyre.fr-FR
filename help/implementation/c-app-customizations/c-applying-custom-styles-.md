---
description: Pour créer un contenu de style personnalisé pour les groupes d'utilisateurs, vous devez d'abord ajouter une balise d'utilisateur au compte, puis mettre en forme le contenu à l'aide de CSS.
seo-description: Pour créer un contenu de style personnalisé pour les groupes d'utilisateurs, vous devez d'abord ajouter une balise d'utilisateur au compte, puis mettre en forme le contenu à l'aide de CSS.
seo-title: Application de styles personnalisés
solution: Experience Manager
title: Application de styles personnalisés
uuid: 0556 aa 2 f -4 fcd -4 bde-abb 5-479 ec 682 f 573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Application de styles personnalisés{#applying-custom-styles}

Pour créer un contenu de style personnalisé pour les groupes d&#39;utilisateurs, vous devez d&#39;abord ajouter une balise d&#39;utilisateur au compte, puis mettre en forme le contenu à l&#39;aide de CSS.

Pour chaque balise utilisateur ajoutée via Studio ou Ping pour Pull, Livefyre crée deux classes CSS, qui peuvent être utilisées pour mettre en forme le contenu du groupe.

Lors de la conversion des balises utilisateur en classes CSS :

* Livefyre crée deux classes : fyre-author-tag-*** &lt; votre_ groupe &gt;*** et fyre-tag-*** &lt; votre_ groupe &gt;***. Les deux éléments peuvent être utilisés pour mettre en forme le contenu.

* Les espaces inclus dans la balise sont convertis en traits de soulignement. Par exemple : L&#39;utilisateur favori devient favori_ utilisateur.
* Les caractères Unicode inclus dans les noms de groupes ne seront pas convertis et apparaissent sous la forme Unicode dans les noms de classe. Par exemple : Le groupe d&#39;utilisateurs&#39;modérateur&#39;devient fyre-comment-author-tag-shake ateur.

Une fois vos groupes d&#39;utilisateurs créés, utilisez les classes CSS de Livefyre pour appliquer un style personnalisé au contenu.

## Contenu de style pour les modérateurs (et les propriétaires) {#section_vjv_2cv_xz}

* Utilisez la classe CSS. fyre-modérator.

   >[!NOTE]
   >
   >Les propriétaires, étant donné qu&#39;ils sont également modérateurs, ont également cette classe appliquée à leur contenu dans le flux.

* Créez une règle CSS pour afficher ou mettre en forme un badge pour le groupe :

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Contenu de style pour les groupes d&#39;utilisateurs {#section_ghn_s1v_xz}

Créez une règle CSS pour afficher ou mettre en forme un badge pour le groupe :

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

Utilisez la classe CSS fyre-author-tag-*** &lt; votre_ groupe &gt;*** ou fyre-tag-*** &lt; votre_ groupe &gt;*** pour mettre en forme la police et l&#39;arrière-plan de chaque élément publié à partir d&#39;un compte associé à la balise sélectionnée.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

