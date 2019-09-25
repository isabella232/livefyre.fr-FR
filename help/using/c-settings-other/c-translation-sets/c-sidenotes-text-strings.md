---
description: Personnalisation des chaînes de texte pour les Sidenotes Livefyre
seo-description: Personnalisation des chaînes de texte pour les Sidenotes Livefyre
seo-title: Sidenotes chaînes de texte
solution: Experience Manager
title: Sidenotes chaînes de texte
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Sidenotes chaînes de texte{#sidenotes-text-strings}

Personnalisation des chaînes de texte pour les Sidenotes Livefyre

Cette page répertorie et décrit toutes les chaînes disponibles pour la personnalisation dans les applications Sidenotes. Pour plus d’informations sur les chaînes disponibles pour les principales applications Livefyre, voir Personnalisations des chaînes.

ImplémentationAuthStream InfoAuteur / Informations sur le contenu Actions de l'utilisateurFonctions de publicationInterfaceModérateurErreurs

## Implémentation {#section_wp2_ql4_xz}

Pour implémenter cette fonctionnalité, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration Javascript. Si vous ne fournissez pas de champ, le texte par défaut sera utilisé.

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

Chaînes disponibles pour le processus d’authentification et dans les menus des utilisateurs authentifiés.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Chaînes du menu Auth | menuAuthSignInBtn | Se connecter |
|  | menuAuthSignedInMsg | Vous devez vous connecter à {action} |
|  | menuUserEditProfile | Modifier le profil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Se déconnecter |
|  | menuUserBackBtn | Toutes |

## Informations sur le flux {#section_wpy_gl4_xz}

Chaînes disponibles pour l’affichage et l’information du flux de contenu.

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
|  | commentReplyLink | Voir {nombre} réponses |
|  | commentReplyLinkSing | Voir réponse |
|  | commentVoteCount | votes |
|  | commentVoteCountSing | vote |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | Un tableau. Par défaut =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplication | Vous pouvez maintenant lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Mettez le texte</span> en surbrillance et cliquez sur l’ <span class="&rdquo;fycon-write&rdquo;"></span> icône ou cliquez sur l’ <span class="&rdquo;fycon-action-view&rdquo;"></span> icône à la fin de chaque paragraphe. |
|  | questionMockText | Ce qui est "familiairement connu" n'est pas correctement connu, juste pour la raison qu'il est "familier". |
|  | questionTitle | Qu'est-ce qu'une Sidenote ? |

## Actions de l’utilisateur {#section_qxd_fl4_xz}

Chaînes disponibles pour les actions utilisateur : marquage, partage et mention J’aime du contenu existant.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Options du menu Répondre | menuRéponsesAfficherTitre | Détails |
|  | menuRéponsesViewReply | Réponse à la conversation |
| Options du menu Partager | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Partager |
| Options du menu Indicateur | menuFlagOptionDésaccord | Désapprouver |
|  | menuFlagOptionOffensive | Offensive |
|  | menuFlagOptionOffTopic | Hors rubrique |
|  | menuFlagOptionSpam | Indésirables |
|  | menuFlagTitle | Marquer comme... |
|  | facebookShareCaption | Sidenotes sur "{title}" |
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
|  | editorEditPosting | Enregistrement... |
|  | editorEditReplyTitle | Modifier la réponse |
|  | editorEditTitle | Modifier le logo |
|  | editorPlaceholder | Que penses-tu ? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Publication |
|  | editorPosting | Publication… |
|  | editorReplyBtn | Poster une réponse |
|  | editorReplyTitle | Répondre en écriture |
|  | editorTitle | Écrire Sidenote |
|  | emptyImageBlockTxt | Que penses-tu ? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Répondre |
|  | threadReplyBtn | Réponse à la conversation |
| Supprimer les options du menu | menuConfirmAccept | Oui, {action} |
|  | menuConfirmCancel | Annuler |
|  | menuConfirmTitle | Etes-vous sûr ? |
| Options du menu Etc | menuEtcOptionApprouver | Approuver |
|  | menuEtcOptionDelete | Supprimer |
|  | menuEtcOptionEdit | Modifier      |
|  | menuEtcOptionFlag | Marquer d’un indicateur |
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
|  | errorDuplicate | Nous aimons votre note aussi, mais vous ne pouvez pas la poster deux fois. |
|  | errorGeneral | Une erreur s'est produite. Veuillez réessayer. |
|  | errorServer | Quelque chose a mal tourné avec notre serveur. Essaie encore ça ? |

