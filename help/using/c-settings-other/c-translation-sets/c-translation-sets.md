---
description: Les jeux de traduction vous permettent de spécifier une autre langue pour les applications.
title: Jeux de transformations
exl-id: 1de99602-b97e-42e9-8450-39abd4ba2f9b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 7%

---

# Jeux de traduction{#translation-sets}

Les jeux de traduction vous permettent de spécifier une autre langue pour les applications.

Utilisez les paramètres de traduction pour localiser des applications dans différentes langues ou pour spécifier un texte de remplacement pour plusieurs applications à partir d’un seul emplacement dans Studio. Par exemple, vous pouvez vous assurer que tous les sites en espagnol utilisent l’espagnol pour tous les champs de l’application. Vous pouvez également modifier le texte afin que tous les champs correspondent à la voix et à l’aspect de votre site ou réseau.

Vous pouvez spécifier des paramètres de traduction pour toutes les applications, à l’exception de Storify 2. Pour plus d’informations sur les champs que vous pouvez localiser, voir [Localize Strings](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings).

Commentaires, Live Blog et Chat partagent le même ensemble de chaînes au sein d’un jeu de traductions.

Spécifiez un jeu de traduction pour un réseau, un site, une application ou en utilisant une API.

Les jeux de traduction à différents niveaux se remplacent en suivant ce modèle :

Le jeu de traduction d’API remplace tous les jeux de traduction à n’importe quel niveau (application, réseau et site)
Le jeu de traduction d’application remplace les jeux de traduction au niveau du réseau et au niveau du site.
Les jeux de traduction au niveau du site remplacent les jeux de traduction au niveau du réseau.

## Vérifier les chaînes de texte {#c_review_text_strings}

Personnalisation des chaînes de texte pour les révisions de Livefyre.

Cette page liste et décrit les chaînes disponibles pour la personnalisation dans les applications de révision. Les chaînes répertoriées ici s’ajoutent aux chaînes par défaut pour les applications de base Livefyre et les remplacent, répertoriées dans la section Personnalisations des chaînes. Lorsque des duplicata sont répertoriés, les chaînes répertoriées dans ces tableaux sont la valeur par défaut des applications Reviews.

Implémentation
Interface de révision/évaluation
Informations sur le flux
Auteur / Informations sur le contenu
Actions de l’utilisateur
Fonctions de publication
Erreurs

## Implémentation {#section-vsy-1k4-xz}

Pour mettre en oeuvre cette fonctionnalité, transmettez un mappage d’objet 1-1 des chaînes que vous souhaitez remplacer à l’objet de configuration JavaScript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

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

## Interface de révision et de notation {#section_iyv_zj4_xz}

Chaînes disponibles pour l’interface utilisateur Révision et évaluation.

| Élément | Clé | Texte par défaut |
|--- |--- |--- |
| Boutons | editReviewBtn | Modifier la révision |
|  | reviewBtn | Révision en écriture |
|  | reviewsFermés | Révisions clôturées |
|  | showReviewBtn | Afficher la révision |
|  | follow | Je suis intéressé |
|  | shareText | Je viens d&#39;écrire une critique. Regardez ! |
| Info-bulles de notation | ratingValues | Un tableau. Par défaut = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Remarque : Les valeurs du tableau doivent être dupliquées pour attribuer le même nom à la moitié gauche et à la moitié droite de chaque étoile. |
| Sous-parties de classement | ratingSubpartPlaceholder | Un tableau. Par défaut = [] |
|  | ratingSubpartTitles | Un tableau. Par défaut = [] |
|  | reviewStreamTitle | Vierge par défaut. Titre de la section de résumé de la révision. |
| Divers | averageRating | Note moyenne de l’utilisateur |
|  | breakHeader | Ventilation des notes |
|  | utile | %s sur %s a trouvé utile |
|  | utilePlural | %s sur %s a trouvé utile |
|  | outOf | / |
|  | ratingType | star |

## Informations sur le flux {#section_wmv_yj4_xz}

Chaînes disponibles pour l’affichage et les informations du flux de contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Tri | sortBy | *Vierge par défaut.* |
|  | sortHighestRated | [Note la plus élevée](https://d.pr/i/huTd) |
|  | sortLowestRated | [Note la moins élevée](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Très utile](https://d.pr/i/huTd) |
| Diffusion en continu. | showMore | Afficher plus |
| Vitesse de diffusion élevée | newComment | Nouvelle révision |
|  | newComments | Nouvelles révisions |
| Nombre d’écouteurs | listenerCount | écoute de personne |
|  | listenerCountPlural | écoute |
| Nombre de commentaires | commentCountLabel | LiveReviews<strong> | </strong> |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Nombre de notifications de notification | commentNotifier | Nouvelle révision |
|  | commentNotifierPlural | Nouvelles révisions |

## Auteur / Informations sur le contenu {#section_osx_xj4_xz}

Paramètres disponibles pour les informations sur l’auteur et le contenu individuel.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Ventilation du thread | reviewsContentNotFoundMsg | [Cette révision n&#39;est plus visible](https://d.pr/i/svXs) |
|  | backToComments | Retour aux révisions |

## Actions de l&#39;utilisateur {#section_tlx_wj4_xz}

Chaînes disponibles pour les actions de l’utilisateur : signaler, partager et marquer du contenu existant comme utile.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Pied de page de commentaire | wasReviewHelpful | [Utile ?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Utile ? |
|  | ownWasReviewHelpful | [J&#39;ai trouvé utile.](https://d.pr/i/Q0mA) |
|  | reviewWasHelpful | [Oui](https://d.pr/i/Q0mA) |
|  | usefulDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHelpful | [Non](https://d.pr/i/Q0mA) |
| Vote modal | voteTitle | Cette révision a-t-elle été utile ? |
|  | VoteDownvote | Non |
|  | voteReplyTitle | Cette réponse a-t-elle été utile ? |
|  | voteTitle | Ce commentaire a-t-il été utile ? |
|  | voteUpvote | Oui |
| Indicateur modal | flagTitle | Indicateur %s de la révision |
|  | flagSuccessMsg | La révision a été marquée. |
| Indicateur Mobile | flagConfirmationMessage | Marquer la révision de %s comme %s ? |
| Mention modale | mentionsDefaultText | Je vous ai mentionné dans une critique de Livefyre ! |
| Partager le mode | shareTitle | Partager la révision |

## Fonctions de publication {#section_yl1_wj4_xz}

Chaînes disponibles pour les utilisateurs qui publient des révisions.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Éditeur | bodyPlaceholder | Révision en écriture... |
|  | postEditButton | Modifier      |
|  | postEditCancelButton | Annuler |
|  | postAsButton | Post-révision as... |
|  | postButton | Post-révision |
|  | postReplyAsButton | Publier comme... |
|  | postReplyButton | Publication |
|  | shareButton | Partager |
|  | titlePlaceholder | Titre… |

## Erreurs {#section_jbc_vj4_xz}

Chaînes disponibles pour les messages d’erreur généraux.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Erreurs | errorDéjàPosted | Vous ne pouvez publier qu’une seule révision. |
|  | errorAuthError | Vous n’êtes pas autorisé à publier une révision sur cette conversation |
|  | errorCommentsNotAllowed | Les révisions ne peuvent pas être publiées pour le moment |
|  | errorDislikeOwnComment | Vous ne pouvez pas ne pas aimer votre propre évaluation. |
|  | errorDuplicate | Vous n’avez pas le droit de publier votre avis deux fois, même si vous avez aimé votre avis. |
|  | errorEditDuplicate | Vous devez modifier le corps de la révision lorsque vous la modifiez. |
|  | errorEditNotAllowed | Vous n&#39;êtes pas autorisé à modifier des révisions sur cette conversation. |
|  | errorEditTimeExceeded | Votre période de modification de révision a expiré. |
|  | errorEmpty | Il semble que vous essayez de publier une révision vide. |
|  | errorEmptyTitle | Il semble que vous essayez de publier un titre vide |
|  | errorFieldRating | évaluation |
|  | errorFieldReview | examiner |
|  | errorFieldTitle | title |
|  | errorMaxChars | Désolé, votre avis est trop long. Veuillez modifier et réessayer. |
|  | errorMissingFields | Veuillez saisir une |
|  | errorRatingEmpty | Vous ne pouvez pas soumettre une évaluation vide |
|  | errorRatingNotSet | Toutes les évaluations doivent être définies |
|  | errorRatingNotValid | L&#39;évaluation doit être un objet |
|  | errorShowMore | Une erreur s&#39;est produite lors du chargement d&#39;autres révisions. |
|  | errorTitleMaxChars | Désolé, votre titre est trop long. Veuillez modifier et réessayer. |
|  | errorVoteOwnComment | Vous ne pouvez pas voter pour votre propre révision |

## Sidenotes chaînes de texte {#c_sidenotes_text_strings}

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
|  | datetimeMonths | Un tableau. Par défaut =[ &quot;Janvier&quot;, &quot;Février&quot;, &quot;Mars&quot;, &quot;Avril&quot;, &quot;Mai&quot;, &quot;Juin&quot;, &quot;Juillet&quot;, &quot;Août&quot;, &quot;Septembre&quot;, &quot;Octobre&quot;, &quot;Novembre&quot;, &quot;Décembre&quot; ] |
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
