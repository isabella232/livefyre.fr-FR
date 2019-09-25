---
description: valeur nulle
seo-description: valeur nulle
seo-title: Sidenotes Chaînes personnalisées
title: Sidenotes Chaînes personnalisées
uuid: 73745273-d3fb-4569-8910-d149fb37a7b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Sidenotes Chaînes personnalisées{#sidenotes-custom-strings}

Les chaînes personnalisées sont appliquées via un objet injecté dans le constructeur Sidenotes et remplacent les chaînes par défaut utilisées dans l’application. Elles peuvent être utilisées pour personnaliser n’importe quelle partie de la langue en fonction de votre style ou de vos spécifications linguistiques. Les chaînes fusionnent automatiquement avec les valeurs par défaut.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Clé | Par défaut |
|---|---|
| appName | Sidenotes |
| commentModeratorTag | Mod |
| commentPendingTag | En attente |
| commentReadMoreLink | En savoir plus |
| commentReplyLink | Voir {nombre} réponses |
| commentReplyLinkSing | Voir réponse |
| commentVoteCount | votes |
| commentVoteCountSing | vote |
| editorPlaceholder | Que penses-tu ? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Publication |
| editorPosting | Publication… |
| editorReplyBtn | Poster une réponse |
| editorReplyTitle | Répondre en écriture |
| editorTitle | Note d'écriture |
| emptyImageBlockTxt | Que penses-tu ? |
| emptyTextBlockTxt | + |
| errorConnection | Oh oh. Vous ne semblez pas avoir une bonne connexion. |
| errorDuplicate | Nous aimons votre note aussi, mais vous ne pouvez pas la poster deux fois. |
| errorGeneral | Une erreur s'est produite. Veuillez réessayer. |
| errorServer | Quelque chose a mal tourné avec notre serveur. Essaie encore ça ? |
| facebookShareCaption | SideNotes sur "{title}" |
| menuAuthSignedInMsg | Vous devez vous connecter à {action} |
| menuAuthSignInBtn | Se connecter |
| menuBackBtn | Retour |
| menuConfirmAccept | Oui, {action} |
| menuConfirmCancel | Annuler |
| menuConfirmTitle | Etes-vous sûr ? |
| menuEtcOptionApprouver | Approuver |
| menuEtcOptionDelete | Supprimer |
| menuEtcOptionEdit | Modifier      |
| menuEtcOptionFlag | Marquer d’un indicateur |
| menuEtcOptionShare | Partager |
| menuEtcPostedAt | Publié le {date} |
| menuEtcTitle | Plus |
| menuFlagOptionDésaccord | Désapprouver |
| menuFlagOptionOffensive | Offensive |
| menuFlagOptionOffTopic | Hors rubrique |
| menuFlagOptionSpam | Indésirables |
| menuFlagTitle | Marquer comme... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Aide |
| menuInfoLivefyreLink | Visitez Livefyre.com |
| menuRéponsesViewReply | Réponse à la conversation |
| menuRéponsesAfficherTitre | Détails |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copier le lien permanent |
| menuShareOptionLinkComplete | Copié |
| menuShareOptionLinkFailed | Échec de la copie |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Partager |
| notificationApprouvé | Approuvés |
| notificationDeleted | Supprimé |
| notificationFlagged | Avec indicateur |
| permalinkBackBtn | Toutes |
| permalinkTitle | Permalink |
| questionExplication | Vous pouvez maintenant lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets.<br><br>Mettez le texte en surbrillance et cliquez sur l’icône "fycon-write" ou cliquez sur l’icône "fycon-action-view" à la fin de chaque paragraphe. |
| questionMockText | Ce qui est "familiairement connu" n'est pas correctement connu, juste pour la raison qu'il est "familier". |
| questionTitle | Qu'est-ce qu'une Sidenote ? |
| file d’attenteCommentairesPlural | {number} Nouveaux Sidenotes |
| queueCommentsSingular | 1 Nouveau Sidenote |
| file d'attenteRéponsesPlural | {number} nouvelles réponses |
| queuedRepliesSingular | 1 Nouvelle réponse |
| responseBtn | Répondre |
| signInToPost | Connectez-vous pour écrire une note de connexion |
| sliderCommentTally | of |
| sliderInviteRead | Lu |
| sliderInviteWrite | Écriture |
| sliderWriteText | Que penses-tu ? Appuyez pour écrire |
| threadCollapseBtn | Condenser |
| threadExpandBtnPlural | Développer les réponses {number} |
| threadExpandBtnSingular | Développer 1 réponse |
| threadReplyBtn | Réponse à la conversation |
