---
description: Personnalisation des chaînes des applications Livefyre.
seo-description: Personnalisation des chaînes des applications Livefyre.
seo-title: Localiser les chaînes
solution: Experience Manager
title: Localiser les chaînes
uuid: c 0 ab 352 d -5 d 3 a -45 d 7-bbd 0-aed 165835646
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Localiser les chaînes{#localize-strings}

Personnalisation des chaînes des applications Livefyre.

Les chaînes de texte de la plupart des éléments HTML d'une application Livefyre peuvent être personnalisées. Cela permet de modifier le texte des éléments HTML rendus, tels que le bouton « Publier sous », le texte « Nombre de commentaires » ou le bouton « Se connecter », à n'importe quelle chaîne UTF -8 valide. Utilisez cette fonctionnalité pour ajouter une personnalité à votre implémentation du flux ou pour localiser la langue de l'application pour votre base d'utilisateurs.

* Commentaires, conversation et blog en direct

   * [Implémentation](#c-localize-strings/section_im4_224_xz)
   * [Accès au compte](#c-localize-strings/section_cm3_d24_xz)
   * [Informations de diffusion en continu](#c-localize-strings/section_wx1_c24_xz)
   * [Tri du flux](#c-localize-strings/section_ih2_124_xz)
   * [Informations sur le contenu](#c-localize-strings/section_llv_yd4_xz)
   * [Contenu incitatif](#c-localize-strings/section_gmw_vd4_xz)
   * [Editeur de texte](#c-localize-strings/section_ky5_td4_xz)
   * [Options de réponse](#c-localize-strings/section_zvt_qd4_xz)
   * [Notification de commentaire](#c-localize-strings/section_qqt_pd4_xz)
   * [Messages d'erreur](#c-localize-strings/section_omz_jxn_xz)

* [Format de date et de date](#c-localize-strings/section_yz4_g5n_xz)
* [Mur multimédia](#c-localize-strings/section_vwt_d5n_xz)
* [Carte](#c-localize-strings/section_fxv_c5n_xz)
* [Mosaic](#c-localize-strings/section_e2s_b5n_xz)
* [Carrousel](#c-localize-strings/section_l2z_hkn_xz)
* [Carte de fonctionnalités](#c-localize-strings/section_mw2_hkn_xz)
* [Sondage](#c-localize-strings/section_pdg_fwh_xz)
* [Identité Livefyre](#c-localize-strings/section_zc3_xvh_xz)
* Plus:
   * [Révision des chaînes de texte](/help/using/c-settings-other/c-translation-sets/c-review-text-strings.md#c_review_text_strings)
   * [Commentaires de sidenotes](/help/using/c-settings-other/c-translation-sets/c-sidenotes-text-strings.md#c_sidenotes_text_strings)

## Implémentation {#section_im4_224_xz}

Pour mettre en œuvre cette fonctionnalité, transmettez un mappage d'objet 1-1 des chaînes que vous souhaitez remplacer par l'objet de configuration JavaScript. Si vous ne fournissez pas de champ, le texte par défaut est utilisé.

Exemple :

```
var customStrings = {     
   postAsButton: "New Post As Text",     
   postEditButton: "New Post Edit Text"  
};   
   convConfig["strings"] = customStrings; fyre.conv.load(     
   networkConfig,     
   [convConfig],     
   function(){}  
);
```

Cette page répertorie toutes les chaînes de texte qui peuvent être personnalisées pour les applications de base Livefyre.

## Accès au compte {#section_cm3_d24_xz}

Chaînes disponibles pour le processus d'authentification et à partir des menus d'utilisateurs authentifiés.

![](assets/strings_threadheader-150x40.png)

| Elément | Clé | Texte par défaut |
|---|---|---|
|  | Displayname | % s |
|  | Editprofile | Modifier le profil |
|  | Notificationsettings | Paramètres de notification |
|  | Siteadmin | Console d'administration (liens vers Studio) |
|  | Signout | Déconnexion |

## Informations de diffusion en continu {#section_wx1_c24_xz}

Chaînes disponibles pour les informations de flux de contenu et affichées. Indique le nombre de personnes qui écoutent, le nombre de publications à l'application et permet aux utilisateurs de se connecter ou d'accéder aux informations de leur compte.

| Clé | Texte par défaut | Données de flux |
|---|---|---|
|  | Commentcountlabelzero | Commentaire % s |
|  | Commentcountlabel | Commentaire % s |
|  | Commentcountlabelplural | Commentaires % s |
|  | Listenercount | personne qui écoute |
|  | Listenercountplural | personne qui écoute |
|  | Liveblogpostcountlabelzero | publication |
|  | Liveblogpostcountlabel | publication |
|  | Liveblogpostcountlabelplural | publications |
| Options de thread | Threadbreakoutbutton | Afficher tout le thread |
|  | Togglecollapse | Basculer vers la fin |
| Commentaires à forte vélocité/mise en file d'attente | actualiser | Actualiser |
|  | Newcomment | Nouveau commentaire |
|  | Newcomments | Nouveaux commentaires |
|  | Newreply | nouvelle réponse |
|  | Newanswers | nouvelles réponses |

## Tri du flux {#section_ih2_124_xz}

Permet de trier le contenu renvoyé par âge ou par popularité.

![](assets/strings_newestoldesttop-1-150x56.png)

| Clé | Texte par défaut | Options d'en-tête |
|---|---|---|
|  | Sortnewest | Plus récent |
|  | Sortoldest | Le plus ancien |
|  | Sorttopcomments | Principaux commentaires |
|  | Sorthotthreads | Threads logiciels |
|  | Sortseparator |  |  |
|  | Streamsorting | Chargement |
|  | Topcommentscontentnotfoundmsg | Il n'y a pas encore assez de mentions J'aime. |
|  | Hotthreadscontentnotfoundmsg | Il n'y a pas encore suffisamment de threads. |
|  | Streamrefreshmsg | Découvrez les nouveautés. |
| Options de pied de page | Archiveheadertitle | Depuis l'archive |
|  | Archiveshowmore | Montrer plus |
|  | Showmore | Afficher plus de commentaires |
|  | Showmoreliveblog | Afficher plus de publications |

![](assets/strings_threadend-150x47.png)

## Informations sur le contenu {#section_llv_yd4_xz}

Répertorie les informations sur la publication : nom d'utilisateur, balises utilisateur appliquées et heure de publication.

![](assets/strings_authorinfo-150x52.png)  ![](assets/strings_posttime-150x45.png)

| Clé | Texte par défaut | Auteur |
|---|---|---|
|  | modérateur | modérateur |
|  | Hovercardviewprofile | Afficher le profil complet |
| Informations sur la publication | Timejustnow | just |
|  | Timeminutesago | minute auparavant |
|  | Timeminutesagoplural | minutes auparavant |
|  | Timehoursago | heure auparavant |
|  | Timehoursagoplural | heure auparavant |
|  | Timedaysago | jour auparavant |
|  | Timedaysagoplural | jours auparavant |
|  | Likesplural | Mentions J'aime |
|  | Likessingular | Aimer |
|  | Moderatoredittimestamp | Modifié par un modérateur |
|  | Commenttombstone | Ce commentaire a été supprimé. |
|  | Permalinknotfoundmsg | Ce commentaire n'est plus visible. |
|  | Quickprofiletooltip | Profil rapide |

## Contenu incitatif {#section_gmw_vd4_xz}

S'il est activé, le contenu incitatif est répertorié en haut du flux.

|  | Clé | Texte par défaut |
|---|---|---|
| Libellés présentés |  |  |
| ![](assets/strings_featuredcontent-150x40.png) | Featuredcommentstag | Proposé |
|  | Featuredcommentstitleplural | Commentaires présentés |

## Editeur de texte {#section_ky5_td4_xz}

Par défaut, disponible en haut de la page pour tous les utilisateurs.

![](assets/strings_texteditor-1-150x77.png)

|  | Clé | Texte par défaut |
|---|---|---| 
| Boutons Editeur | suivre | + Suivre |
|  | ne pas suivre | - Ne pas suivre |
|  | Liveblogfollow | Suivre le blog en direct |
|  | Liveblogunfollow | Ne pas suivre le blog en direct |
|  | Postbutton (disponible pour les utilisateurs connectés.) | Commentaire Publication |
|  | Postasbutton (disponible pour les utilisateurs non authentifiés.) | Publier le commentaire sous… |
|  | Posteditbutton | Modifier un commentaire |
|  | Posteditasbutton | Modifier le commentaire sous… |
|  | Posteditcancelbutton | Annuler |
|  | Editordisabled | Cette conversation est actuellement clôturée pour les nouveaux commentaires. |
| Options de messagerie instantanée | Livechatpostbuttonlabel | Publication |
|  | Livechatposteditbutton | Modifier |
|  | Livechatwindowsinstruction | Appuyez sur Ctrl + entrée pour publier |
|  | Livechatotherinstruction | Appuyez sur Commande + entrée pour publier |

## Options de réponse {#section_zvt_qd4_xz}

Sauf indication contraire, disponible pour tous les utilisateurs connectés. Placez le pointeur de la souris sur un panneau de contenu pour accéder à.

![](assets/strings_banusermodal-150x36.png)

| Clé | Texte par défaut |  |
|---|---|---|
| Options de réponse utilisateur | Disponible pour fin - utilisateurs. |  |
| Flagbutton | Indicateur |
|  | Flagcommenttooltip | Indicateur |
|  | Editbutton (disponible uniquement pour les auteurs et les modérateurs, s'ils sont activés.) | Modifier |
|  | Deletebutton (disponible uniquement pour les auteurs et les modérateurs, s'ils sont activés.) | Supprimer |
|  | Deletecommenttooltip | Supprimer |
|  | Sharebutton | Partager |
|  | Sharecommenttooltip | Partager |
|  | Likebutton | Aimer |
|  | Unlikebutton | Contrairement à |
|  | Replybutton | Répondre |
|  | Replybuttonsingular (disponible pour Chat et Live Blog.) | Répondre |
|  | Replybuttonplural (disponible pour Chat et Live Blog.) | Réponses |

![](assets/strings_responseoptions-150x35.png)

| Clé | Texte par défaut |  |
|---|---|---|
| Modal modal | Flagtitle | Commentaire de l'indicateur % s |
|  | Flagsubtitle | Marquer comme |
|  | Flagdefaultselectoption | Sélectionner |
|  | Flagspam | Indésirable |
|  | Flagspambutton | Indésirable |
|  | Flagspamcommenttooltip | Indésirable |
|  | Flagoffensive | Offensif |
|  | Flagoffensivebutton | Offensif |
|  | Flagoffensivecommenttooltip | Offensif |
|  | Flagapprove | Refuser |
|  | Flagdisagreebutton | Refuser |
|  | Flagdisagreecommenttooltip | Refuser |
|  | Flagofftopic | Rubrique désactivée |
|  | Flagofftopicbutton | Rubrique désactivée |
|  | Flagofftopiccommenttooltip | Rubrique désactivée |
|  | Flagemail | Courriel |
|  | Flagemailplaceholder | you@example.com |
|  | Flagnotes | Remarques |
|  | Flagnotesplaceholder | Commencez à saisir ici… |
|  | Flagconfirmbutton | OK |
|  | Flagcancelbutton | Annuler |
|  | Flagconfirmationmessage | Signaler le commentaire % s comme % s ? |
|  | Flagsuccessmsg | Le commentaire a été marqué. |

![](assets/strings_flagmodal-150x87.png)

| Clé | Texte par défaut |  |
|---|---|---|
| Partager le modal | Sharetitle | Partager le commentaire |
|  | Shareplaceholdertext | Que pensez-vous ? |
|  | Sharelabel | Partager le : |
|  | Sharetexttwitter | blank |
|  | Sharetextfacebook | blank |
|  | Sharetextlinkedin | blank |
|  | Sharebuttontext | Partager |
|  | Sharepermalink | Permalink |
|  | Loadingpermalink | Chargement de l'URL courte… |
|  | Sharetext | Je viens de publier un commentaire. Vérifiez-la ! |

![](assets/strings_sharemodal-150x59.png)

| Clé | Texte par défaut |  |
|---|---|---|
| Modale de réponse | Postreplyasbutton | Publier le commentaire sous… |
|  | Postreplybutton (disponible pour les utilisateurs connectés.) | Commentaire Publication |
|  | Backtohotthreads | Retour aux threads chauds |

![](assets/strings_backto-150x48.png)

| Clé | Texte par défaut |  |
|---|---|---|
| @ mention @ mentions Twitter | Mentiontitle | Mention de partage |
|  | Mentionsubtitletwitter | Partager le tweet sur : |
|  | Mentiondefaulttext | Je vous ai mentionné dans un commentaire Livefyre ! |
|  | Mentionconfirmbutton | OK |
|  | Mentioncancelbutton | Annuler |
|  | Mentionerrorgenated | Oops ! Une erreur est survenue ! Livefyre a été alerté. |
|  | Mentionerrornoneselected | Au moins une mention doit être activée. |
|  | Mentionmenutitle | Pour afficher et mentionner vos amis |
|  | Mentiontwitterconnect | Connexion à Twitter |
|  | Mentiontwitterfetching | Récupération des amis… |
|  | Mentionsuccessmsg | Les mentions ont bien été envoyées. |

![](assets/strings_sharemention-150x60.png)

| Clé | Texte par défaut |  |
|---|---|---|
| Modifier le modal | Disponible pour les administrateurs Studio, les gestionnaires d'utilisateurs ou les modérateurs |  |
| @ (@ mention.) | </> (Ouvre la fenêtre HTML personnalisée.) |  |
|  | Customhtmldialogtitle (s'affiche comme en-tête du modal.) | Ajout de code HTML personnalisé |

![](assets/strings_moderatoreditmodal-150x49.png)

| Clé | Texte par défaut |  |
|---|---|---|
| Options de réponse du modérateur | Disponible pour les administrateurs Studio, les gestionnaires d'utilisateurs ou les modérateurs. |  |
| Pendingcomment | en attente |
|  | Banuserbutton | Interdire l'utilisateur |
|  | Banusertooltip | Interdire l'utilisateur |
|  | Bozobutton | Bozo |
|  | Bozocommenttooltip | Bozo |
|  | Featurebutton | Fonction |
|  | Featurecommenttooltip | Fonction |
|  | Unfeaturebutton | Unfeature |
|  | Featuredcommenttooltip | Unfeature |

![](assets/strings_adminoptions-150x33.png)

| Clé | Texte par défaut |  |
|---|---|---|
| Configuration modale de l'utilisateur | Disponible pour les administrateurs Studio, les gestionnaires d'utilisateurs ou les modérateurs. |  |
| Bantitle | Interdire l'utilisateur |  |
|  | Banane | Souhaitez-vous vraiment interdire cet utilisateur ? |
|  | Banconfirmbutton | OK |
|  | Bancancelbutton | Annuler |

## Notification de commentaire {#section_qqt_pd4_xz}

Si activé, disponible au bas de la page pour toutes les applications de conversation Livefyre.

![](assets/strings_notifier-150x112.png)

|  | Clé | Texte par défaut |
|---|---|---|
| Étiquettes de notifications | Commentnotification | Nouveau commentaire |
|  | Commentnotifierplural | Nouveaux commentaires |
|  | Liveblognotification | Nouvelle publication |
|  | Liveblognotifierplural | Nouvelles publications |

## Messages d'erreur {#section_omz_jxn_xz}

Chaînes disponibles pour les messages d'erreur personnalisables.

| Clé | Texte par défaut |
|---|---|
| Errorautherror | Vous n'êtes pas autorisé à publier un commentaire sur cette conversation |
| Errorcommentsnotallowed | Les commentaires ne sont pas autorisés dans cette conversation |
| Errordefault | Une erreur est survenue. Veuillez réessayer. |
| Errorduplicate | Comme vous avez aimé votre commentaire, vous n'êtes pas autorisé à le publier deux fois. |
| Erroreditduplicate | Vous devez modifier le corps du commentaire lorsque vous le modifiez. |
| Erroreditnotallowed | Vous n'êtes pas autorisé à modifier les commentaires de cette conversation. |
| Erroredittimeexceeded | Désolé, votre période de modification des commentaires a expiré. |
| Errorempty | Il semble que vous essayiez de publier un commentaire vide. |
| Errorexpired | Votre session a expiré. Veuillez recharger la page. |
| Errorflagnotselected | Veuillez sélectionner un type de marqueur. |
| Errorguestamed | Désolé, seuls ceux qui possèdent des comptes peuvent aimer le contenu. |
| Errorinsufficientpermissions | Autorisations insuffisantes |
| Errorinvalidchar | Il semble que vous essayiez de publier un caractère non valide. |
| Errorlikeowncomment | Vous ne pouvez pas aimer votre propre commentaire |
| Errormalformed | Il semble que vous essayez de publier du contenu mal formé. |
| Errormaxchars | Désolé, votre commentaire est trop long. Veuillez modifier et réessayer. |
| Errormedianotavailable | Le média n'est plus visible. |
| Errorshowmore | Une erreur s'est produite lors du chargement d'autres commentaires. |
| Multiplemedianotallowederror | Vos autorisations ne vous donnent qu'une pièce jointe multimédia à la fois. |

## Format de date et de date {#section_yz4_g5n_xz}

Traduisez et personnalisez la manière dont les dates s'affichent sur les cartes de contenu dans les applications de visualisation.

| Clé | Texte par défaut |
|---|---|
| Hoursago | {number} h |
| Hoursagosingular | {number} h |
| Justnow | 1s |
| Minutesago | {number} m |
| Minutesagosingular | {number} m |
| Monthdayformat | {day} {monthabbrev} |
| Monthdayyearformat | {day} {monthabbrev} {year} |
| Monthnames | Janvier, Février, Mars, Avril, Mai, Juin, Juillet, Août, Septembre, Octobre, Novembre, Décembre |
| Monthnamesabbrev | Jan, Fév, Mar, Apr, May, May, Jun, Aug, Sep, Oct, Nov, Dec |
| Secondsago | {number} s |
| Secondsagosingular | {number} s |

## Mur multimédia {#section_vwt_d5n_xz}

Chaînes disponibles pour l'application Mur multimédia.

| Clé | Texte par défaut |
|---|---|
| Featuredtext | Proposé |
| Sharebuttontext | Partager |

| Clé | Texte par défaut |
|---|---|
| Postbuttontext | Qu'est-ce que vous pensez ? |
| Postmodaltitle | Publier votre commentaire |
| Postmodalbutton | Publier votre commentaire |
| Postmodalplaceholder | Que souhaitez-vous dire ? |
| Showmorebuttontext | Charger plus |
| Sharebuttontext | Partager |

## Carte {#section_fxv_c5n_xz}

Chaînes disponibles pour les cartes.

| Clé | Texte par défaut |
|---|---|
| Featuredtext | Proposé |
| Sharebuttontext | Partager |

## Mosaic {#section_e2s_b5n_xz}

Chaînes disponibles pour Mosaics.

| Clé | Texte par défaut |
|---|---|
| Featuredtext | Proposé |
| Sharebuttontext | Partager |

## Carrousel {#section_l2z_hkn_xz}

Chaînes disponibles pour Carousel.

| Clé | Texte par défaut |
|---|---|
| Featuredtext | Proposé |
| Sharebuttontext | Partager |

## Carte de fonctionnalités {#section_mw2_hkn_xz}

Chaînes disponibles pour la carte de fonctionnalités.

| Clé | Texte par défaut |
|---|---|
| Featuredtext | Proposé |
| Sharebuttontext | Partager |

## Télécharger une application {#section_grc_gkn_xz}

Chaînes disponibles pour l'application de téléchargement.

| Clé | Texte par défaut |
|---|---|
| Postbuttontext | Qu'est-ce que vous pensez ? |
| Postmodaltitle | Publier votre commentaire |
| Postmodalbutton | Publier votre commentaire |
| Postmodaltitleplaceholder | Saisie d'un titre |
| Postmodalplaceholder | Que souhaitez-vous dire ? |
| Postmodalconfirmationtitle | Merci d'avoir publié ! |
| Postmodalconfirmationmessage | Votre publication est en cours de révision. |
| Postmodalconfirmationbutton | Terminé |
| titre |  |
| message |  |
| Editorerrorattachmentsrequired | Une pièce jointe est requise |
| Editorerrorbody | Ajoutez un message. |
| Editorerrorduplicate | Comme vous le souhaitez, vous ne pouvez pas le publier deux fois |
| Editorerrorgeneric | Une erreur s'est produite |
| Editorerrortitlerequired | Un titre est requis |

## Sondage {#section_pdg_fwh_xz}

Chaînes disponibles pour les sondages.

| Clé | Texte par défaut |
|---|---|
| Totalvoteslabel | % s votes au total |
| Sharestringtext | Je viens de voter sur % squel est votre vote ? |
| Pollclosedlabel | Ce sondage est actuellement fermé. |

## Identité Livefyre {#section_zc3_xvh_xz}

Chaînes disponibles pour Livefyre Identité.

| Clé | Texte par défaut |
|--- |--- |
| Automaticallyfollowconversations | Suivez automatiquement les conversations que je joins |
| back | Retour |
| biographie | Biographie |
| créer | Créer |
| Createanewaccount | Créer un compte |
| Createnewaccountwithemail | Création d'un compte avec courrier électronique |
| Changeavatar | Change Avatar |
| Choosefile | Choisir un fichier |
| Completeaccount | Compte complet |
| Emailwhensomeonereplies | Courriel lorsque quelqu'un répond à moi |
| Emailcommentsifollow | Commentaires par courriel dans les conversations que j'ai suivies |
| Emailsenttoresetpassword | Courriel envoyé ! Cochez la case correspondant à un lien pour réinitialiser votre mot de passe. |
| Emailverificationsent | Vérification de courrier électronique envoyée |
| Firstname | Prénom |
| Forgotpassword | Mot de passe oublié ? |
| Forgotyourpassword | Vous avez oublié votre mot de passe ? |
| Forgotyourpasswordinstructions | Entrez votre nom d'utilisateur ou votre adresse électronique ci-dessous, et nous vous enverrons un lien pour modifier votre mot de passe. |
| Forminputclosebuttontext | Fermer |
| Forminputcancelbuttontext | Annuler |
| Forminputsavebuttontext | Enregistrer |
| Hasnotleftanycomments | n'a laissé aucun commentaire |
| Locationisfrom | provient de |
| Labelavatar | Avatar |
| Labelcomments | Commentaires |
| Labelconfirmnewpassword | Confirmer le nouveau mot de passe |
| Labelconfirmpassword | Confirmer le mot de passe |
| Labelemail | Adresse électronique |
| Labellikes | Mentions J'aime |
| Labelloading | Chargement |
| Labelnewpassword | Nouveau mot de passe |
| Labelnotification | Notifications |
| Labelpassword | Mot de passe |
| Labelprofile | Profil |
| Labelusername | Nom d'utilisateur |
| Labelusernameoremail | Nom d'utilisateur ou courriel |
| Lastname | Nom |
| Livefyreaccount | Compte Livefyre |
| emplacement | Emplacement |
| Loadingprofile | Chargement du profil |
| Newpassword | Nouveau mot de passe |
| Oldpassword | Ancien mot de passe |
| on | on |
| ou | ou |
| Passwordlinkexpired | Le lien sur lequel vous avez cliqué pour réinitialiser votre mot de passe a expiré. Réinitialisez votre mot de passe et nous vous enverrons un nouveau lien. |
| Pleasecheckemailtocomplete | Veuillez vérifier votre adresse électronique pour terminer votre enregistrement. |
| publié | Publié |
| Poweredby | optimisé par |
| Profilenotificationimmediate | immediate |
| Profilenotificationhourly | horaire |
| Profilenotificationnever | jamais |
| Recentcomments | Commentaires récents |
| réinitialiser | Réinitialiser |
| Resetpassword | Réinitialiser le mot de passe |
| Signin | Connexion |
| Signinwith | Connexion avec |
| Signinwithemail | Connexion avec courrier électronique |
| Signup | Inscription |
| Socialaccount | Compte social |
| Successpasswordchanged | Réussite ! Votre mot de passe a été modifié et vous êtes maintenant connecté. |
| Termsandconditions | Conditions générales |
| Termsandconditionsintro | En vous inscrivant à la page |
| Termsofuse | Conditions d'utilisation |
| Termsofuseintro | En vous connectant, vous acceptez de |
| Thisuser | Cet utilisateur |
| Verifypassword | Vérifier le mot de passe |
| Filesizelimit | 2 Mo max. |
| accountnotfound | Compte introuvable |
| Avatarimageexceedsize | Votre image d'avatar dépasse la limite de 2 Mo. |
| fieldisrequired | Le champ accepte uniquement un entier. |
| fieldonlyacceptsavalidemail | Le champ accepte uniquement un courriel valide. |
| fieldonlyacceptsletters | Le champ accepte uniquement les lettres |
| Filesizemustbelessthanmo | La taille du fichier doit être inférieure {#}à Mo |
| invalidusernameorpassword | Nom d'utilisateur ou mot de passe non valide |
| minimumlengthofcharacters | Longueur minimale {#} des caractères |
| maximumlengthofcharacters | Longueur maximale {#} des caractères |
| ici waswasanerror | Une erreur s'est produite |
| thisfieldisrequired | Ce champ est obligatoire. |
| validations de fichier | Extensions de fichier valides |
| valuemustmatch | La valeur doit correspondre |
| Passwordlength | de 6 à 32 caractères. |
| Passwordcharacters | comprennent les caractères inférieur et supérieur - caractères de casse. |
| Passwordsymbols | inclure au moins un nombre et un symbole. |
| Passwordusername | ne contient pas votre nom d'utilisateur. |
| Passwordpopovertitle | Votre mot de passe doit : |
| Passworderrorcontainsfirstname | Le mot de passe que vous avez saisi contient le nom d'utilisateur, le prénom ou le nom. Pour des raisons de sécurité, veuillez saisir un mot de passe qui ne contient pas votre nom d'utilisateur, prénom ou nom. N'oubliez pas non plus que votre mot de passe doit contenir : 6 à 32 caractères Caractère majuscule Caractère en minuscules Un symbole |
| Passworderrorcontainslastname | Le mot de passe que vous avez saisi contient le nom d'utilisateur, le prénom ou le nom. Pour des raisons de sécurité, veuillez saisir un mot de passe qui ne contient pas votre nom d'utilisateur, prénom ou nom. N'oubliez pas non plus que votre mot de passe doit contenir : 6 à 32 caractères Caractère majuscule Caractère en minuscules Un symbole |
| Passworderrorcontainsusername | Le mot de passe que vous avez saisi contient le nom d'utilisateur, le prénom ou le nom. Pour des raisons de sécurité, veuillez saisir un mot de passe qui ne contient pas votre nom d'utilisateur, prénom ou nom. N'oubliez pas non plus que votre mot de passe doit contenir : 6 à 32 caractères Caractère majuscule Caractère en minuscules Un symbole |
| Passworderrortooshort | 6 caractères au minimum pour le mot de passe |
| Passworderrortoolong | 32 caractères au maximum pour le mot de passe |
| Passworderrormisjustifier ppercase | Le mot de passe doit contenir au moins un caractère majuscule. |
| Passworderrormissinglowercase | Mot de passe doit contenir au moins un caractère minuscule. |
| Passworderrormissingsymbol | Le mot de passe doit contenir au moins un symbole du jeu. `!@#$%^&*()?.,<>\’;:”[]{}|` |


