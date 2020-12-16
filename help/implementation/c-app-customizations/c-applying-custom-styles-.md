---
description: Pour personnaliser le contenu des groupes d’utilisateurs, vous devez d’abord ajouter une balise d’utilisateur au compte, puis mettre en forme le contenu à l’aide de CSS.
seo-description: Pour personnaliser le contenu des groupes d’utilisateurs, vous devez d’abord ajouter une balise d’utilisateur au compte, puis mettre en forme le contenu à l’aide de CSS.
seo-title: Application de styles personnalisés
solution: Experience Manager
title: Application de styles personnalisés
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# Application de styles personnalisés {#applying-custom-styles}

Pour personnaliser le contenu des groupes d’utilisateurs, vous devez d’abord ajouter une balise d’utilisateur au compte, puis mettre en forme le contenu à l’aide de CSS.

Pour chaque balise d’utilisateur ajoutée via Studio ou Ping for Pull, Livefyre crée deux classes CSS, qui peuvent toutes deux être utilisées pour mettre en forme le contenu du groupe.

Lors de la conversion des balises d’utilisateur en classes CSS :

* Livefyre crée deux classes : fyre-author-tag-***&lt;votre_groupe>*** et fyre-tag-author-****&lt;votre_groupe>***. Les deux peuvent être utilisés pour mettre en forme le contenu.

* Les espaces inclus dans la balise sont convertis en traits de soulignement. Par exemple : &quot;Utilisateur favori&quot; devient utilisateur favori.
* Les caractères Unicode inclus dans les noms de groupe ne seront pas convertis et apparaîtront sous forme Unicode dans les noms de classe. Par exemple : Le groupe d&#39;utilisateurs &quot;modérateur&quot; deviendra fyre-comment-author-tag-modéateur.

Une fois vos groupes d’utilisateurs créés, utilisez les classes CSS de Livefyre pour appliquer un style personnalisé au contenu.

## Contenu du style pour les modérateurs (et les propriétaires) {#section_vjv_2cv_xz}

* Utilisez la classe CSS .fyre-modérator.

   >[!NOTE]
   >
   >Les propriétaires, puisqu’ils sont également modérateurs, verront cette classe appliquée à leur contenu dans le flux également.

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

## Contenu du style pour les groupes d’utilisateurs {#section_ghn_s1v_xz}

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

Utilisez la classe CSS fyre-author-tag-***&lt;votre_groupe>*** ou fyre-tag-author-****&lt;votre_groupe>*** pour mettre en forme la police et l’arrière-plan de chaque élément publié à partir d’un compte associé à la balise sélectionnée.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

