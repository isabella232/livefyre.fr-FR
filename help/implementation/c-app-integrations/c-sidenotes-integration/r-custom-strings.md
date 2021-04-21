---
title: Sidenotes Chaînes personnalisées
description: Sidenotes Chaînes personnalisées
exl-id: b5e2c18b-5b98-45ff-aa89-dd92a02949a9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 10%

---

# Sidenotes Chaînes personnalisées{#sidenotes-custom-strings}

Les chaînes personnalisées sont appliquées via un objet injecté dans le constructeur Sidenotes et remplacent les chaînes par défaut utilisées dans l’application. Ils peuvent être utilisés pour personnaliser n’importe quelle partie de la langue en fonction de vos spécifications de style ou de langue. Les chaînes fusionnent automatiquement avec les valeurs par défaut.

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
| commentReplyLink | Voir {number} réponses |
| commentReplyLinkSing | Voir réponse |
| commentVoteCount | votes |
| commentVoteCountSing | vote |
| editorPlaceholder | Que penses-tu ? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Publication |
| editorPosting | Publication… |
| editorReplyBtn | Poster une réponse |
| editorReplyTitle | Répondre en écriture |
| editorTitle | Note d&#39;écriture |
| emptyImageBlockTxt | Que penses-tu ? |
| emptyTextBlockTxt | + |
| errorConnection | Oh oh. Vous ne semblez pas avoir une bonne connexion. |
| errorDuplicate | Votre note nous plaît aussi, mais vous ne pouvez pas la poster deux fois. |
| errorGeneral | Une erreur s&#39;est produite. Veuillez réessayer. |
| errorServer | Quelque chose s&#39;est mal passé avec notre serveur. Essaie encore ça ? |
| facebookShareCaption | SideNotes sur &quot;{title}&quot; |
| menuAuthSignedInMsg | Vous devez être connecté à {action} |
| menuAuthSignInBtn | Se connecter |
| menuBackBtn | Retour |
| menuConfirmAccept | Oui, {action} |
| menuConfirmCancel | Annuler |
| menuConfirmTitle | Etes-vous sûr ? |
| menuEtcOptionApprouver | Approuver |
| menuOptionOptionSupprimer | Supprimer |
| menuOptionEdition | Modifier      |
| menuOptionFlag | Marquer d’un indicateur |
| menuEtcOptionShare | Partager |
| menuEtcPostedAt | Publié le {date} |
| menuEtcTitle | Plus |
| menuFlagOptionDésaccord | Désaccord |
| menuFlagOptionOffensive | Offensive |
| menuFlagOptionOffTopic | Désactivé la rubrique |
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
| questionExplication | Vous pouvez maintenant lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets.<br><br>Mettez le texte en surbrillance et cliquez sur l’icône &quot;fycon-write&quot; ou cliquez sur l’icône &quot;fycon-action-vue&quot; à la fin de chaque paragraphe. |
| questionMockText | Ce qui est &quot;familiairement connu&quot; n&#39;est pas correctement connu, juste pour la raison qu&#39;il est &quot;familier&quot;. |
| questionTitle | Qu&#39;est-ce qu&#39;une Sidenote ? |
| file d&#39;attenteCommentairesPlural | {number} Nouveaux identifiants |
| queuedCommentsSingular | 1 nouveau logo |
| file d&#39;attenteRéponsesPlural | {number} Nouvelles réponses |
| file d&#39;attenteRéponsesSingular | 1 Nouvelle réponse |
| responseBtn | Répondre |
| signInToPost | Se connecter pour écrire une note de connexion |
| sliderCommentTally | of |
| sliderInviteRead | Lu |
| sliderInviteWrite | Écriture |
| sliderWriteText | Que penses-tu ? Appuyez pour écrire |
| threadCollapseBtn | Condenser |
| threadExpandBtnPlural | Développer les réponses {number} |
| threadExpandBtnSingular | Développer 1 réponse |
| threadReplyBtn | Réponse à la conversation |
