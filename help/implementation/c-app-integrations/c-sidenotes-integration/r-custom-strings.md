---
description: valeur nulle
seo-description: valeur nulle
seo-title: Chaînes personnalisées avec indicateur
title: Chaînes personnalisées avec indicateur
uuid: 73745273-d 3 fb -4569-8910-d 149 fb 37 a 7 b 4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Chaînes personnalisées avec indicateur{#sidenotes-custom-strings}

Les chaînes personnalisées sont appliquées par l&#39;intermédiaire d&#39;un objet injecté dans le constructeur des balises et remplacent les chaînes par défaut utilisées par l&#39;application. Ils peuvent être utilisés pour personnaliser une partie de la langue en fonction de vos spécifications de style ou de langue. Les chaînes fusionnent automatiquement avec les valeurs par défaut.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Clé | Par défaut |
|---|---|
| Appname | Commentaires de sidenotes |
| Commentmoderatortag | Mod |
| Commentpendingtag | En attente |
| Commentreadmorelink | En savoir plus |
| Commentreplylink | Voir {number} réponses |
| Commentreplylinksing | Voir la réponse |
| Commentvotecount | votes |
| Commentvotecountsing | voter |
| Editorplaceholder | Que pensez-vous ? |
| Editorpostbtn | Caractère sidenote de publication |
| Editorpostbtnmobile | Publication |
| Editorpublication | Publication… |
| Editorreplybtn | Post-réponse |
| Editorreplytitle | Ecrire une réponse |
| Editortitle | Note écrite |
| Emptyimageblocktxt | Que pensez-vous ? |
| Emptytextblocktxt | + |
| Errorconnection | Uh-oh. Vous ne semblez pas avoir une bonne connexion. |
| Errorduplicate | Vous aimez également votre remarque, mais vous ne pouvez pas la publier deux fois. |
| Errorgenated | Une erreur est survenue. Veuillez réessayer. |
| Errorserver | Un problème est survenu avec notre serveur. Essayez-le de nouveau ? |
| Facebooksharecaption | Sidenotes sur « {title} » |
| Menuauthsignedinmsg | Vous devez être connecté à {action} |
| Menuauthsigninbtn | Connexion |
| Menubackbtn | Retour |
| Menuconfirmaccept | Oui, {action} |
| Menuconfirmcancel | Annuler |
| Menuconfirmtitle | Êtes-vous sûr ? |
| Menuetcoptionapprove | Approuver |
| Menuetcoptiondelete | Supprimer |
| Menuetcoptionedit | Modifier |
| Menuetcoptionflag | Indicateur |
| Menuetcoptionshare | Partager |
| Menuetcpostedat | Publié le {date} |
| Menuetctitle | Plus |
| Menuflagoptionapprove | Refuser |
| Menuflagoptionoffensive | Offensif |
| Menuflagoptionofftopic | Rubrique désactivée |
| Menuflagoptionspam | Indésirable |
| Menuflagtitle | Marquer comme… |
| Menuinfocopyright | © Livefyre, Inc. 2014 |
| Menuinfohelp | Aide |
| Menuinfolivefyrelink | Visitez Livefyre.com |
| Menucylinesviewreply | Répondre à la conversation |
| Menucylinesviewtitle | Détails |
| Menushareoptionfacebook | Facebook |
| Menushareoptionlink | Copier le permalink |
| Menushareoptionlinkcomplete | Copié |
| Menushareoptionlinkfailed | Échec de la copie |
| Menushareoptiontwitter | Twitter |
| Menusharetitle | Partager |
| Notificationapprouvé | Approuvé |
| Notificationdeleted | Supprimé |
| Notificationflagged | Marqué |
| Permalinkbackbtn | Tout |
| Permalinktitle | Permalink |
| Questiondescription | Vous pouvez désormais lire et écrire des commentaires directement sur des phrases, des paragraphes, des images et des guillemets.<br><br>Mettez en surbrillance le texte et cliquez sur l&#39;icône « fycon-write » ou cliquez sur l&#39;icône « fycon-action-view » à la fin de chaque paragraphe. |
| Questionmocktext | Ce qui est connu « connu connu » n&#39;est pas connu, c&#39;est qu&#39;il est « familier ». |
| Questiontitle | Qu&#39;est-ce qu&#39;une illustration ? |
| Queuedcommentsplural | {number} Nouveaux commentaires |
| Queuedcommentssingular | 1 Nouveau fichier Sidenote |
| Queuedpliesplural | {number} Nouvelles réponses |
| Queuedpliessingular | 1 Nouvelle réponse |
| Replybtn | Répondre |
| Signintopost | Se connecter pour écrire un caractère annexe |
| Slidercommenttally | of |
| Sliderinviteread | Read |
| Sliderinvitewrite | Écrire |
| Sliderwritetext | Que pensez-vous ? Appuyez sur pour écrire |
| Threadcollapsebtn | Réduire |
| Threadexpandbtnplural | Développer {number} réponses |
| Threadexpandbtnsingular | Développer 1 réponse |
| Threadreplybtn | Répondre à la conversation |
