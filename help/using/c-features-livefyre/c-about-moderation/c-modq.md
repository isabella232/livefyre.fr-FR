---
description: Modérez le contenu à partir d'une interface intelligente et intelligente.
seo-description: Modérez le contenu à partir d'une interface intelligente et intelligente.
seo-title: Modérer le contenu à l'aide de modq
title: Modérer le contenu à l'aide de modq
uuid: c 630 fb 85-7 bd 0-4 da 0-ac 7 e -080 e 970 fb 4 f 9
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Modérer le contenu à l'aide de modq{#moderate-content-using-modq}

Modérez le contenu à partir d'une interface intelligente et intelligente.

Modq crée une file d'attente en temps réel de tout le contenu sur votre site ou réseau correspondant aux règles de prémodération que vous avez définies, ce qui permet à vos modérateurs de se concentrer uniquement sur le contenu qui requiert leur attention.

Une fois que vous avez défini les paramètres modq, le nouveau contenu entrant dans le flux ou le contenu existant marqué par vos utilisateurs sera ajouté à votre file d'attente. Les modifications apportées à vos règles ne supprimeront pas le contenu de modq, mais ajouteront du nouveau contenu à la file d'attente selon vos nouveaux paramètres.

Modq vous permet de :

* Modérez en contexte, affichez les threads entiers et Approuver, Corbeille ou Bozo, soit individuellement, soit en un seul clic.
* Augmentez la vitesse et l'efficacité de votre flux de travail.
* Répondre au contenu, ce qui accroît votre implication dans votre communauté.
* Permettre à plusieurs modérateurs de travailler dans le contenu sans en dupliquer chacun - le travail d'autres utilisateurs.

Le contenu Livefyre est répertorié dans modq pendant 6 semaines au maximum et le contenu prémodéré qui n'a pas été corrigé est répertorié dans modq pendant 90 jours.

>[!NOTE]
>
>Un seul élément de contenu peut être répertorié plusieurs fois s'il correspond à plusieurs règles pour inclusion dans modq. Par exemple, si un élément de contenu déclenche une règle d'indicateur d'utilisateur pour Offensif, puis déclenche ultérieurement une autre règle pour Profane, elle est répertoriée à deux reprises dans modq.

Le contenu qui ne s'affiche pas dans modq inclut :

* Contenu coupé.
* Contenu approuvé par un modérateur.
* Contenu publié par un utilisateur interdit ou indicateur d'utilisateur appliqué par un utilisateur interdit.

## Navigation dans modq {#section_uv4_db2_yy}

Modq est divisé en deux panneaux à onglets :

* **[!UICONTROL Items]** répertorie tous les contenus de synchronisation Livefyre et socialsync pour la modération. Cet onglet inclut tout contenu de recherche ou de flux social qui a été marqué ou modifié après la modération.
* **[!UICONTROL Streams Premoderation]** répertorie tout le contenu entrant dans vos applications à partir de flux dont la fonction Prémodérée est activée. (Pour plus d'informations, voir Création de flux.)

Les deux onglets proposent de nombreux filtres et outils de modération.

* **[!UICONTROL Item Count]** Le nombre d'éléments restant dans la file d'attente s'affiche dans le coin supérieur gauche de modq.
* **[!UICONTROL Filter]** Cliquez sur **[!UICONTROL Filter]** pour définir les paramètres d'affichage du contenu dans le volet.
* **[!UICONTROL History]** Cliquez sur **[!UICONTROL History]** le bouton en haut à droite de l'écran pour ouvrir la liste du contenu récemment modéré, ce qui vous permet de revoir votre travail ou de modifier une action de modération récente. Cliquez de nouveau sur le bouton pour revenir à votre contenu mis en file d'attente. Seules les 100 actions les plus récentes s'affichent. **L'historique** ne répertorie pas les actions effectuées par un autre modérateur.

* **[!UICONTROL User Pane]** Cliquez sur les boutons Développer ou Réduire en haut à droite de la page pour ouvrir ou fermer le volet Utilisateur.

## Présentation du contenu modal {#section_oxm_kgz_y1b}

Chaque élément de contenu répertorié affiche les informations d'aperçu, y compris le site où il a été publié et son auteur. La sélection d'un élément affiche l'ensemble du contenu, y compris les médias.

>[!NOTE]
>
>Le contenu Livefyre natif affiche plus d'informations que le contenu ajouté à votre application par le biais de flux ou d'autres sources de réseaux sociaux.

Les informations suivantes s'affichent lorsque vous sélectionnez un élément :

* **[!UICONTROL Time in Queue:]** indique la durée d'ajout de l'élément de contenu à modq.
* **[!UICONTROL App name:]** l'application dans laquelle le contenu apparaît. Liens vers le site avec l'application.
* **[!UICONTROL Content Body:]** le texte et la vignette du média, le cas échéant.
* **[!UICONTROL Status:]** l'état actuel du contenu (En attente, Enfoncé, etc.).
* **[!UICONTROL Author information:]** nom et nom d'utilisateur de l'auteur.
* **[!UICONTROL Timestamp:]** horodatage relatif de la création du contenu. Permalinks à l'élément de contenu de la page de contenu de l'application Studio.
* **[!UICONTROL Flag Type:]** Outrage, Désaccord, Indésirable, etc.

   * INDICATEURS SAFE : Indésirable et bloc.
   * Indicateur appliqué par votre réseau et votre liste de profil du site : Profility.
   * Indicateurs appliqués par SAFE : Hate speech, PII (Personal Identification Information), Injurt et Profanity.
   * Indicateurs d'utilisateur : Indésirable, Hors rubrique, Offensif et Accord.

* **[!UICONTROL Flag origin:]** source de l'indicateur répertorié. Peut être SAFE, un nom d'utilisateur ou Livefyre.
* **[!UICONTROL More info:]** répertorie les détails du contenu, y compris le nombre de mentions J'aime, d'indicateurs d'utilisateur, de réponses et de toutes les balises appliquées au contenu. Cliquer sur le site ouvre la page de niveau supérieur du site sur lequel se trouve le contenu. Cliquez sur l'horodatage pour afficher une vue threads du contenu en contexte sur la page.

## Options de filtre dans le modq {#section_r2c_qc2_yy}

Cliquez **[!UICONTROL Filter]** sur dans le coin supérieur gauche de la fenêtre modq pour ouvrir un panneau contenant les options de filtrage disponibles pour le contenu répertorié. A mesure que vous sélectionnez les options, modq se met automatiquement à jour afin de répertorier uniquement le contenu filtré. Cliquez pour **[!UICONTROL Clear filters]** effacer toutes les options sélectionnées et rechargez la liste complète des éléments.

Différentes options de filtre sont disponibles pour les onglets **[!UICONTROL Items]** et les **[!UICONTROL Streams Premoderation]** onglets.

Les options suivantes sont disponibles pour le modq sous les deux **[!UICONTROL Items]** et **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Utilisez le champ Rechercher les applications pour filtrer les résultats par application. Plusieurs applications peuvent être sélectionnées.
* **[!UICONTROL System Flags]**. Filtrez le contenu selon des règles telles que les règles Indésirable, Profility, SAFE et Prémodération.

   * Si vous sélectionnez cette option **[!UICONTROL Spam]** , tout le contenu balisé comme indésirable par SAFE est répertorié.
   * La sélection **[!UICONTROL Profanity]** répertorie tout le contenu balisé Profane par votre réseau ou Liste du profil du site.
   * La sélection **[!UICONTROL SAFE]** répertorie tout le contenu entrant dans modq à la suite de vos règles SAFE.
   * La sélection **[!UICONTROL Premoderation]** répertorie tout le contenu balisé pour la prémodération par votre réseau, votre diffusion en continu ou vos paramètres d'application.

* **[!UICONTROL User Flags]** Filtrage du contenu par indicateurs utilisateur. Les options incluent Outrage, Indésirable, Hors rubrique et Accord.
* **[!UICONTROL Rights Requests.]** Affichez uniquement le contenu avec des droits accordés en cochant la case.
* **[!UICONTROL Entered the queue.]** Filtrez le contenu selon la période pendant laquelle le contenu a été envoyé à modq. Le contenu d'heure envoyé à modq n'est pas nécessairement le moment où le contenu a été publié sur son application.

Les options suivantes sont disponibles pour le modq sous **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtrez le contenu par la source sociale à partir de laquelle le contenu est issu. Par exemple, les options des sources sociales incluent Twitter, Instagram, Facebook et RSS.

L'option suivante est disponible pour le modq sous **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtrez le contenu selon la recommandation donnée par la recommandation de modération automatisée.

Les illustrations suivantes montrent l'aspect des recommandations de modération dans modq : ![](assets/mod_reco1.png)

La recommandation de modération est indiquée pour le contenu lorsqu'elle est configurée **[!UICONTROL Network Settings > Moderation]** et **[!UICONTROL Network Settings > ModQ]**.

## Actions que vous pouvez utiliser dans modq {#section_h4g_wrn_z1b}

Vous pouvez déterminer les actions à effectuer avec chaque élément de contenu dans le modq.

Sélectionnez l'une des options suivantes :

* **[!UICONTROL Checkbox]** Icône permettant d'approuver le contenu
* **[!UICONTROL Trash can]** Icône permettant d'envoyer le contenu à la corbeille
* **[!UICONTROL Request Rights]** pour demander les droits au contenu du propriétaire du contenu.

   >[!NOTE]
   >
   >Vous ne pouvez pas demander de droits dans modq pour le contenu d'Instagram. Vous devez utiliser la bibliothèque ou le contenu de l'application pour envoyer des demandes de droits pour le contenu d'Instagram.

* **[!UICONTROL Feature and Approve]** pour approuver le contenu et présenter également l'élément de contenu.
* **[!UICONTROL Product Tag and Approve]** pour ajouter un produit depuis votre catalogue de produits au contenu, puis l'approuver.
* **[!UICONTROL Mark as Pending]** pour marquer le contenu comme étant en attente.

>[!NOTE]
>
>Une fois que vous avez corbeille un élément de contenu, l'élément de contenu et toutes les réponses à l'élément de contenu sont définitivement supprimés de modq. Pour placer un élément de contenu avec tendance dans une application, reportez-vous à [la section Ajout d'un élément enfoncé à une application](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Si le contenu est déjà à l'état souhaité, le choix de Corbeille, de Bozo ou d'Approuver confirme l'état et supprime l'élément de la liste. La modération d'un élément de contenu le supprime immédiatement de votre queueet et la désactivera dans les files d'attente des modérateurs.

>[!NOTE]
>
>Le contenu de diffusion peut ne pas être Bozo'd. Le contenu en flux continu supprimera définitivement le flux continu et ne peut pas être annulé.

Une fois le contenu modéré, il sera supprimé du modq du modérateur et son auteur ne peut plus la modifier dans le flux. Si un modérateur ferme un élément ou si un utilisateur supprime son commentaire, il apparaît grisé dans les files d'attente des autres modérateurs en temps réel. Lorsque le contenu est grisé, **[!UICONTROL Clear Moderated]** le bouton s'affiche sur la page, ce qui permet aux modérateurs de le supprimer de leur liste et de conserver leur place sur la page quelle que soit l'activité du modérateur.

## Utilisation de la fonction Corbeille dans modq {#section_tpx_qgz_y1b}

Utilisez la section Paramètres pour sélectionner les options disponibles lorsque le contenu est marqué comme étant enfoncé.

* ****[!UICONTROL Confirm Trash]**** Activez cette option pour exiger que les modérateurs confirment leur action lors de la définition du contenu sur Corbeille. Lorsque cette option est activée, la sélection **[!UICONTROL Trash]** pour le contenu affiche une boîte de dialogue demandant un **[!UICONTROL Reason for Moderation]**champ et offre un champ dans lequel a **[!UICONTROL Note]** peut être saisi.

   (Ce paramètre est disponible **[!UICONTROL only]** au niveau du réseau et s'applique à tous les sites situés sous votre réseau.)

* ****[!UICONTROL Hide Replies]**** Activez cette option pour supprimer automatiquement les réponses lorsqu'un commentaire parent est coupé ou Bozo'd.

## Modification de l'état de l'utilisateur dans modq {#section_tmw_lg1_z1b}

Cliquez sur **[!UICONTROL User actions]** le bouton du panneau Résumé utilisateur pour Couper, Interdire ou Liste blanche.

* **[!UICONTROL Mute:]** vous permet de couper les drapeaux de l'utilisateur qui a marqué l'élément de contenu répertorié. Utilisez cette option pour exclure les drapeaux de l'utilisateur de vos filtres de prémodération. Le contenu qu'ils signalent ne saisira pas modq en raison de l'indicateur et leurs indicateurs ne seront pas inclus dans les règles de marquage.
* **[!UICONTROL Ban:]** vous permet d'exclure l'utilisateur répertorié de votre site ou du réseau. (Seuls les administrateurs Studio ou les gestionnaires d'utilisateurs peuvent interagir avec un utilisateur.)
* **[!UICONTROL Whitelist:]** vous permet de liste blanche pour votre site ou votre réseau. (Seuls les administrateurs Studio ou les gestionnaires utilisateur peuvent créer un réseau liste blanche.)



Applications utilisant modq :

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Révisions](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Commentaires de sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Bouton Télécharger](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

