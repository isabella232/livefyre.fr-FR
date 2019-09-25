---
description: valeur nulle
seo-description: valeur nulle
seo-title: Utilisation du filtre de rentabilité
solution: Experience Manager
title: Utilisation du filtre de rentabilité
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilisation du filtre de rentabilité{#using-the-profanity-filter}

Tout le contenu publié dans une application Livefyre est vérifié pour des raisons de profanation. Si un mot figurant dans la liste des propension se trouve dans le contenu ou dans le nom d’affichage d’un utilisateur, ce contenu est marqué "Profanité", ce qui vous permet de le filtrer pour les recherches de prémodération, de règles, de modération ou de type général dans le contenu de l’application.

>[!NOTE]
>
>Le contenu des administrateurs et des gestionnaires de Studio n’est pas soumis à la vérification de la règle de rentabilité et le contenu publié par un modérateur ne sera pas marqué.

Livefyre fournit une liste de profils par défaut. Vous pouvez choisir d'appliquer cette liste au niveau du réseau, de fournir votre propre liste ou d'utiliser un agrégat des deux. Les sites individuels de votre réseau peuvent hériter de la liste de rentabilité du réseau ou utiliser une liste personnalisée pour être spécifique au site.

Pour fournir votre propre liste de profils personnalisés comme valeur par défaut de votre réseau, veuillez l'envoyer à votre gestionnaire de compte Livefyre.

## Activation du filtrage des bénéfices {#section_yqc_qsk_f1b}

Activez et configurez le filtre de profil au niveau du réseau et du site. Désactivez le filtre de profil au niveau du réseau pour désactiver automatiquement le filtre de profil pour tous les sites qui héritent du réseau.

>[!NOTE]
>
>Tout le contenu passant par Livefyre est vérifié pour des raisons de profanation. Si du contenu est trouvé, qui inclut des mots figurant dans la liste de profanation SAFE par défaut ou dans votre liste de Profanité personnalisée, il est marqué "Profanité". Pour configurer Livefyre de manière à agir automatiquement sur ces éléments, passez **[!UICONTROL Enable Profanity Checking]** à **[!UICONTROL ON]**.

## Activation du filtre de rentabilité pour un réseau {#section_twd_ssk_f1b}

1. Sélectionnez **[!UICONTROL Network]** dans le menu déroulant du réseau.
1. Atteindre **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Faites défiler l’écran jusqu’au **[!UICONTROL Profanity List]**, puis définissez **[!UICONTROL Enable Profanity Checking]** sur **[!UICONTROL ON]**.

1. Utilisez le **[!UICONTROL Update Network Profanity List]** champ pour ajouter des mots à la liste ou cliquez sur un mot pour le supprimer de la liste.

>[!NOTE]
>
>La modification de la liste des bénéficiaires au niveau du réseau n'affectera aucune liste au niveau du site déjà en place. Pour vous assurer que les modifications du réseau sont apportées au site, sélectionnez-le **[!UICONTROL Restore Network List]** pour le site une fois les modifications effectuées.

## Activation du filtre de rentabilité pour un site {#section_fld_wsk_f1b}

1. Sélectionnez le site dans le menu déroulant du réseau.
1. Atteindre **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Faites défiler l’écran vers le bas jusqu’à **[!UICONTROL Profanity List]** et définissez **[!UICONTROL Enable Profanity Checking]** sur **[!UICONTROL ON]**.

1. Choisissez l’une des options suivantes :

   * Pour hériter de la liste des bénéfices du réseau (ce n’est pas courant), définissez **[!UICONTROL Use Site Profanity List]** sur **[!UICONTROL OFF]**.

   * Pour modifier la liste des bénéfices spécifiquement pour le site, définissez **[!UICONTROL Use Site Profanity List]** le champ **[!UICONTROL On]** **[!UICONTROL Update Profanity List]** pour lequel vous pouvez modifier la liste :

      * Pour supprimer un mot, cliquez dessus.
      * Pour ajouter un mot, saisissez-le dans la **[!UICONTROL Add new word]** zone et appuyez sur **[!UICONTROL Return]**.

      * Pour savoir si un mot est inclus dans la liste, entrez-le dans la **[!UICONTROL Test profanity filter]** zone.
   * Pour réimporter la liste des bénéfices du réseau et l'appliquer au site, cliquez sur **[!UICONTROL Restore Network List]**.
   * Pour effacer tout le contenu de la liste et commencer à partir de zéro, cliquez sur **[!UICONTROL Clear List]**.


## Utilisation de contenu qui contient de la rentabilité {#section_epy_dtk_f1b}

Utilisez la liste des propriétés pour vous aider à filtrer vos recherches de contenu et à créer des règles de prémodération pour ModQ.

Pour rechercher du contenu contenant des obscénités, sélectionnez **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** puis cochez la **[!UICONTROL Profanity]** case. Tout le contenu qui a été capturé par le filtre de rentabilité pour le site ou le réseau sélectionné s'affiche. Cette liste comprend le contenu extrait dans l’application à l’aide de SocialSync et de Flux de données.

Pour créer des règles de modération, sélectionnez **[!UICONTROL Settings > Network Settings > Moderation]** dans Studio. Une fois le filtre de profil activé, une nouvelle règle s’affiche, vous permettant d’indiquer ou de modérer le contenu contenant du contenu de profil. Par défaut, cette règle active automatiquement **[!UICONTROL Premoderate]** le contenu de profil, qui peut être remplacé par **[!UICONTROL Trash it]** ou **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Si un seul élément de contenu est soumis à plusieurs types de règles (règles SAFE et Flag, par exemple), le plus strict sera appliqué. Par exemple : Si votre règle de prémodération indique de modérer un élément de contenu, mais qu’une règle SAFE indique de le corrompre, il sera supprimé.

## Affichage et mise à jour de la liste des bénéfices pour un réseau {#section_qdb_btk_f1b}

1. Atteindre **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Faites défiler jusqu’à la **[!UICONTROL Profanity List]** section.
1. Définissez cette option **[!UICONTROL Enable Profanity Checking]** pour **[!UICONTROL On]** afficher la liste activée pour votre réseau (par défaut Livefyre ou votre liste personnalisée téléchargée) et modifiez-la. Vous pouvez modifier la liste comme suit :
   * Pour supprimer un mot, cliquez dessus.
   * Pour ajouter un mot, saisissez-le dans la **[!UICONTROL Add new word]** zone et appuyez sur **[!UICONTROL Return]**.
   * Pour savoir si un mot est inclus dans la liste, entrez-le dans la **[!UICONTROL Test profanity filter]** zone.

>[!NOTE]
>
>Seuls les administrateurs et les modérateurs de Studio peuvent modifier les listes de profil.

