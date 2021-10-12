---
description: Les jeux de traduction vous permettent de spécifier une autre langue pour les applications.
title: Jeux de traduction
exl-id: 688138bf-f8e9-4fe5-99e2-2451deefd217
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 7%

---

# Jeux de traduction {#translation-sets}

Les jeux de traduction vous permettent de spécifier une autre langue pour les applications.

Utilisez les paramètres de traduction pour localiser les applications dans différentes langues ou pour spécifier un texte de remplacement pour plusieurs applications à partir d’un emplacement dans Studio. Par exemple, vous pouvez vous assurer que tous les sites en espagnol utilisent l’espagnol pour tous les champs de l’application. Vous pouvez également modifier le texte de sorte que tous les champs correspondent à la voix et à l’aspect de votre site ou réseau.

Vous pouvez spécifier les paramètres de traduction pour toutes les applications, à l’exception de Storify 2. Pour plus d’informations sur les champs que vous pouvez localiser, voir [Localisation des chaînes](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Comments, Live Blog et Chat partagent le même ensemble de chaînes au sein d’un ensemble de traductions.

Spécifiez un jeu de traduction pour un réseau, un site, une application ou à l’aide d’une API.

Les jeux de traduction à différents niveaux se chevauchent en suivant ce modèle :

* La visionneuse de traduction d’API remplace les visionneuses de traduction à n’importe quel niveau (application, réseau et site).
* Le jeu de traduction d’application remplace les jeux de traduction au niveau du réseau et au niveau du site.
* Les ensembles de traduction au niveau du site remplacent les ensembles de traduction au niveau du réseau.

## Vérifier les chaînes de texte {#c-review-text-strings}

Personnalisation des chaînes de texte pour les révisions Livefyre.

Cette page répertorie et décrit les chaînes disponibles pour la personnalisation dans les applications de révision. Les chaînes répertoriées ici s’ajoutent aux chaînes par défaut des applications de base Livefyre et les remplacent, répertoriées dans Personnalisations des chaînes. Lorsque des doublons sont répertoriés, les chaînes répertoriées dans ces tableaux sont la valeur par défaut des applications Reviews.

* Mise en œuvre
* Interface de révision/notation
* Informations sur la diffusion
* Création/Informations sur le contenu
* Actions des utilisateurs
* Fonctions de publication
* Erreurs

## Mise en œuvre {#section-vsy-1k4-xz}

Pour mettre en oeuvre cette fonction, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration JavaScript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

Exemple :

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Interface de révision/notation {#section_iyv_zj4_xz}

Chaînes disponibles pour l’interface utilisateur de révision et d’évaluation.

| Élément | Clé | Texte par défaut |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Boutons |  |  |
|  | editReviewBtn | Modifier la révision |
|  | reviewBtn | Révision en écriture |
|  | reviewClosed | Révisions fermées |
|  | showReviewBtn | Afficher la révision |
|  | Follow | Je suis intéressé |
|  | shareText | Je viens d&#39;écrire une critique. Regardez ! |
| infobulles de notation |  |  |
|  | ratingValues | Un tableau. Valeur par défaut = [‘Pauvre’, ‘Pauvre’, ‘Juste’, ‘Moyenne’, ‘Moyenne’, ‘Bon’, ‘Bon’, ‘Excellent’, ‘Excellent’]; |
|  |  | Remarque : Les valeurs du tableau doivent être dupliquées afin d’attribuer le même nom à la moitié gauche et à la moitié droite de chaque étoile. |
| Sous-parties de notation |  |  |
|  | ratingSubpartPlaceholder | Un tableau. Par défaut = [] |
|  | ratingSubpartTitles | Un tableau. Par défaut = [] |
|  | reviewStreamTitle | Vide par défaut. Titre de la section de résumé de la révision. |
| Divers |  |  |
|  | averageRating | Note d’utilisateur moyenne |
|  | ventilationHeader | Ventilation des évaluations |
|  | useful | %s de %s a trouvé utile |
|  | usefulPlural | %s de %s a trouvé utile |
|  | outOf | / |
|  | ratingType | star |

## Informations sur la diffusion {#section_wmv_yj4_xz}

Chaînes disponibles pour les informations de diffusion de contenu et l’affichage.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Tri* |  |  |
|  | sortBy | *Vide par défaut.* |
|  | sortHighestRated | Note la plus élevée |
|  | sortLowestRated | Note la plus basse |
|  | sortMostHelpful | Très utile |
| *Diffusion en continu de divers éléments.* |  |  |
|  | showMore | Afficher plus |
| *Vitesse de diffusion élevée* |  |  |
|  | newComment | Nouvelle révision |
|  | newComments | Nouvelles révisions |
| *Nombre d’écouteurs* |  |  |
|  | listenerCount | écoute de personne |
|  | listenerCountPlural | personnes écoutant |
| *Nombre de commentaires* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *Nombre de notifications de commentaires* |  |  |
|  | commentNotifier | Nouvelle révision |
|  | commentNotifierPlural | Nouvelles révisions |

## Création/Informations sur le contenu {#section_osx_xj4_xz}

Paramètres disponibles pour les informations sur l’auteur et le contenu individuel.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Déformation des threads* |  |  |
|  | reviewContentNotFoundMsg | Cette révision n’est plus visible |
|  | backToComments | Retour aux révisions |

## Actions des utilisateurs {#section_tlx_wj4_xz}

Chaînes disponibles pour les actions de l’utilisateur : marquer, partager et marquer du contenu existant comme étant utile.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Pied de page de commentaire* |  |  |
|  | wasReviewHelpful | Utile ? |
|  | wasReviewHelpfulMobile | Utile ? |
|  | ownWasReviewHelpful | Trouvé utile. |
|  | reviewWasHelpful | Oui |
|  | usefulDivider | &amp;vert; |
|  | reviewWasNotHelpful | Non |
| *Vote modal* |  |  |
|  | voteTitle | Cette révision a-t-elle été utile ? |
|  | voteDownvote | Non |
|  | voteReplyTitle | Cette réponse a-t-elle été utile ? |
|  | voteTitle | Ce commentaire a-t-il été utile ? |
|  | voteUpvote | Oui |
| *Fenêtre d’indicateur* |  |  |
|  | flagTitle | Marquer la révision de %s |
|  | flagSuccessMsg | La révision a été signalée. |
| *Marquer Mobile* |  |  |
|  | flagConfirmationMessage | Marquer la révision de %s comme %s ? |
| *Fenêtre modale de mention* |  |  |
|  | sayDefaultText | Je vous ai mentionné dans une critique de Livefyre ! |
| *Partager le modal* |  |  |
|  | shareTitle | Partager la révision |

## Fonctions de publication {#section_yl1_wj4_xz}

Chaînes disponibles pour les utilisateurs publiant des révisions.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Éditeur* |  |  |
|  | bodyPlaceholder | Révision en écriture... |
|  | postEditButton | Modifier      |
|  | postEditCancelButton | Annuler |
|  | postAsButton | Post-révision sous la forme ... |
|  | postButton | Post-révision |
|  | postReplyAsButton | Publier comme ... |
|  | postReplyButton | Publication |
|  | shareButton | Partager |
|  | titlePlaceholder | Titre… |

## Erreurs {#section_jbc_vj4_xz}

Chaînes disponibles pour les messages d’erreur généraux.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Erreurs |  |  |
|  | errorAlreadyPosted | Vous ne pouvez publier qu’une seule révision. |
|  | errorAuthError | Vous n’êtes pas autorisé à publier une révision sur cette conversation. |
|  | errorCommentsNotAllowed | Les révisions ne peuvent pas être publiées pour le moment. |
|  | errorDislikeOwnComment | Vous ne pouvez pas ne pas aimer votre propre révision. |
|  | errorDuplicate | Même si vous avez aimé votre révision, vous n’êtes pas autorisé à la publier deux fois. |
|  | errorEditDuplicate | Vous devez modifier le corps de la révision lorsque vous la modifiez. |
|  | errorEditNotAllowed | Vous n’êtes pas autorisé à modifier des révisions sur cette conversation. |
|  | errorEditTimeExceeded | Désolé, votre période de modification de révision a expiré. |
|  | errorEmpty | Il semble que vous essayez de publier une révision vide. |
|  | errorEmptyTitle | Il semble que vous essayez de publier un titre vide. |
|  | errorFieldRating | évaluation par étoiles |
|  | errorFieldReview | review |
|  | errorFieldTitle | title |
|  | errorMaxChars | Désolé, votre examen est trop long. Modifiez et réessayez. |
|  | errorMissingFields | Veuillez saisir une |
|  | errorRatingEmpty | Vous ne pouvez pas soumettre une évaluation vide |
|  | errorRatingNotSet | Toutes les évaluations doivent être définies. |
|  | errorRatingNotValid | L’évaluation doit être un objet |
|  | errorShowMore | Une erreur s’est produite lors du chargement d’autres révisions. |
|  | errorTitleMaxChars | Désolé, votre titre est trop long. Modifiez et réessayez. |
|  | errorVoteOwnComment | Vous ne pouvez pas voter pour votre propre avis |

## Sidenotes Chaînes De Texte {#c_sidenotes_text_strings}

Personnalisation des chaînes de texte pour Livefyre Sidenotes

<!-- 

c_sidenotes_text_strings.dita

 -->

Cette page répertorie et décrit toutes les chaînes disponibles pour la personnalisation dans les applications Sidenotes. Pour plus d’informations sur les chaînes disponibles pour les applications Livefyre principales, voir Personnalisations des chaînes.

* Mise en œuvre
* Auth
* Informations sur la diffusion
* Création/Informations sur le contenu
* Actions des utilisateurs
* Fonctions de publication
* Interface du modérateur
* Erreurs

## Mise en œuvre {#section_wp2_ql4_xz}

Pour mettre en oeuvre cette fonction, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration JavaScript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

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

Chaînes disponibles pour le processus d’authentification et depuis les menus des utilisateurs authentifiés.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Chaînes de menu d’authentification* |  |  |
|  | menuAuthSignInBtn | Se connecter |
|  | menuAuthSignedInMsg | Vous devez vous connecter à {action}. |
|  | menuUserEditProfile | Modifier le profil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Se déconnecter |
|  | menuUserBackBtn | Toutes |

## Informations sur la diffusion {#section_wpy_gl4_xz}

Chaînes disponibles pour les informations de diffusion de contenu et l’affichage.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Options du menu Infos* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Aide |
|  | menuInfoLivefyreLink | Visitez Livefyre.com |

## Création/Informations sur le contenu {#section_dhb_gl4_xz}

Paramètres disponibles pour les informations sur l’auteur et le contenu individuel.

| Élément | Clé | Texte par défaut |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | En attente |
|  | commentReadMoreLink | En savoir plus |
|  | commentReplyLink | Voir {number} réponses |
|  | commentReplyLinkSing | Voir la réponse |
|  | commentVoteCount | votes |
|  | commentVoteCountSing | vote |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *Un tableau. Par défaut = *[ &quot;Janvier&quot;, &quot;Février&quot;, &quot;Mars&quot;, &quot;Avril&quot;, &quot;Mai&quot;, &quot;Juin&quot;, &quot;Juillet&quot;, &quot;Août&quot;, &quot;Septembre&quot;, &quot;Octobre&quot;, &quot;Novembre&quot;, &quot;Décembre&quot; ] |
|  | questionExplanation | Vous pouvez désormais lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets. <br>Mettez le texte en surbrillance et cliquez sur l’icône ou cliquez sur l’icône située à la fin de chaque paragraphe. |
|  | questionMockText | Ce qui est &quot;familièrement connu&quot; n&#39;est pas correctement connu, juste pour la raison qu&#39;il est &quot;familier&quot;. |
|  | questionTitle | Qu&#39;est-ce qu&#39;une Sidenote ? |

## Actions des utilisateurs {#section_qxd_fl4_xz}

Chaînes disponibles pour les actions de l’utilisateur : marquer, partager et aimer du contenu existant ;

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Options du menu Répondre* |  |  |
|  | menuRepliesViewTitle | Détails |
|  | menuRepliesViewReply | Réponse à la conversation |
| *Options du menu Partager* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Partager |
| *Options du menu Indicateur* |  |  |
|  | menuFlagOptionDissame | Désapprouver |
|  | menuFlagOptionOffensive | Offensive |
|  | menuFlagOptionOffTopic | Désactivation de la rubrique |
|  | menuFlagOptionSpam | Indésirables |
|  | menuFlagTitle | Marquer comme ... |
|  | facebookShareCaption | Sidenotes sur &quot;{title}&quot; |
| *Options utilisateur mobiles* |  |  |
|  | sliderCommentTally | of |
|  | sliderInviteRead | Lu |
|  | sliderInviteWrite | Write |
|  | sliderLoading | Chargement en cours… |
|  | sliderWriteText | Que penses-tu ? Appuyez pour écrire. |

## Fonctions de publication {#section_xzf_2l4_xz}

Chaînes disponibles pour les utilisateurs publiant du contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
|  | editorEditBtn | Enregistrer |
|  | editorEditPoting | Enregistrer... |
|  | editorEditReplyTitle | Modifier la réponse |
|  | editorEditTitle | Modifier le sidenote |
|  | editorPlaceholder | Que penses-tu ? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Publication |
|  | editorPost | Publication… |
|  | editorReplyBtn | Poster une réponse |
|  | editorReplyTitle | Write Reply |
|  | editorTitle | Write Sidenote |
|  | emptyImageBlockTxt | Que penses-tu ? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Répondre |
|  | threadReplyBtn | Réponse à la conversation |
| *Options du menu Supprimer* |  |  |
|  | menuConfirmAccept | Oui, {action} |
|  | menuConfirmCancel | Annuler |
|  | menuConfirmTitle | Etes-vous sûr ? |
| *Options de menu etc.* |  |  |
|  | menuEtcOptionApprove | Approuver |
|  | menuEtcOptionDelete | Supprimer |
|  | menuEtcOptionEdit | Modifier      |
|  | menuEtcOptionFlag | Marquer d’un indicateur |
|  | menuEtcOptionShare | Partager |
|  | menuEtcPostedAt | Publié le {date} |
|  | menuEtcTitle | Plus |

## Interface du modérateur {#section_o5f_dl4_xz}

Chaînes disponibles dans l’interface du modérateur authentifié par l’utilisateur.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Messages de confirmation du menu Plus* |  |  |
|  | notificationApproval | Approuvés |
|  | notificationDeleted | Supprimé |
|  | notificationFlagged | Avec indicateur |

## Erreurs {#section_gtk_cl4_xz}

Chaînes disponibles pour les messages d’erreur généraux.

| Élément | Clé | Texte par défaut |
|---|---|---|
|  | errorConnection | Oh oh. Vous ne semblez pas avoir une bonne connexion. |
|  | errorDuplicate | Votre note nous plaît aussi, mais vous ne pouvez pas la publier deux fois. |
|  | errorGeneral | Une erreur s’est produite. Veuillez réessayer. |
|  | errorServer | Quelque chose a mal tourné avec notre serveur. Essaie encore ça ? |
