---
description: Personnalisation des chaînes de texte pour les révisions de Livefyre.
seo-description: Personnalisation des chaînes de texte pour les révisions de Livefyre.
seo-title: Vérifier les chaînes de texte
solution: Experience Manager
title: Vérifier les chaînes de texte
uuid: 86251e49-bc73-4eec-9f9b-b4b0a5b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 5%

---


# Vérifier les chaînes de texte{#review-text-strings}

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
|  | reviewBtn | [Révision en écriture](https://d.pr/i/QscA) |
|  | reviewsFermés | [Révisions clôturées](https://d.pr/i/zr7M) |
|  | showReviewBtn | [Afficher la révision](https://d.pr/i/onxU) |
|  | follow | Je suis intéressé |
|  | shareText | Je viens d&#39;écrire une critique. Regardez ! |
| Info-bulles de notation | ratingValues | Un tableau. Par défaut = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Remarque : Les valeurs du tableau doivent être dupliquées pour attribuer le même nom à la moitié gauche et à la moitié droite de chaque étoile. |
| Sous-parties de classement | ratingSubpartPlaceholder | Un tableau. Par défaut = `[]` |
|  | ratingSubpartTitles | Un tableau. Par défaut = `[]` |
|  | reviewStreamTitle | Vierge par défaut. Titre de la section de résumé de la révision. |
| Divers | averageRating | [Note moyenne de l’utilisateur](https://d.pr/i/QscA) |
|  | breakHeader | [Ventilation des notes](https://d.pr/i/QscA) |
|  | utile | %s sur %s a trouvé utile |
|  | utilePlural | %s sur %s a trouvé utile |
|  | outOf | / |
|  | ratingType | star |

## Informations sur le flux {#section_wmv_yj4_xz}

Chaînes disponibles pour l’affichage et les informations du flux de contenu.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Tri | sortBy | Vierge par défaut. |
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

