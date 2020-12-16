---
description: Modérez le contenu à partir d’une interface unique et intelligente.
seo-description: Modérez le contenu à partir d’une interface unique et intelligente.
seo-title: Modération du contenu à l’aide de ModQ
title: Modération du contenu à l’aide de ModQ
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# Modération du contenu à l’aide de ModQ{#moderate-content-using-modq}

Modérez le contenu à partir d’une interface unique et intelligente.

ModQ crée une file d’attente en temps réel de tout le contenu de votre site ou réseau qui correspond aux règles de prémodération que vous avez définies, ce qui permet aux modérateurs de se concentrer uniquement sur le contenu qui requiert leur attention.

Une fois que vous avez défini les paramètres ModQ, le nouveau contenu entrant dans le flux ou le contenu existant marqué par vos utilisateurs est ajouté à votre file d’attente. Les modifications apportées à vos règles ne supprimeront pas le contenu du ModQ, mais ajouteront un nouveau contenu à la file d’attente en fonction de vos nouveaux paramètres.

ModQ vous permet de :

* Modérez en contexte, vue des threads entiers et Approuvez, Corbeille ou Bozo des éléments de contenu individuels ou des threads complets en un seul clic.
* Augmentez la vitesse et l’efficacité de votre flux de travail.
* Répondez au contenu en augmentant votre implication dans votre communauté.
* Permettre à plusieurs modérateurs de travailler sur le contenu, sans dupliquer les travaux des autres.

Le contenu Livefyre est répertorié dans ModQ pendant 6 semaines au maximum et le contenu prémodéré en flux continu qui n’a pas été traité est répertorié dans ModQ pendant 90 jours.

>[!NOTE]
>
>Un seul élément de contenu peut être répertorié plusieurs fois s’il correspond à plusieurs règles d’inclusion dans ModQ. Par exemple, si un élément de contenu déclenche une règle d’indicateur d’utilisateur pour Offensive, puis déclenche une autre règle pour Profane, elle est répertoriée deux fois dans ModQ.

Le contenu qui ne s’affiche pas dans ModQ comprend :

* Contenu haché.
* Contenu approuvé par un modérateur.
* Contenu publié par un utilisateur interdit ou indicateurs d’utilisateur appliqués par un utilisateur interdit.

## Navigation dans ModQ {#section_uv4_db2_yy}

ModQ est divisé en deux panneaux à onglets :

* **[!UICONTROL Items]** liste tous les contenus Livefyre natifs et SocialSync prévus pour la modération. Cet onglet comprend tout contenu de recherche ou de diffusion en continu sur Social qui a été marqué ou modifié après modération.
* **[!UICONTROL Streams Premoderation]** liste tout le contenu entrant dans vos applications à partir de flux avec l’option Prémodéré activée. (Pour plus d’informations, voir Création de flux.)

Les deux onglets offre de nombreux filtres et outils de modération identiques.

* **[!UICONTROL Item Count]** Le nombre d’éléments restants dans la file d’attente s’affiche dans le coin supérieur gauche de ModQ.
* **[!UICONTROL Filter]** Cliquez sur  **[!UICONTROL Filter]** pour définir les paramètres par lesquels le contenu sera répertorié dans le volet.
* **[!UICONTROL History]** Cliquez sur le  **[!UICONTROL History]** bouton en haut à droite de l’écran pour ouvrir une liste de contenu récemment modéré, ce qui vous permet de revoir votre travail ou de modifier une action de modération récente. Cliquez de nouveau sur le bouton pour revenir au contenu en file d’attente. Seules les 100 actions les plus récentes s’affichent. **L&#39;** histoire ne liste pas les actions entreprises par un autre modérateur.

* **[!UICONTROL User Pane]** Cliquez sur les boutons Développer ou Réduire en haut à droite de la page pour ouvrir ou fermer le volet Utilisateur.

## Présentation du contenu ModQ {#section_oxm_kgz_y1b}

Chaque élément de contenu répertorié affiche des informations sur la prévisualisation, y compris le site sur lequel il a été publié et son auteur. La sélection d’un élément affiche l’intégralité du contenu, y compris tout média.

>[!NOTE]
>
>Le contenu natif Livefyre affiche plus d’informations que le contenu ajouté à votre application par le biais de flux ou d’autres sources de médias sociaux.

Les informations suivantes s’affichent lorsque vous sélectionnez un élément :

* **[!UICONTROL Time in Queue:]** liste la durée pendant laquelle l’élément de contenu a été ajouté à ModQ.
* **[!UICONTROL App name:]** l’application dans laquelle le contenu s’affiche. Liens vers le site avec l’application.
* **[!UICONTROL Content Body:]** miniature de texte et de média, le cas échéant.
* **[!UICONTROL Status:]** l’état actuel du contenu (En attente, En mémoire tampon, etc.).
* **[!UICONTROL Author information:]** le nom et le nom d’utilisateur de l’auteur.
* **[!UICONTROL Timestamp:]** l’horodatage relatif de la création du contenu. Permet d’établir un lien d’accès à l’élément de contenu de la page Contenu de l’application de Studio.
* **[!UICONTROL Flag Type:]** Offensive, Désaccord, Indésirable, etc.

   * Indicateurs SAFE : Indésirable et en masse.
   * Indicateur appliqué par votre Liste de rentabilité réseau et site : Profanité.
   * Indicateurs appliqués par SAFE : Discours haineux, informations personnelles identifiables, insultes et profanation.
   * Indicateurs utilisateur : Indésirable, hors sujet, offensif et en désaccord.

* **[!UICONTROL Flag origin:]** la source de l’indicateur répertorié. Peut être SAFE, un nom d&#39;utilisateur ou Livefyre.
* **[!UICONTROL More info:]** listes des détails sur le contenu, notamment le nombre de mentions J’aime, d’indicateurs utilisateur, de réponses et de balises éventuelles appliquées au contenu. Cliquer sur le site ouvre la page de niveau supérieur du site sur lequel se trouve le contenu. Un clic sur l’horodatage ouvre une vue filetée du contenu dans le contexte de la page.

## Options de filtre dans ModQ {#section_r2c_qc2_yy}

Cliquez sur **[!UICONTROL Filter]** en haut à gauche de la fenêtre ModQ pour ouvrir un panneau contenant les options de filtre disponibles pour le contenu répertorié. Lorsque vous sélectionnez des options, ModQ met automatiquement à jour vers la liste votre contenu filtré uniquement. Cliquez sur **[!UICONTROL Clear filters]** pour effacer toutes les options sélectionnées et recharger la liste complète des éléments.

Différentes options de filtre sont disponibles pour les onglets **[!UICONTROL Items]** et **[!UICONTROL Streams Premoderation]**.

Les options suivantes sont disponibles pour ModQ sous **[!UICONTROL Items]** et **[!UICONTROL Streams Premoderation]** :

* **[!UICONTROL App]**. Utilisez le champ Rechercher des applications pour filtrer les résultats par application. Plusieurs applications peuvent être sélectionnées.
* **[!UICONTROL System Flags]**. Vous pouvez filtrer le contenu selon des règles telles que les règles Indésirable, Profanité, Sécurité et Prémodération.

   * La sélection de **[!UICONTROL Spam]** liste tous les contenus marqués comme indésirables par SAFE.
   * La sélection de **[!UICONTROL Profanity]** liste tout le contenu balisé Profane par votre Liste de profil réseau ou de site.
   * La sélection de **[!UICONTROL SAFE]** liste tout le contenu entrant ModQ en raison de vos règles SAFE.
   * La sélection de **[!UICONTROL Premoderation]** liste tout le contenu balisé pour la prémodération par vos paramètres réseau, de diffusion en continu ou d’application.

* **[!UICONTROL User Flags]** Filtrez le contenu par indicateurs utilisateur. Les options disponibles sont Offensive, Spam, Hors sujet et Désaccord.
* **[!UICONTROL Rights Requests.]** Affichez uniquement le contenu avec les droits accordés en cochant la case.
* **[!UICONTROL Entered the queue.]** Vous pouvez filtrer le contenu selon la période au cours de laquelle le contenu a été envoyé à ModQ. L’heure à laquelle le contenu a été envoyé à ModQ n’est pas nécessairement celle à laquelle le contenu a été publié sur son application.

Les options suivantes sont disponibles pour ModQ sous **[!UICONTROL Streams Premoderation]** :

* **[!UICONTROL Social Source]** Filtrez le contenu selon la source sociale d’où provient le contenu. Par exemple, les options des sources sociales sont Twitter, Instagram, Facebook et RSS.

L’option suivante est disponible pour ModQ sous **[!UICONTROL Items]** :

**[!UICONTROL Moderation Recommendations]**. Filtrez le contenu selon la recommandation donnée par la recommandation de modération automatisée.

Les images suivantes montrent à quoi ressemble la Recommendations de modération dans ModQ :  ![](assets/mod_reco1.png)

La recommandation de modération est donnée pour le contenu lorsqu’elle est configurée dans **[!UICONTROL Network Settings > Moderation]** et **[!UICONTROL Network Settings > ModQ]**.

## Actions que vous pouvez utiliser dans ModQ {#section_h4g_wrn_z1b}

Vous pouvez décider ce que vous voulez faire de chaque élément de contenu dans le ModQ.

Sélectionnez l’une des options suivantes :

* L&#39;icône **[!UICONTROL Checkbox]** pour approuver le contenu
* L&#39;icône **[!UICONTROL Trash can]** pour envoyer le contenu à la corbeille
* **[!UICONTROL Request Rights]** pour demander les droits sur le contenu au propriétaire du contenu.

   >[!NOTE]
   >
   >Vous ne pouvez pas demander de droits dans ModQ pour du contenu sur Instagram. Vous devez utiliser la bibliothèque ou le contenu de l&#39;application pour envoyer des demandes de droits pour du contenu à partir d&#39;Instagram.

* **[!UICONTROL Feature and Approve]** pour approuver le contenu et présenter également l’élément de contenu.
* **[!UICONTROL Product Tag and Approve]** pour ajouter un produit de votre catalogue de produits au contenu, puis l’approuver.
* **[!UICONTROL Mark as Pending]** pour marquer le contenu comme en attente.

>[!NOTE]
>
>Une fois que vous corrompez un élément de contenu, ce dernier et toutes les réponses à cet élément de contenu sont définitivement supprimés de ModQ. Pour placer un élément de contenu corrompu dans une application, voir [Ajouter un élément corrompu dans une application](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Si le contenu est déjà dans l’état souhaité, l’option Corbeille, Bozo ou Approuver confirme l’état et supprime l’élément de la liste. La modération d’un élément de contenu le supprime immédiatement de votre file d’attente et le désactive dans les files d’attente d’autres modérateurs.

>[!NOTE]
>
>Le contenu du flux ne peut pas être Bozo. Le contenu du flux de suivi le supprime définitivement du flux et ne peut pas être annulé.

Une fois le contenu modéré, il est supprimé du ModQ du modérateur et son auteur ne peut plus le modifier dans le flux. Si un modérateur rejette un élément ou si un utilisateur supprime son commentaire, celui-ci apparaît grisé dans les files d’attente d’autres modérateurs en temps réel. Lorsque le contenu a été grisé, le bouton **[!UICONTROL Clear Moderated]** s’affiche sur la page, ce qui permet aux modérateurs de le supprimer de leurs listes et de conserver leur place sur la page, quelle que soit l’activité du modérateur.

## Utilisation de la fonction Corbeille dans ModQ {#section_tpx_qgz_y1b}

Utilisez la section Paramètres pour sélectionner les options disponibles lorsque le contenu est marqué comme étant en pointillé.

* ****[!UICONTROL Confirm Trash]**** Activez cette option pour exiger que les modérateurs confirment leur action lors de la définition du contenu dans la corbeille. Lorsqu&#39;elle est activée, la sélection de **[!UICONTROL Trash]** pour le contenu affiche une boîte de dialogue demandant un **[!UICONTROL Reason for Moderation]** et offre un champ dans lequel un **[!UICONTROL Note]** peut être saisi.

   (Ce paramètre est disponible **[!UICONTROL only]** au niveau du réseau et s&#39;applique à tous les sites sous votre réseau.)

* ****[!UICONTROL Hide Replies]**** Activez cette option pour corrompre automatiquement les réponses lorsqu’un commentaire parent est corrompu ou que Bozo est corrompu.

## Modifier le statut d&#39;utilisateur dans ModQ {#section_tmw_lg1_z1b}

Cliquez sur le bouton **[!UICONTROL User actions]** du panneau Résumé pour l’utilisateur pour mettre l’utilisateur en sourdine, interdire ou Placer sur la liste autorisée.

* **[!UICONTROL Mute:]** vous permet de mettre en sourdine les indicateurs de l’utilisateur qui a marqué l’élément de contenu répertorié. Utilisez cette option pour exclure les indicateurs de l’utilisateur de vos filtres de prémodération. Le contenu qu’ils signalent n’entre pas dans ModQ en raison de l’indicateur et leurs indicateurs ne sont pas inclus dans les règles d’indicateur.
* **[!UICONTROL Ban:]** vous permet d’interdire l’utilisateur répertorié sur votre site ou réseau. (Seuls les administrateurs Studio ou les gestionnaires d’utilisateurs peuvent interdire un utilisateur sur le réseau.)
* **[!UICONTROL Whitelist:]** vous permet de placer sur la liste autorisée l’utilisateur répertorié pour votre site ou réseau. (Seuls les administrateurs Studio ou les gestionnaires d’utilisateurs peuvent mettre en réseau une liste autorisée d’utilisateur.)



Applications utilisant ModQ :

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Critiques](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Bouton Télécharger](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

