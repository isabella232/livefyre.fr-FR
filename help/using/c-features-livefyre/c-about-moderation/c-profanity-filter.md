---
description: valeur nulle
seo-description: valeur nulle
seo-title: Utilisation du filtre de profilage
solution: Experience Manager
title: Utilisation du filtre de profilage
uuid: b 0 b 1 fbae-c 88 c -403 c -9 b 91-df 6620675 f 39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilisation du filtre de profilage{#using-the-profanity-filter}

L&#39;intégralité du contenu publié dans une application Livefyre est recherchée. Si un mot inclus dans la liste de profilité se trouve dans le contenu ou dans le nom d&#39;affichage d&#39;un utilisateur, ce contenu est marqué « Profanity », ce qui vous permet de le filtrer pour la prémodération, les règles, le modq ou les recherches générales dans le contenu de l&#39;application.

>[!NOTE]
>
>Le contenu des administrateurs Studio et des gestionnaires n&#39;est pas soumis à la vérification de règle Profanity et le contenu publié par un modérateur ne sera pas marqué.

Livefyre fournit une liste de profilité par défaut. Vous pouvez choisir d&#39;appliquer cette liste au niveau du réseau, de fournir votre propre liste ou d&#39;utiliser un agrégat des deux. Les sites individuels de votre réseau peuvent hériter de la liste Profanity du réseau ou utiliser une liste personnalisée pour être spécifique au site.

Pour fournir votre propre liste de profil personnalisée comme valeur par défaut du réseau, envoyez-la à votre gestionnaire de compte Livefyre.

## Activation du filtrage du profilage {#section_yqc_qsk_f1b}

Activez et configurez le filtre de profilité au niveau du réseau et du site. Désactivez le filtre de profilité au niveau du réseau pour désactiver automatiquement le filtre de profilité pour tous les sites héritant du réseau.

>[!NOTE]
>
>L&#39;ensemble du contenu transitant par Livefyre est analysé. Si le contenu contient des mots figurant dans la liste Profil SAFE SAFE ou dans votre liste Profanity personnalisée, il est marqué « Profanity ».  » » Pour définir Livefyre pour qu&#39;il prenne automatiquement des décisions sur ces éléments, activez **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**.

## Activation du filtre de profilité d&#39;un réseau {#section_twd_ssk_f1b}

1. Sélectionnez **[!UICONTROL Network]** dans le menu déroulant réseau.
1. Accédez **[!UICONTROL Settings > Network Settings > Moderation]**à.
1. Faites défiler la page jusqu&#39;à la **[!UICONTROL Profanity List]** position, puis définissez **[!UICONTROL Enable Profanity Checking]** la **[!UICONTROL ON]** variable sur.

1. Utilisez **[!UICONTROL Update Network Profanity List]** le champ pour ajouter des mots à la liste ou cliquez sur un mot pour le supprimer de la liste.

>[!NOTE]
>
>La modification de la liste du profilage au niveau réseau n&#39;affecte pas les listes au niveau du site déjà en place. Pour vous assurer que les modifications du réseau sont effectuées sur le site, sélectionnez **[!UICONTROL Restore Network List]** le site une fois les modifications effectuées.

## Activation du filtre de profilité d&#39;un site {#section_fld_wsk_f1b}

1. Sélectionnez le site dans le menu déroulant du réseau.
1. Accédez **[!UICONTROL Settings > Site Settings > Moderation]**à.
1. Faites défiler la page jusqu&#39;à la valeur **[!UICONTROL Profanity List]** et sélectionnez **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**-la.

1. Choisissez l&#39;une des options suivantes :

   * Pour hériter de la liste Profanity du réseau (ce n&#39;est pas courant), définissez **[!UICONTROL Use Site Profanity List]** cette option **[!UICONTROL OFF]** sur.

   * Pour modifier la liste Profanity spécifiquement pour le site, définissez **[!UICONTROL Use Site Profanity List]** cette option sur **[!UICONTROL On]** l&#39;ouverture du **[!UICONTROL Update Profanity List]** champ dans lequel vous pouvez modifier la liste :

      * Pour supprimer un mot, cliquez sur le mot.
      * Pour ajouter un mot, entrez le mot dans **[!UICONTROL Add new word]****[!UICONTROL Return]** la zone.

      * Pour savoir si un mot est inclus dans la liste, tapez le mot dans **[!UICONTROL Test profanity filter]** la zone.
   * Pour réimporter le profil du réseau et l&#39;appliquer au site, cliquez **[!UICONTROL Restore Network List]** sur.
   * Pour effacer tout le contenu de la liste et commencer à zéro, cliquez **[!UICONTROL Clear List]** sur.


## Utilisation du contenu contenant un profil {#section_epy_dtk_f1b}

Utilisez la liste Profanity pour filtrer vos recherches de contenu et créer des règles de prémodération pour modq.

Pour rechercher du contenu contenant du profilage, accédez **[!UICONTROL Library > App Content]****[!UICONTROL Filter by Flags]** à la case et cochez la **[!UICONTROL Profanity]** case. Tout le contenu qui a été capturé par le filtre de profanity pour le site ou le réseau sélectionné s&#39;affiche. Cette liste comprend le contenu extrait dans l&#39;application à l&#39;aide de socialsync et Streams.

Pour créer des règles de prémodération, sélectionnez l&#39;option **[!UICONTROL Settings > Network Settings > Moderation]** Studio. Une fois le filtre de profilité activé, une nouvelle règle s&#39;affiche, vous permettant de marquer ou prémodérer le contenu contenant le profilage. Par défaut, cette règle active automatiquement **[!UICONTROL Premoderate]** le contenu du profane, qui peut être modifié en **[!UICONTROL Trash it]** ou **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Si un seul élément de contenu est soumis à plusieurs types de règles (comme les règles SAFE et Flag), plus les règles sont strictes, plus le strict est appliqué. Par exemple : Si votre règle de prémodération indique de prémodérer un élément de contenu mais qu&#39;une règle SAFE indique de la corbeille, elle sera coupée.

## Affichage et mise à jour de la liste du profilage pour un réseau {#section_qdb_btk_f1b}

1. Accédez **[!UICONTROL Settings > Network Settings > Moderation]**à.
1. Faites défiler la section jusqu&#39;à la **[!UICONTROL Profanity List]** section.
1. Définissez **[!UICONTROL Enable Profanity Checking]** la **[!UICONTROL On]** liste pour qu&#39;elle affiche la liste activée pour votre réseau (par défaut Livefyre ou votre liste personnalisée téléchargée) et modifiez-la. Vous pouvez la modifier comme suit :
   * Pour supprimer un mot, cliquez sur le mot.
   * Pour ajouter un mot, entrez le mot dans **[!UICONTROL Add new word]****[!UICONTROL Return]** la zone.
   * Pour savoir si un mot est inclus dans la liste, tapez le mot dans **[!UICONTROL Test profanity filter]** la zone.

>[!NOTE]
>
>Seuls les administrateurs Studio et les modérateurs peuvent modifier les listes de profilées.

