---
description: Personnalisation des chaînes de texte pour les révisions Livefyre.
seo-description: Personnalisation des chaînes de texte pour les révisions Livefyre.
seo-title: Révision des chaînes de texte
solution: Experience Manager
title: Révision des chaînes de texte
uuid: 86251 e 49-bc 73-4 eec -9 f 9 b-b 4 b 0 a 5 b 42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Révision des chaînes de texte{#review-text-strings}

Personnalisation des chaînes de texte pour les révisions Livefyre.

Cette page répertorie et décrit les chaînes disponibles pour la personnalisation dans les applications de révision. Les chaînes répertoriées ici s&#39;ajoutent aux chaînes par défaut des applications Livefyre, répertoriées dans la section Personnalisations de chaînes. Lorsque des doublons sont répertoriés, les chaînes répertoriées dans ces tableaux sont les valeurs par défaut pour les applications de révision.

Analyse de mise en œuvre/Informations
de flux d&#39;interface
de flux Informations Auteur/Contenu Informations
de l&#39;utilisateur Fonctions de publication

## Implémentation {#section-vsy-1k4-xz}

Pour mettre en œuvre cette fonction, transmettez un mappage d&#39;objet 1-1 des chaînes que vous souhaitez remplacer par l&#39;objet de configuration Javascript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

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

Chaînes disponibles pour l&#39;interface utilisateur de révision et de notation.

| Elément | Clé | Texte par défaut |
|--- |--- |--- |
| Boutons | Editreviewbtn | Modifier la révision |
|  | Reviewbtn | [Révision de la révision](https://d.pr/i/QscA) |
|  | Reviewsclosed | [Révisions fermées](https://d.pr/i/zr7M) |
|  | Showreviewbtn | [Afficher la révision](https://d.pr/i/onxU) |
|  | suivre | Je suis intéressé |
|  | Sharetext | Je viens de rédiger une révision. Vérifiez-la ! |
| Info-bulles | Ratingvalues | Un tableau. Default = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Remarque : Les valeurs du tableau doivent être dupliquées pour affecter à la fois la moitié gauche et la moitié droite de chaque étoile au même nom. |
| Sous-parties de notation | Ratingsubpartplaceholder | Un tableau. Par défaut = `[]` |
|  | Ratingsubparttitles | Un tableau. Par défaut = `[]` |
|  | Reviewstreamtitle | Vide par défaut. Titre de la section résumé de la révision. |
| Misc | Averagerating | [Évaluation moyenne des utilisateurs](https://d.pr/i/QscA) |
|  | Breakdownheader | [Ventilation d&#39;évaluation](https://d.pr/i/QscA) |
|  | utile | % s sur % s trouvé |
|  | Helpfulplural | % s sur % s trouvé |
|  | out of | / |
|  | Ratingtype | star |

## Informations de diffusion en continu {#section_wmv_yj4_xz}

Chaînes disponibles pour les informations de flux de contenu et affichées.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Tri | Sortby | Vide par défaut. |
|  | Sorthighestrated | [Évaluation la plus élevée](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Note la plus faible](https://d.pr/i/huTd) |
|  | Sortmosthelpound | [Plus efficace](https://d.pr/i/huTd) |
| Stream misc. | Showmore | Montrer plus |
| Vélocité élevée du flux | Newcomment | Nouvelle révision |
|  | Newcomments | Nouvelles révisions |
| Nombre d&#39;écouteurs | Listenercount | personne qui écoute |
|  | Listenercountplural | personne qui écoute |
| Nombre de commentaires | Commentcountlabel | Livereviews<strong> | </strong>% s |
|  | Commentcountlabelplural | Livereviews<strong> | </strong>% s |
| Nombre de notifications de commentaire | Commentnotification | Nouvelle révision |
|  | Commentnotifierplural | Nouvelles révisions |

## Informations Auteur/Contenu {#section_osx_xj4_xz}

Stings disponibles pour l&#39;auteur et les informations sur le contenu individuel.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Rupture de thread | Reviewscontentnotfoundmsg | [Cette révision n&#39;est plus visible](https://d.pr/i/svXs) |
|  | Backtocomments | Retour aux révisions |

## Actions de l&#39;utilisateur {#section_tlx_wj4_xz}

Chaînes disponibles pour les actions de l&#39;utilisateur : marquage, partage et marquage du contenu existant comme utile.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Pied de page de commentaire | Wasreviewhelpful | [Utile ?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | Utile ? |
|  | Ownwasreviewhelpful | [Utile.](https://d.pr/i/Q0mA) |
|  | Reviewwashelp | [Oui](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [&amp; amp ; vert ;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpound | [Non](https://d.pr/i/Q0mA) |
| Modale de vote | Votetitle | Cette révision était-elle utile ? |
|  | Votedownvote | Non |
|  | Votereplytitle | Cette réponse était-elle utile ? |
|  | Votetitle | Ce commentaire était-il utile ? |
|  | Voteupvote | Oui |
| Modale de marquage | Flagtitle | Révision de l&#39;indicateur % s |
|  | Flagsuccessmsg | La révision a été marquée. |
| Indicateur mobile | Flagconfirmationmessage | La révision de l&#39;indicateur % s est-elle comme % s ? |
| Mention modale | Mentiondefaulttext | Je vous ai mentionné dans une révision Livefyre ! |
| Partage modal | Sharetitle | Partager la révision |

## Fonctions de publication {#section_yl1_wj4_xz}

Chaînes disponibles pour les utilisateurs qui publient des révisions.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Editeur | Bodyplaceholder | Ecrire la révision… |
|  | Posteditbutton | Modifier |
|  | Posteditcancelbutton | Annuler |
|  | Postasbutton | Post Review as… |
|  | Postbutton | Post-révision |
|  | Postreplyasbutton | Publier comme… |
|  | Postreplybutton | Publication |
|  | Sharebutton | Partager |
|  | Titleplaceholder | Titre… |

## Erreurs {#section_jbc_vj4_xz}

Chaînes disponibles pour les messages d&#39;erreur généraux.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Erreurs | Erroralreadypost | Vous pouvez uniquement publier une révision. |
|  | Errorautherror | Vous n&#39;êtes pas autorisé à publier une révision sur cette conversation |
|  | Errorcommentsnotallowed | Les révisions ne peuvent pas être publiées pour l&#39;instant |
|  | Errordisestinowncomment | Vous ne pouvez pas aimer votre propre révision |
|  | Errorduplicate | Comme vous avez aimé votre révision, vous n&#39;êtes pas autorisé à la publier deux fois. |
|  | Erroreditduplicate | Vous devez modifier le corps de la révision lorsque vous le modifiez. |
|  | Erroreditnotallowed | Vous n&#39;êtes pas autorisé à modifier les révisions dans cette conversation. |
|  | Erroredittimeexceeded | Désolé, votre période de modification de révision a expiré. |
|  | Errorempty | Il semble que vous essayez de publier une révision vide. |
|  | Erroremptytitle | Il semble que vous essayez de publier un titre vide |
|  | Errorfieldrating | star |
|  | Errorfieldreview | réviser |
|  | Errorfieldtitle | titre |
|  | Errormaxchars | Désolé, votre révision est trop longue. Veuillez modifier et réessayer. |
|  | Errormissingfields | Veuillez saisir un |
|  | Errorratingempty | Vous ne pouvez pas soumettre une évaluation vide |
|  | Errorratingnotset | Toutes les notes doivent être définies. |
|  | Errorratingnotvalid | La note doit être un objet. |
|  | Errorshowmore | Une erreur s&#39;est produite lors du chargement d&#39;autres révisions. |
|  | Errortitlemaxchars | Désolé, votre titre est trop long. Veuillez modifier et réessayer. |
|  | Errorvoteowncomment | Vous ne pouvez pas voter sur votre propre révision |

