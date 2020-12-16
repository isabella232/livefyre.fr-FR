---
description: valeur nulle
seo-description: valeur nulle
seo-title: Utilisation du filtre de rentabilité
solution: Experience Manager
title: Utilisation du filtre de rentabilité
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 1%

---


# Utilisation du filtre de rentabilité{#using-the-profanity-filter}

Tout le contenu publié dans une application Livefyre est contrôlé pour son obscénité. Si un mot inclus dans la liste de profil se trouve dans le contenu ou dans le nom d’affichage d’un utilisateur, ce contenu est marqué &quot;Profanité&quot;, ce qui vous permet de le filtrer pour les recherches de prémodération, de règles, de règles, de questions multimédias ou les recherches générales dans le contenu de l’application.

>[!NOTE]
>
>Le contenu des administrateurs et gestionnaires de Studio n’est pas soumis à la vérification de la règle de rentabilité et le contenu publié par un modérateur ne sera pas marqué.

Livefyre fournit une liste de profanation par défaut. Vous pouvez choisir d&#39;appliquer cette liste au niveau du réseau, de fournir votre propre liste ou d&#39;utiliser un agrégat des deux. Les sites individuels de votre réseau peuvent hériter de la Liste de rentabilité du réseau ou utiliser une liste personnalisée pour être spécifiques au site.

Pour fournir votre propre liste de profil personnalisée comme valeur par défaut de votre réseau, envoyez-la à votre gestionnaire de compte Livefyre.

## Activation du filtrage des bénéfices {#section_yqc_qsk_f1b}

Activez et configurez le filtre de profil au niveau du réseau et du site. Désactivez le filtre de profil au niveau du réseau pour désactiver automatiquement le filtre de profil pour tous les sites qui héritent du réseau.

>[!NOTE]
>
>Tout le contenu qui passe par Livefyre est contrôlé pour son obscénité. Si le contenu qui contient des mots figurant sur la liste de profanation par défaut SAFE ou dans votre liste de Profanité personnalisée est trouvé, il est marqué &quot;Profanité&quot;. Pour configurer Livefyre de manière à ce qu&#39;il agisse automatiquement sur ces éléments, faites **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

## Activer le filtre de rentabilité pour un réseau {#section_twd_ssk_f1b}

1. Sélectionnez **[!UICONTROL Network]** dans le menu déroulant du réseau.
1. Atteindre **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Faites défiler l&#39;écran jusqu&#39;à **[!UICONTROL Profanity List]** et définissez **[!UICONTROL Enable Profanity Checking]** sur **[!UICONTROL ON]**.

1. Utilisez le champ **[!UICONTROL Update Network Profanity List]** pour ajouter des mots à la liste ou cliquez sur un mot pour le supprimer de la liste.

>[!NOTE]
>
>La modification de la Liste de Profanité au niveau du réseau n&#39;affectera aucune Liste au niveau du site déjà en place. Pour vous assurer que les modifications du réseau sont apportées au site, sélectionnez **[!UICONTROL Restore Network List]** pour le site après les modifications.

## Activer le filtre de rentabilité pour un site {#section_fld_wsk_f1b}

1. Sélectionnez le site dans le menu déroulant du réseau.
1. Atteindre **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Faites défiler l&#39;écran jusqu&#39;à **[!UICONTROL Profanity List]** et définissez **[!UICONTROL Enable Profanity Checking]** sur **[!UICONTROL ON]**.

1. Choisissez l’une des options suivantes :

   * Pour hériter de la Liste Profanité du réseau (ce n&#39;est pas courant), définissez **[!UICONTROL Use Site Profanity List]** sur **[!UICONTROL OFF]**.

   * Pour modifier la Liste Profanity spécifiquement pour le site, définissez **[!UICONTROL Use Site Profanity List]** sur **[!UICONTROL On]** pour ouvrir le champ **[!UICONTROL Update Profanity List]**, où vous pouvez modifier la liste :

      * Pour supprimer un mot, cliquez dessus.
      * Pour ajouter un mot, saisissez le mot dans la zone **[!UICONTROL Add new word]** et appuyez sur **[!UICONTROL Return]**.

      * Pour savoir si un mot est inclus dans la liste, saisissez-le dans la zone **[!UICONTROL Test profanity filter]**.
   * Pour réimporter la Liste Profanité réseau et l&#39;appliquer au site, cliquez sur **[!UICONTROL Restore Network List]**.
   * Pour effacer de zéro tout le contenu de la liste et du début, cliquez sur **[!UICONTROL Clear List]**.


## Utilisation de contenu contenant de la rentabilité {#section_epy_dtk_f1b}

Utilisez la Liste Profanité pour vous aider à filtrer vos recherches de contenu et à créer des règles de modération pour ModQ.

Pour rechercher du contenu contenant des obscénités, accédez à **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** et cochez la case **[!UICONTROL Profanity]**. Tout le contenu qui a été capturé par le filtre de rentabilité pour le site ou le réseau sélectionné s&#39;affiche. Cette liste inclura le contenu extrait dans l’application à l’aide de SocialSync et de Streams.

Pour créer des règles de modération, sélectionnez **[!UICONTROL Settings > Network Settings > Moderation]** dans Studio. Une fois le filtre de profil activé, une nouvelle règle s’affiche, vous permettant d’indiquer ou de prémodérer le contenu contenant du contenu de profil. Par défaut, cette règle active automatiquement **[!UICONTROL Premoderate]** pour le contenu de profil, qui peut être remplacé par **[!UICONTROL Trash it]** ou **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Si un seul élément de contenu est soumis à plusieurs types de règles (règles SAFE et Flag, par exemple), le plus strict sera appliqué. Par exemple : Si votre règle de prémodération indique de modérer un élément de contenu, mais qu’une règle SAFE indique de le supprimer, il sera supprimé.

## Vue et mise à jour de la Liste Profanity pour un réseau {#section_qdb_btk_f1b}

1. Atteindre **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Faites défiler l&#39;écran jusqu&#39;à la section **[!UICONTROL Profanity List]**.
1. Définissez **[!UICONTROL Enable Profanity Checking]** sur **[!UICONTROL On]** pour afficher la Liste activée pour votre réseau (par défaut Livefyre ou votre liste personnalisée téléchargée) et la modifier. Vous pouvez modifier la liste comme suit :
   * Pour supprimer un mot, cliquez dessus.
   * Pour ajouter un mot, saisissez le mot dans la zone **[!UICONTROL Add new word]** et appuyez sur **[!UICONTROL Return]**.
   * Pour savoir si un mot est inclus dans la liste, saisissez-le dans la zone **[!UICONTROL Test profanity filter]**.

>[!NOTE]
>
>Seuls les administrateurs et les modérateurs de Studio peuvent modifier les Listes Profanity.

