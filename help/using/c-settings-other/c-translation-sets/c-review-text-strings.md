---
description: Personnalisation des chaînes de texte pour les révisions Livefyre.
title: Vérifier les chaînes de texte
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# Vérifier les chaînes de texte{#review-text-strings}

Personnalisation des chaînes de texte pour les révisions Livefyre.

Cette page répertorie et décrit les chaînes disponibles pour la personnalisation dans les applications de révision. Les chaînes répertoriées ici s’ajoutent aux chaînes par défaut des applications de base Livefyre et les remplacent, répertoriées dans Personnalisations des chaînes. Lorsque des doublons sont répertoriés, les chaînes répertoriées dans ces tableaux sont la valeur par défaut des applications Reviews.

Implémentation
Interface de révision/notation
Informations sur la diffusion
Création/Informations sur le contenu
Actions des utilisateurs
Fonctions de publication
Erreurs

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
|--- |--- |--- |
| Boutons | editReviewBtn | Modifier la révision |
|  | reviewBtn | Révision en écriture |
|  | reviewClosed | Révisions fermées |
|  | showReviewBtn | Afficher la révision |
|  | Follow | Je suis intéressé |
|  | shareText | Je viens d&#39;écrire une critique. Regardez ! |
| infobulles de notation | ratingValues | Un tableau. Par défaut = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Remarque : Les valeurs du tableau doivent être dupliquées afin d’affecter le même nom à la moitié gauche et à la moitié droite de chaque étoile. |
| Sous-parties de notation | ratingSubpartPlaceholder | Un tableau. Par défaut = `[]` |
|  | ratingSubpartTitles | Un tableau. Par défaut = `[]` |
|  | reviewStreamTitle | Vide par défaut. Titre de la section de résumé de la révision. |
| Divers | averageRating | Note d’utilisateur moyenne |
|  | ventilationHeader | Ventilation des évaluations |
|  | useful | %s de %s a trouvé utile |
|  | usefulPlural | %s de %s a trouvé utile |
|  | outOf | / |
|  | ratingType | star |

## Informations sur la diffusion {#section_wmv_yj4_xz}

Chaînes disponibles pour les informations de diffusion de contenu et l’affichage.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Tri | sortBy | Vide par défaut. |
|  | sortHighestRated | Note la plus élevée |
|  | sortLowestRated | Note la plus basse |
|  | sortMostHelpful | Très utile |
| Diffusion en continu de divers éléments. | showMore | Afficher plus |
| Vitesse de diffusion élevée | newComment | Nouvelle révision |
|  | newComments | Nouvelles révisions |
| Nombre d’écouteurs | listenerCount | écoute de personne |
|  | listenerCountPlural | personnes écoutant |
| Nombre de commentaires | commentCountLabel | LiveReviews<strong> | </strong> |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Nombre de notifications de commentaires | commentNotifier | Nouvelle révision |
|  | commentNotifierPlural | Nouvelles révisions |

## Création/Informations sur le contenu {#section_osx_xj4_xz}

Paramètres disponibles pour les informations sur l’auteur et le contenu individuel.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Déformation des threads | reviewContentNotFoundMsg | Cette révision n’est plus visible |
|  | backToComments | Retour aux révisions |

## Actions des utilisateurs {#section_tlx_wj4_xz}

Chaînes disponibles pour les actions de l’utilisateur : marquer, partager et marquer du contenu existant comme étant utile.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Pied de page de commentaire | wasReviewHelpful | Utile ? |
|  | wasReviewHelpfulMobile | Utile ? |
|  | ownWasReviewHelpful | Trouvé utile. |
|  | reviewWasHelpful | Oui |
|  | usefulDivider | &amp;vert; |
|  | reviewWasNotHelpful | Non |
| Vote modal | voteTitle | Cette révision a-t-elle été utile ? |
|  | voteDownvote | Non |
|  | voteReplyTitle | Cette réponse a-t-elle été utile ? |
|  | voteTitle | Ce commentaire a-t-il été utile ? |
|  | voteUpvote | Oui |
| Fenêtre d’indicateur | flagTitle | Marquer la révision de %s |
|  | flagSuccessMsg | La révision a été signalée. |
| Marquer Mobile | flagConfirmationMessage | Marquer la révision de %s comme %s ? |
| Fenêtre modale de mention | sayDefaultText | Je vous ai mentionné dans une critique de Livefyre ! |
| Partager le modal | shareTitle | Partager la révision |

## Fonctions de publication {#section_yl1_wj4_xz}

Chaînes disponibles pour les utilisateurs publiant des révisions.

| Élément | Clé | Texte par défaut |
|---|---|---|
| Éditeur | bodyPlaceholder | Révision en écriture... |
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
| Erreurs | errorAlreadyPosted | Vous ne pouvez publier qu’une seule révision. |
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
