---
description: Personnalisation des chaînes de texte pour les Sidenotes Livefyre
seo-description: Personnalisation des chaînes de texte pour les Sidenotes Livefyre
seo-title: Sidentifie les chaînes de texte
solution: Experience Manager
title: Sidentifie les chaînes de texte
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 12%

---


# Sidentifie les chaînes de texte{#sidenotes-text-strings}

Personnalisation des chaînes de texte pour les Sidenotes Livefyre

Cette page liste et décrit toutes les chaînes disponibles pour la personnalisation dans les applications Sidenotes. Pour plus d’informations sur les chaînes disponibles pour les principales applications Livefyre, voir Personnalisations des chaînes.

Implémentation
Auth
Informations sur le flux
Auteur / Informations sur le contenu
Actions de l’utilisateur
Fonctions de publication
Interface du modérateur
Erreurs

## Implémentation {#section_wp2_ql4_xz}

Pour mettre en oeuvre cette fonctionnalité, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration JavaScript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

Exemple :

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Authentification {#section_pqf_3l4_xz}

Chaînes disponibles pour le processus d’authentification et à partir des menus des utilisateurs authentifiés.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Chaînes de menu Auth | menuAuthSignInBtn | Se connecter |
|  | menuAuthSignedInMsg | Vous devez être connecté à {action} |
|  | menuUserEditProfile | Modifier le profil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Se déconnecter |
|  | menuUserBackBtn | Toutes |

## Informations sur le flux {#section_wpy_gl4_xz}

Chaînes disponibles pour l’affichage et les informations du flux de contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Options du menu Infos | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Aide |
|  | menuInfoLivefyreLink | Visitez Livefyre.com |

## Auteur / Informations sur le contenu {#section_dhb_gl4_xz}

Paramètres disponibles pour les informations sur l’auteur et le contenu individuel.

| Élément | Clé | Texte par défaut |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | En attente |
|  | commentReadMoreLink | En savoir plus |
|  | commentReplyLink | Voir {number} réponses |
|  | commentReplyLinkSing | Voir réponse |
|  | commentVoteCount | votes |
|  | commentVoteCountSing | vote |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | Un tableau. Par défaut =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplication | Vous pouvez maintenant lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Mettez le </span> texte en surbrillance et cliquez sur l’ <span class="&rdquo;fycon-write&rdquo;"></span> icône ou cliquez sur l’ <span class="&rdquo;fycon-action-view&rdquo;"></span> icône à la fin de chaque paragraphe. |
|  | questionMockText | Ce qui est &quot;familiairement connu&quot; n&#39;est pas correctement connu, juste pour la raison qu&#39;il est &quot;familier&quot;. |
|  | questionTitle | Qu&#39;est-ce qu&#39;une Sidenote ? |

## Actions de l&#39;utilisateur {#section_qxd_fl4_xz}

Chaînes disponibles pour les actions de l’utilisateur : marquage, partage et mention &quot;J’aime&quot; du contenu existant.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Options du menu Répondre | menuRéponsesAfficherTitre | Détails |
|  | menuRéponsesViewReply | Réponse à la conversation |
| Options du menu Partager | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Partager |
| Options du menu Indicateur | menuFlagOptionDésaccord | Désaccord |
|  | menuFlagOptionOffensive | Offensive |
|  | menuFlagOptionOffTopic | Désactivé la rubrique |
|  | menuFlagOptionSpam | Indésirables |
|  | menuFlagTitle | Marquer comme... |
|  | facebookShareCaption | Identifications sur &quot;{title}&quot; |
| Options utilisateur mobiles | sliderCommentTally | of |
|  | sliderInviteRead | Lu |
|  | sliderInviteWrite | Écriture |
|  | sliderLoading | Chargement en cours… |
|  | sliderWriteText | Que penses-tu ? Appuyez pour écrire. |

## Fonctions de publication {#section_xzf_2l4_xz}

Chaînes disponibles pour les utilisateurs qui publient du contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
|  | editorEditBtn | Enregistrer |
|  | editorEditPosting | Enregistrement en cours... |
|  | editorEditReplyTitle | Modifier la réponse |
|  | editorEditTitle | Modifier le logo |
|  | editorPlaceholder | Que penses-tu ? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Publication |
|  | editorPosting | Publication… |
|  | editorReplyBtn | Poster une réponse |
|  | editorReplyTitle | Répondre en écriture |
|  | editorTitle | Écrire une identité |
|  | emptyImageBlockTxt | Que penses-tu ? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Répondre |
|  | threadReplyBtn | Réponse à la conversation |
| Supprimer les options du menu | menuConfirmAccept | Oui, {action} |
|  | menuConfirmCancel | Annuler |
|  | menuConfirmTitle | Etes-vous sûr ? |
| Options du menu Etc | menuEtcOptionApprouver | Approuver |
|  | menuOptionOptionSupprimer | Supprimer |
|  | menuOptionEdition | Modifier      |
|  | menuOptionFlag | Marquer d’un indicateur |
|  | menuEtcOptionShare | Partager |
|  | menuEtcPostedAt | Publié le {date} |
|  | menuEtcTitle | Plus |

## Interface du modérateur {#section_o5f_dl4_xz}

Chaînes disponibles pour l’interface du modérateur authentifié par l’utilisateur.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Messages de confirmation du menu Plus | notificationApprouvé | Approuvés |
|  | notificationDeleted | Supprimé |
|  | notificationFlagged | Avec indicateur |

## Erreurs {#section_gtk_cl4_xz}

Chaînes disponibles pour les messages d’erreur généraux.

| Élément | Clé | Texte par défaut |
|---|---|---|
|  | errorConnection | Oh oh. Vous ne semblez pas avoir une bonne connexion. |
|  | errorDuplicate | Votre note nous plaît aussi, mais vous ne pouvez pas la poster deux fois. |
|  | errorGeneral | Une erreur s&#39;est produite. Veuillez réessayer. |
|  | errorServer | Quelque chose s&#39;est mal passé avec notre serveur. Essaie encore ça ? |

