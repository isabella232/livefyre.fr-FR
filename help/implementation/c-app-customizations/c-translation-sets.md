---
description: Les visionneuses de traduction permettent de spécifier une autre langue
  pour les applications.
seo-description: Les visionneuses de traduction permettent de spécifier une autre
  langue pour les applications.
seo-title: Visionneuses de traduction
solution: Experience Manager
title: Visionneuses de traduction
uuid: 8 ba 66 a 61-5520-482 a-bc 0 b-e 4 f 6 b 57 f 1744
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Visionneuses de traduction {#translation-sets}

Les visionneuses de traduction permettent de spécifier une autre langue pour les applications.

<!-- 
c_translation_sets.dita
-->

Utilisez les paramètres de traduction pour localiser les applications dans différentes langues ou pour spécifier du texte alternatif pour plusieurs applications depuis un emplacement dans Studio. Par exemple, vous pouvez vous assurer que tous les sites en espagnol utilisent le langage espagnol pour tous les champs d'application. Vous pouvez également modifier le texte afin que tous les champs correspondent à la voix et à l'aspect de votre site ou réseau.

Vous pouvez spécifier les paramètres de traduction pour toutes les applications, à l'exception de Storify 2. Pour plus d'informations sur les champs que vous pouvez localiser, voir [Localisation des chaînes](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Commentaires, Blog en direct et Chat partagent le même ensemble de chaînes dans un jeu de traduction.

Spécifiez un jeu de traduction pour un réseau, un site, une application ou à l'aide d'une API.

Les visionneuses de traduction à différents niveaux sont remplacées par les autres suivantes :

* Le jeu de traduction d'API remplace tous les jeux de traduction à tout niveau (application, réseau et site)
* Le jeu de traduction de l'application remplace les visionneuses de traduction au niveau réseau et au niveau du site.
* Les jeux de traduction au niveau du site remplacent les visionneuses de traduction au niveau du réseau.

## Révision des chaînes de texte {#c-review-text-strings}

Personnalisation des chaînes de texte pour les révisions Livefyre.

Cette page répertorie et décrit les chaînes disponibles pour la personnalisation dans les applications de révision. Les chaînes répertoriées ici s'ajoutent aux chaînes par défaut des applications Livefyre, répertoriées dans la section Personnalisations de chaînes. Lorsque des doublons sont répertoriés, les chaînes répertoriées dans ces tableaux sont les valeurs par défaut pour les applications de révision.

* Implémentation
* Interface de révision/évaluation
* Informations de diffusion en continu
* Informations Auteur/Contenu
* Actions de l'utilisateur
* Fonctions de publication
* Erreurs

## Implémentation {#section-vsy-1k4-xz}

Pour mettre en œuvre cette fonction, transmettez un mappage d'objet 1-1 des chaînes que vous souhaitez remplacer par l'objet de configuration Javascript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

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

Chaînes disponibles pour l'interface utilisateur de révision et de notation.

| Elément | Clé | Texte par défaut |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Boutons |  |  |
|  | Editreviewbtn | Modifier la révision |
|  | Reviewbtn | Révision de la révision |
|  | Reviewsclosed | Révisions fermées |
|  | Showreviewbtn | Afficher la révision |
|  | suivre | Je suis intéressé |
|  | Sharetext | Je viens de rédiger une révision. Vérifiez-la ! |
| Info-bulles |  |  |
|  | Ratingvalues | Un tableau. Par défaut =['Poor ','Poor ','Fair ','Fair ','Average ','Average ','Good ','Good ','Excellent ';'Excellent ']; |
|  |  | Remarque : Les valeurs du tableau doivent être dupliquées pour affecter à la fois la moitié gauche et la moitié droite de chaque étoile au même nom. |
| Sous-parties de notation |  |  |
|  | Ratingsubpartplaceholder | Un tableau. Par défaut =[] |
|  | Ratingsubparttitles | Un tableau. Par défaut =[] |
|  | Reviewstreamtitle | Vide par défaut. Titre de la section résumé de la révision. |
| Misc |  |  |
|  | Averagerating | Évaluation moyenne des utilisateurs |
|  | Breakdownheader | Ventilation d'évaluation |
|  | utile | % s sur % s trouvé |
|  | Helpfulplural | % s sur % s trouvé |
|  | out of | / |
|  | Ratingtype | star |

## Informations de diffusion en continu {#section_wmv_yj4_xz}

Chaînes disponibles pour les informations de flux de contenu et affichées.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Tri* |  |  |
|  | Sortby | *Vide par défaut.* |
|  | Sorthighestrated | [Évaluation la plus élevée](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Note la plus faible](https://d.pr/i/huTd) |
|  | Sortmosthelpound | [Plus efficace](https://d.pr/i/huTd) |
| *Stream misc.* |  |  |
|  | Showmore | Montrer plus |
| *Vélocité élevée du flux* |  |  |
|  | Newcomment | Nouvelle révision |
|  | Newcomments | Nouvelles révisions |
| *Nombre d'écouteurs* |  |  |
|  | Listenercount | personne qui écoute |
|  | Listenercountplural | personne qui écoute |
| *Nombre de commentaires* |  |  |
|  | Commentcountlabel | Livereviews |
|  | Commentcountlabelplural | Livereviews |
| *Nombre de notifications de commentaire* |  |  |
|  | Commentnotification | Nouvelle révision |
|  | Commentnotifierplural | Nouvelles révisions |

## Informations Auteur/Contenu {#section_osx_xj4_xz}

Stings disponibles pour l'auteur et les informations sur le contenu individuel.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Rupture de thread* |  |  |
|  | Reviewscontentnotfoundmsg | [Cette révision n'est plus visible](https://d.pr/i/svXs) |
|  | Backtocomments | Retour aux révisions |

## Actions de l'utilisateur {#section_tlx_wj4_xz}

Chaînes disponibles pour les actions de l'utilisateur : marquage, partage et marquage du contenu existant comme utile.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Pied de page de commentaire* |  |  |
|  | Wasreviewhelpful | [Utile ?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | Utile ? |
|  | Ownwasreviewhelpful | [Utile.](https://d.pr/i/Q0mA) |
|  | Reviewwashelp | [Oui](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp ; vert ;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpound | [Non](https://d.pr/i/Q0mA) |
| *Modale de vote* |  |  |
|  | Votetitle | Cette révision était-elle utile ? |
|  | Votedownvote | Non |
|  | Votereplytitle | Cette réponse était-elle utile ? |
|  | Votetitle | Ce commentaire était-il utile ? |
|  | Voteupvote | Oui |
| *Modale de marquage* |  |  |
|  | Flagtitle | Révision de l'indicateur % s |
|  | Flagsuccessmsg | La révision a été marquée. |
| *Indicateur mobile* |  |  |
|  | Flagconfirmationmessage | La révision de l'indicateur % s est-elle comme % s ? |
| *Mention modale* |  |  |
|  | Mentiondefaulttext | Je vous ai mentionné dans une révision Livefyre ! |
| *Partage modal* |  |  |
|  | Sharetitle | Partager la révision |

## Fonctions de publication {#section_yl1_wj4_xz}

Chaînes disponibles pour les utilisateurs qui publient des révisions.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Editeur* |  |  |
|  | Bodyplaceholder | Ecrire la révision… |
|  | Posteditbutton | Modifier |
|  | Posteditcancelbutton | Annuler |
|  | Postasbutton | Post Review as… |
|  | Postbutton | Post-révision |
|  | Postreplyasbutton | Publier comme… |
|  | Postreplybutton | Publication |
|  | Sharebutton | Partager |
|  | Titleplaceholder | Titre… |

## Erreurs {#section_jbc_vj4_xz}

Chaînes disponibles pour les messages d'erreur généraux.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Erreurs |  |  |
|  | Erroralreadypost | Vous pouvez uniquement publier une révision. |
|  | Errorautherror | Vous n'êtes pas autorisé à publier une révision sur cette conversation |
|  | Errorcommentsnotallowed | Les révisions ne peuvent pas être publiées pour l'instant |
|  | Errordisestinowncomment | Vous ne pouvez pas aimer votre propre révision |
|  | Errorduplicate | Comme vous avez aimé votre révision, vous n'êtes pas autorisé à la publier deux fois. |
|  | Erroreditduplicate | Vous devez modifier le corps de la révision lorsque vous le modifiez. |
|  | Erroreditnotallowed | Vous n'êtes pas autorisé à modifier les révisions dans cette conversation. |
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
|  | Errorshowmore | Une erreur s'est produite lors du chargement d'autres révisions. |
|  | Errortitlemaxchars | Désolé, votre titre est trop long. Veuillez modifier et réessayer. |
|  | Errorvoteowncomment | Vous ne pouvez pas voter sur votre propre révision |

## Chaînes de texte avec lettres {#c_sidenotes_text_strings}

Personnalisation des chaînes de texte pour les courriers électroniques Livefyre

<!-- 

c_sidenotes_text_strings.dita

 -->

Cette page répertorie et décrit toutes les chaînes disponibles pour la personnalisation dans les applications de commentaires annexes. Pour plus d'informations sur les chaînes disponibles pour les applications Livefyre principales, reportez-vous à la page Personnalisations de chaînes.

* Implémentation
* Authentique
* Informations de diffusion en continu
* Informations Auteur/Contenu
* Actions de l'utilisateur
* Fonctions de publication
* Interface du modérateur
* Erreurs

## Implémentation {#section_wp2_ql4_xz}

Pour mettre en œuvre cette fonction, transmettez un mappage d'objet 1-1 des chaînes que vous souhaitez remplacer par l'objet de configuration Javascript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

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

Chaînes disponibles pour le processus d'authentification et à partir des menus d'utilisateurs authentifiés.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Chaînes de menu authentiques* |  |  |
|  | Menuauthsigninbtn | Connexion |
|  | Menuauthsignedinmsg | Vous devez être connecté à {action} |
|  | Menuusereditprofile | Modifier le profil |
|  | Menuuseradmin | Console d'administration |
|  | Menuuserlogout | Déconnexion |
|  | Menuuserbackbtn | Tout |

## Informations de diffusion en continu {#section_wpy_gl4_xz}

Chaînes disponibles pour les informations de flux de contenu et affichées.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Options du menu Informations* |  |  |
|  | Menuinfocopyright | © Livefyre, Inc. 2014 |
|  | Menuinfohelp | Aide |
|  | Menuinfolivefyrelink | Visitez Livefyre.com |

## Informations Auteur/Contenu {#section_dhb_gl4_xz}

Stings disponibles pour l'auteur et les informations sur le contenu individuel.

| Elément | Clé | Texte par défaut |
|---|---|---|
|  | Commentmoderatortag | Mod |
|  | Commentpendingtag | En attente |
|  | Commentreadmorelink | En savoir plus |
|  | Commentreplylink | Voir {number} réponses |
|  | Commentreplylinksing | Voir la réponse |
|  | Commentvotecount | votes |
|  | Commentvotecountsing | voter |
|  | Datetimeminuteprefix | m |
|  | Datetimemonths | * Un tableau. Par défaut = *[ 'janvier ','février ','mars ','avril ','mai ','juin ','juillet ','août ','septembre ','octobre ','novembre ','décembre ' ] |
|  | Questiondescription | Vous pouvez désormais lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets. <br>Mettez en surbrillance le texte et cliquez sur l'icône ou cliquez sur l'icône à la fin de chaque paragraphe. |
|  | Questionmocktext | Ce qui est connu « connu connu » n'est pas connu, c'est qu'il est « familier ». |
|  | Questiontitle | Qu'est-ce qu'une illustration ? |

## Actions de l'utilisateur {#section_qxd_fl4_xz}

Chaînes disponibles pour les actions de l'utilisateur : marquage, partage et aimer le contenu existant.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Options du menu Réponse* |  |  |
|  | Menucylinesviewtitle | Détails |
|  | Menucylinesviewreply | Répondre à la conversation |
| *Options du menu Partager* |  |  |
|  | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Partager |
| *Options du menu Indicateur* |  |  |
|  | Menuflagoptionapprove | Refuser |
|  | Menuflagoptionoffensive | Offensif |
|  | Menuflagoptionofftopic | Rubrique désactivée |
|  | Menuflagoptionspam | Indésirable |
|  | Menuflagtitle | Marquer comme… |
|  | Facebooksharecaption | Indique le titre sur « {title} » |
| *Options utilisateur mobiles* |  |  |
|  | Slidercommenttally | of |
|  | Sliderinviteread | Read |
|  | Sliderinvitewrite | Écrire |
|  | Sliderloading | Chargement en cours… |
|  | Sliderwritetext | Que pensez-vous ? Appuyez sur pour écrire. |

## Fonctions de publication {#section_xzf_2l4_xz}

Chaînes disponibles pour les utilisateurs qui publient du contenu.

| Elément | Clé | Texte par défaut |
|---|---|---|
|  | Editoreditbtn | Enregistrer |
|  | Editoreditpublication | Enregistrement en cours… |
|  | Editoreditreplytitle | Modifier la réponse |
|  | Editoredittitle | Modifier le fichier sidenote |
|  | Editorplaceholder | Que pensez-vous ? |
|  | Editorpostbtn | Caractère sidenote de publication |
|  | Editorpostbtnmobile | Publication |
|  | Editorpublication | Publication… |
|  | Editorreplybtn | Post-réponse |
|  | Editorreplytitle | Ecrire une réponse |
|  | Editortitle | Écrire un caractère sidenote |
|  | Emptyimageblocktxt | Que pensez-vous ? |
|  | Emptytextblocktxt | + |
|  | Replybtn | Répondre |
|  | Threadreplybtn | Répondre à la conversation |
| *Options du menu Supprimer* |  |  |
|  | Menuconfirmaccept | Oui, {action} |
|  | Menuconfirmcancel | Annuler |
|  | Menuconfirmtitle | Êtes-vous sûr ? |
| *Options du menu etc* |  |  |
|  | Menuetcoptionapprove | Approuver |
|  | Menuetcoptiondelete | Supprimer |
|  | Menuetcoptionedit | Modifier |
|  | Menuetcoptionflag | Indicateur |
|  | Menuetcoptionshare | Partager |
|  | Menuetcpostedat | Publié le {date} |
|  | Menuetctitle | Plus |

## Interface du modérateur {#section_o5f_dl4_xz}

Chaînes disponibles pour l'interface du modérateur authentifié par l'utilisateur.

| Elément | Clé | Texte par défaut |
|---|---|---|
| *Messages de confirmation du menu Plus* |  |  |
|  | Notificationapprouvé | Approuvé |
|  | Notificationdeleted | Supprimé |
|  | Notificationflagged | Marqué |

## Erreurs {#section_gtk_cl4_xz}

Chaînes disponibles pour les messages d'erreur généraux.

| Elément | Clé | Texte par défaut |
|---|---|---|
|  | Errorconnection | Uh-oh. Vous ne semblez pas avoir une bonne connexion. |
|  | Errorduplicate | Vous aimez également votre remarque, mais vous ne pouvez pas la publier deux fois. |
|  | Errorgenated | Une erreur est survenue. Veuillez réessayer. |
|  | Errorserver | Un problème est survenu avec notre serveur. Essayez-le de nouveau ? |
