---
description: Les jeux de traduction vous permettent de spécifier une autre langue pour les applications.
seo-description: Les jeux de traduction vous permettent de spécifier une autre langue pour les applications.
seo-title: Jeux de transformations
solution: Experience Manager
title: Jeux de transformations
uuid: 8ba66a61-5520-482a-bc0b-e4f6b57f1744
translation-type: tm+mt
source-git-commit: 366b7248c2f3b6994fa10419599e66fa1c8e5e48

---


# Jeux de transformations {#translation-sets}

Les jeux de traduction vous permettent de spécifier une autre langue pour les applications.

<!-- 
c_translation_sets.dita
-->

Utilisez les paramètres de traduction pour localiser des applications dans différentes langues ou pour spécifier un texte alternatif pour plusieurs applications à partir d’un seul emplacement dans Studio. Par exemple, vous pouvez vous assurer que tous les sites en espagnol utilisent l’espagnol pour tous les champs de l’application. Vous pouvez également modifier le texte afin que tous les champs correspondent à la voix et à l’aspect de votre site ou réseau.

Vous pouvez spécifier des paramètres de traduction pour toutes les applications, à l’exception de Storify 2. Pour plus d’informations sur les champs que vous pouvez localiser, voir [Localisation des chaînes](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Commentaires, Live Blog et Chat partagent le même ensemble de chaînes dans un jeu de traductions.

Spécifiez un jeu de conversions pour un réseau, un site, une application ou à l’aide d’une API.

Les jeux de traduction à différents niveaux se remplacent les uns les autres selon ce modèle :

* Le jeu de conversions API remplace les jeux de conversions à n’importe quel niveau (application, réseau et site)
* Le jeu de traduction d’application remplace les jeux de traduction au niveau du réseau et au niveau du site.
* Les jeux de traduction au niveau du site remplacent les jeux de traduction au niveau du réseau.

## Vérifier les chaînes de texte {#c-review-text-strings}

Personnalisation des chaînes de texte pour Livefyre Reviews.

Cette page répertorie et décrit les chaînes disponibles pour la personnalisation dans les applications de révision. Les chaînes répertoriées ici s’ajoutent aux chaînes par défaut des applications de base Livefyre et les remplacent, répertoriées dans la section Personnalisations des chaînes. Lorsque des doublons sont répertoriés, les chaînes répertoriées dans ces tableaux sont la valeur par défaut des applications de révision.

* Mise en œuvre
* Interface de révision/évaluation
* Informations sur le flux
* Auteur / Informations sur le contenu
* Actions de l’utilisateur
* Fonctions de publication
* Erreurs

## Implémentation {#section-vsy-1k4-xz}

Pour implémenter cette fonctionnalité, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration Javascript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

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

## Interface de révision/évaluation {#section_iyv_zj4_xz}

Chaînes disponibles pour l’interface utilisateur de révision et d’évaluation.

| Élément | Clé | Texte par défaut |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Boutons |  |  |
|  | editReviewBtn | Modifier la révision |
|  | reviewBtn | Révision en écriture |
|  | reviewsFermé | Révisions fermées |
|  | showReviewBtn | Afficher la révision |
|  | suivre | Je suis intéressé |
|  | shareText | Je viens d'écrire une critique. Regarde ! |
| Info-bulles de notation |  |  |
|  | ratingValues | Un tableau. Par Défaut =["Pauvres", "Pauvres", "Bonnes", "Bonnes", "Bonnes", "Excellentes", "Excellentes"]; |
|  |  | Remarque : les valeurs du tableau doivent être dupliquées pour affecter le même nom à la moitié gauche et à la moitié droite de chaque étoile. |
| Sous-parties de classement |  |  |
|  | ratingSubpartPlaceholder | Un tableau. Par défaut = [] |
|  | ratingSubpartTitles | Un tableau. Par défaut = [] |
|  | reviewStreamTitle | Vide par défaut. Titre de la section Résumé de la révision. |
| Misc |  |  |
|  | note moyenne | Note moyenne utilisateur |
|  | breakHeader | Ventilation des notes |
|  | utile | %s sur %s a trouvé utile |
|  | utilePlural | %s sur %s a trouvé utile |
|  | outOf | / |
|  | ratingType | star |

## Informations sur le flux {#section_wmv_yj4_xz}

Chaînes disponibles pour l’affichage et l’information du flux de contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Tri* |  |  |
|  | sortBy | *Vide par défaut.* |
|  | sortHighestRated | [Note la plus élevée](https://d.pr/i/huTd) |
|  | sortLowestRated | [Note la plus basse](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Très utile](https://d.pr/i/huTd) |
| *Diffusion en continu.* |  |  |
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

## Auteur / Informations sur le contenu {#section_osx_xj4_xz}

Paramètres disponibles pour les informations sur l’auteur et le contenu individuel.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Ventilation du thread* |  |  |
|  | reviewsContentNotFoundMsg | [Cette révision n’est plus visible](https://d.pr/i/svXs) |
|  | backToComments | Retour aux révisions |

## Actions de l’utilisateur {#section_tlx_wj4_xz}

Chaînes disponibles pour les actions utilisateur : marquer, partager et marquer le contenu existant comme utile.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Pied de page de commentaire* |  |  |
|  | wasReviewHelpful | [Utile ?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Utile ? |
|  | ownWasReviewHelpful | [J'ai trouvé utile.](https://d.pr/i/Q0mA) |
|  | reviewWasHelpful | [Oui](https://d.pr/i/Q0mA) |
|  | helpDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHelpful | [Non](https://d.pr/i/Q0mA) |
| *Vote modal* |  |  |
|  | voteTitle | Cette révision a-t-elle été utile ? |
|  | voteDownvote | Non |
|  | voteReplyTitle | Cette réponse a-t-elle été utile ? |
|  | voteTitle | Ce commentaire a-t-il été utile ? |
|  | voteUpvote | Oui |
| *Indicateur modal* |  |  |
|  | flagTitle | Marquer la révision de %s |
|  | flagSuccessMsg | La révision a été marquée. |
| *Marquer Mobile* |  |  |
|  | flagConfirmationMessage | Marquer la révision de %s comme %s ? |
| *Mention modale* |  |  |
|  | mentionsDefaultText | Je vous ai mentionné dans une critique de Livefyre ! |
| *Partager le mode* |  |  |
|  | shareTitle | Partager la révision |

## Fonctions de publication {#section_yl1_wj4_xz}

Chaînes disponibles pour les utilisateurs qui publient des révisions.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Éditeur* |  |  |
|  | bodyPlaceholder | Révision en écriture... |
|  | postEditButton | Modifier      |
|  | postEditCancelButton | Annuler |
|  | postAsButton | Post-révision en tant que... |
|  | postButton | Post-révision |
|  | postReplyAsButton | Publier comme... |
|  | postReplyButton | Publication |
|  | shareButton | Partager |
|  | titlePlaceholder | Titre… |

## Erreurs {#section_jbc_vj4_xz}

Chaînes disponibles pour les messages d’erreur généraux.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Erreurs |  |  |
|  | errorAlreadyPosted | Vous ne pouvez publier qu’une seule révision. |
|  | errorAuthError | Vous n’êtes pas autorisé à publier une révision sur cette conversation |
|  | errorCommentsNotAllowed | Les révisions ne peuvent pas être publiées pour le moment |
|  | errorDislikeOwnComment | Vous ne pouvez pas détester votre propre évaluation. |
|  | errorDuplicate | Vous n’avez pas le droit de le publier deux fois, même si vous avez aimé votre commentaire. |
|  | errorEditDuplicate | Vous devez modifier le corps de la révision lorsque vous la modifiez. |
|  | errorEditNotAllowed | Vous n’êtes pas autorisé à modifier les révisions sur cette conversation. |
|  | errorEditTimeExceeded | Désolé, votre période de modification de révision a expiré. |
|  | errorEmpty | Il semble que vous teniez de publier une révision vide. |
|  | errorEmptyTitle | Vous essayez de publier un titre vide. |
|  | errorFieldRating | note d'étoiles |
|  | errorFieldReview | révision |
|  | errorFieldTitle | title |
|  | errorMaxChars | Désolé, votre examen est trop long. Veuillez modifier et réessayer. |
|  | errorMissingFields | Veuillez saisir une |
|  | errorRatingEmpty | Vous ne pouvez pas envoyer une évaluation vide |
|  | errorRatingNotSet | Toutes les évaluations doivent être définies |
|  | errorRatingNotValid | La notation doit être un objet |
|  | errorShowMore | Une erreur s'est produite lors du chargement d'autres révisions. |
|  | errorTitleMaxChars | Désolé, votre titre est trop long. Veuillez modifier et réessayer. |
|  | errorVoteOwnComment | Vous ne pouvez pas voter pour votre propre avis |

## Sidenotes chaînes de texte {#c_sidenotes_text_strings}

Personnalisation des chaînes de texte pour les Sidenotes Livefyre

<!-- 

c_sidenotes_text_strings.dita

 -->

Cette page répertorie et décrit toutes les chaînes disponibles pour la personnalisation dans les applications Sidenotes. Pour plus d’informations sur les chaînes disponibles pour les principales applications Livefyre, voir Personnalisations des chaînes.

* Mise en œuvre
* Auth
* Informations sur le flux
* Auteur / Informations sur le contenu
* Actions de l’utilisateur
* Fonctions de publication
* Interface du modérateur
* Erreurs

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
| *Chaînes du menu Auth* |  |  |
|  | menuAuthSignInBtn | Se connecter |
|  | menuAuthSignedInMsg | Vous devez vous connecter à {action} |
|  | menuUserEditProfile | Modifier le profil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Se déconnecter |
|  | menuUserBackBtn | Toutes |

## Informations sur le flux {#section_wpy_gl4_xz}

Chaînes disponibles pour l’affichage et l’information du flux de contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Options du menu Infos* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
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
|  | datetimeMonths | *Un tableau. Default = *[ ‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’ ] |
|  | questionExplication | Vous pouvez maintenant lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets. <br>Mettez le texte en surbrillance et cliquez sur l’icône ou cliquez sur l’icône à la fin de chaque paragraphe. |
|  | questionMockText | Ce qui est "familiairement connu" n'est pas correctement connu, juste pour la raison qu'il est "familier". |
|  | questionTitle | Qu'est-ce qu'une Sidenote ? |

## Actions de l’utilisateur {#section_qxd_fl4_xz}

Chaînes disponibles pour les actions utilisateur : marquage, partage et mention J’aime du contenu existant.

| Élément | Clé | Texte par défaut |
|---|---|---|
| *Options du menu Répondre* |  |  |
|  | menuRéponsesAfficherTitre | Détails |
|  | menuRéponsesViewReply | Réponse à la conversation |
| *Options du menu Partager* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Partager |
| *Options du menu Indicateur* |  |  |
|  | menuFlagOptionDésaccord | Désapprouver |
|  | menuFlagOptionOffensive | Offensive |
|  | menuFlagOptionOffTopic | Hors rubrique |
|  | menuFlagOptionSpam | Indésirables |
|  | menuFlagTitle | Marquer comme... |
|  | facebookShareCaption | Sidenotes sur "{title}" |
| *Options utilisateur mobiles* |  |  |
|  | sliderCommentTally | of |
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
| *Supprimer les options du menu* |  |  |
|  | menuConfirmAccept | Oui, {action} |
|  | menuConfirmCancel | Annuler |
|  | menuConfirmTitle | Etes-vous sûr ? |
| *Options du menu Etc* |  |  |
|  | menuEtcOptionApprouver | Approuver |
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
| *Messages de confirmation du menu Plus* |  |  |
|  | notificationApprouvé | Approuvés |
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
