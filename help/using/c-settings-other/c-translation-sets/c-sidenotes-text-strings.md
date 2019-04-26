---
description: Personnalisation des chaînes de texte pour les courriers électroniques
  Livefyre
seo-description: Personnalisation des chaînes de texte pour les courriers électroniques
  Livefyre
seo-title: Chaînes de texte avec lettres
solution: Experience Manager
title: Chaînes de texte avec lettres
uuid: a 3735237-e 55 d -4 bc 0-b 88 d -8 a 323980 ee 09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Chaînes de texte avec lettres{#sidenotes-text-strings}

Personnalisation des chaînes de texte pour les courriers électroniques Livefyre

Cette page répertorie et décrit toutes les chaînes disponibles pour la personnalisation dans les applications de commentaires annexes. Pour plus d'informations sur les chaînes disponibles pour les applications Livefyre principales, reportez-vous à la page Personnalisations de chaînes.

Implémentation
authentique
Informations
de diffusion en continu Auteur/Contenu Informations
de l'utilisateur Fonctions
de publication Erreurs de l'interface
du modérateur

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
| Chaînes de menu authentiques | Menuauthsigninbtn | Connexion |
|  | Menuauthsignedinmsg | Vous devez être connecté à {action} |
|  | Menuusereditprofile | Modifier le profil |
|  | Menuuseradmin | Console d'administration |
|  | Menuuserlogout | Déconnexion |
|  | Menuuserbackbtn | Tout |

## Informations de diffusion en continu {#section_wpy_gl4_xz}

Chaînes disponibles pour les informations de flux de contenu et affichées.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Options du menu Informations | Menuinfocopyright | © Livefyre, Inc. 2014 |
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
|  | Datetimemonths | Un tableau. Par défaut =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | Questiondescription | Vous pouvez désormais lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Mettez en surbrillance le texte</span> et cliquez sur l <span class="&rdquo;fycon-write&rdquo;"></span> 'icône ou cliquez sur <span class="&rdquo;fycon-action-view&rdquo;"></span> l'icône à la fin de chaque paragraphe. |
|  | Questionmocktext | Ce qui est connu « connu connu » n'est pas connu, c'est qu'il est « familier ». |
|  | Questiontitle | Qu'est-ce qu'une illustration ? |

## Actions de l'utilisateur {#section_qxd_fl4_xz}

Chaînes disponibles pour les actions de l'utilisateur : marquage, partage et aimer le contenu existant.

| Elément | Clé | Texte par défaut |
|---|---|---|
| Options du menu Réponse | Menucylinesviewtitle | Détails |
|  | Menucylinesviewreply | Répondre à la conversation |
| Options du menu Partager | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Partager |
| Options du menu Indicateur | Menuflagoptionapprove | Refuser |
|  | Menuflagoptionoffensive | Offensif |
|  | Menuflagoptionofftopic | Rubrique désactivée |
|  | Menuflagoptionspam | Indésirable |
|  | Menuflagtitle | Marquer comme… |
|  | Facebooksharecaption | Indique le titre sur « {title} » |
| Options utilisateur mobiles | Slidercommenttally | of |
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
| Options du menu Supprimer | Menuconfirmaccept | Oui, {action} |
|  | Menuconfirmcancel | Annuler |
|  | Menuconfirmtitle | Êtes-vous sûr ? |
| Options du menu etc | Menuetcoptionapprove | Approuver |
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
| Messages de confirmation du menu Plus | Notificationapprouvé | Approuvé |
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

