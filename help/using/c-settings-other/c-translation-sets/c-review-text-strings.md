---
description: Personnalisation des chaînes de texte pour Livefyre Reviews.
seo-description: Personnalisation des chaînes de texte pour Livefyre Reviews.
seo-title: Vérifier les chaînes de texte
solution: Experience Manager
title: Vérifier les chaînes de texte
uuid: 86251e49-bc73-4eec-9f9b-b4b0a5b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Vérifier les chaînes de texte{#review-text-strings}

Personnalisation des chaînes de texte pour Livefyre Reviews.

Cette page répertorie et décrit les chaînes disponibles pour la personnalisation dans les applications de révision. Les chaînes répertoriées ici s’ajoutent aux chaînes par défaut des applications de base Livefyre et les remplacent, répertoriées dans la section Personnalisations des chaînes. Lorsque des doublons sont répertoriés, les chaînes répertoriées dans ces tableaux sont la valeur par défaut des applications de révision.

ImplémentationRévision / Interface de notationFlux d'informationsAuteur / Informations sur le contenuActions de l'utilisateurFonctions de publicationErreurs

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
|--- |--- |--- |
| Boutons | editReviewBtn | Modifier la révision |
|  | reviewBtn | [Révision en écriture](https://d.pr/i/QscA) |
|  | reviewsFermé | [Révisions fermées](https://d.pr/i/zr7M) |
|  | showReviewBtn | [Afficher la révision](https://d.pr/i/onxU) |
|  | suivre | Je suis intéressé |
|  | shareText | Je viens d'écrire une critique. Regarde ! |
| Info-bulles de notation | ratingValues | Un tableau. Default = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Remarque : Les valeurs du tableau doivent être dupliquées pour attribuer le même nom à la moitié gauche et à la moitié droite de chaque étoile. |
| Sous-parties de classement | ratingSubpartPlaceholder | Un tableau. Par défaut = `[]` |
|  | ratingSubpartTitles | Un tableau. Par défaut = `[]` |
|  | reviewStreamTitle | Vide par défaut. Titre de la section Résumé de la révision. |
| Misc | note moyenne | [Note moyenne utilisateur](https://d.pr/i/QscA) |
|  | breakHeader | [Ventilation des notes](https://d.pr/i/QscA) |
|  | utile | %s sur %s a trouvé utile |
|  | utilePlural | %s sur %s a trouvé utile |
|  | outOf | / |
|  | ratingType | star |

## Informations sur le flux {#section_wmv_yj4_xz}

Chaînes disponibles pour l’affichage et l’information du flux de contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Tri | sortBy | Vide par défaut. |
|  | sortHighestRated | [Note la plus élevée](https://d.pr/i/huTd) |
|  | sortLowestRated | [Note la plus basse](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Très utile](https://d.pr/i/huTd) |
| Diffusion en continu. | showMore | Afficher plus |
| Vitesse de diffusion élevée | newComment | Nouvelle révision |
|  | newComments | Nouvelles révisions |
| Nombre d’écouteurs | listenerCount | écoute de personne |
|  | listenerCountPlural | personnes écoutant |
| Nombre de commentaires | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Nombre de notifications de commentaires | commentNotifier | Nouvelle révision |
|  | commentNotifierPlural | Nouvelles révisions |

## Auteur / Informations sur le contenu {#section_osx_xj4_xz}

Paramètres disponibles pour les informations sur l’auteur et le contenu individuel.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Ventilation du thread | reviewsContentNotFoundMsg | [Cette révision n’est plus visible](https://d.pr/i/svXs) |
|  | backToComments | Retour aux révisions |

## Actions de l’utilisateur {#section_tlx_wj4_xz}

Chaînes disponibles pour les actions utilisateur : marquer, partager et marquer le contenu existant comme utile.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Pied de page de commentaire | wasReviewHelpful | [Utile ?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Utile ? |
|  | ownWasReviewHelpful | [J'ai trouvé utile.](https://d.pr/i/Q0mA) |
|  | reviewWasHelpful | [Oui](https://d.pr/i/Q0mA) |
|  | helpDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHelpful | [Non](https://d.pr/i/Q0mA) |
| Vote modal | voteTitle | Cette révision a-t-elle été utile ? |
|  | voteDownvote | Non |
|  | voteReplyTitle | Cette réponse a-t-elle été utile ? |
|  | voteTitle | Ce commentaire a-t-il été utile ? |
|  | voteUpvote | Oui |
| Indicateur modal | flagTitle | Marquer la révision de %s |
|  | flagSuccessMsg | La révision a été marquée. |
| Marquer Mobile | flagConfirmationMessage | Marquer la révision de %s comme %s ? |
| Mention modale | mentionsDefaultText | Je vous ai mentionné dans une critique de Livefyre ! |
| Partager le mode | shareTitle | Partager la révision |

## Fonctions de publication {#section_yl1_wj4_xz}

Chaînes disponibles pour les utilisateurs qui publient des révisions.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Éditeur | bodyPlaceholder | Révision en écriture... |
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
| Erreurs | errorAlreadyPosted | Vous ne pouvez publier qu’une seule révision. |
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

