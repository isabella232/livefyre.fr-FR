---
description: Gestion du contenu sur votre réseau Livefyre.
seo-description: Gestion du contenu sur votre réseau Livefyre.
seo-title: Onglet Contenu de l’application
solution: Experience Manager
title: Onglet Contenu de l’application
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Onglet Contenu de l’application{#app-content-tab}

Gestion du contenu sur votre réseau Livefyre.

L’onglet Contenu de l’application dans votre bibliothèque vous permet de rechercher et de modérer le contenu publié dans vos applications. L' **[!UICONTROL App Content]** onglet permet à plusieurs filtres de recherche avec des caractères génériques de définir plus rapidement et plus facilement vos paramètres de recherche.

Utilisez l’onglet Contenu de l’application pour :

* Rechercher du contenu
* Afficher l’historique du contenu
* Modération du contenu
* Ajouter une balise
* Contenu des fonctionnalités
* Association de contenu aux produits du catalogue de produits

Pour plus d’informations sur la manière de modérer le contenu à l’aide de l’onglet Contenu de l’application, voir [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Recherche de caractères génériques {#section_jvr_ntm_zz}

Les champs de recherche Livefyre prennent en charge les caractères génériques, ce qui vous permet d’ajouter un astérisque ( * ) aux mots (ou fragments de mot) pour récupérer des correspondances partielles.

Par exemple :

* balle ne renvoie que balle
* le ballon* renvoie le ballon et le ballon
* *la balle retourne la balle et le football
* *ball* retourne le ballon et l'uniball et la neige

## Rechercher du contenu {#section_fw1_mtm_zz}

Le panneau Contenu de l’application vous permet de limiter votre recherche à l’aide de plusieurs options de filtrage de contenu différentes.

![](assets/PublishedState-1024x367.png)

Utilisez la **[!UICONTROL Quick Filters]** liste déroulante pour restreindre le contenu renvoyé à **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** ou à **[!UICONTROL Rights Requests]** l’état. Sélectionnez ensuite une **[!UICONTROL Filter by]** option et utilisez les cases à cocher ou les champs de saisie disponibles pour restreindre votre recherche.

Utilisez le menu déroulant pour trier le contenu de la liste par **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]** ou **[!UICONTROL Most flags]** **[!UICONTROL Most liked]**.

## Filtrage par options {#section_aqn_xqm_zz}

Utilisez la **[!UICONTROL Filter by]** barre pour filtrer selon les options suivantes :

* **Etat** Vous permet de filtrer selon l’état de modération actuel du contenu :** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]** ou **[!UICONTROL Bozo]**.

* **Source** Permet de filtrer selon la source du contenu. Sélectionnez cette option **[!UICONTROL Livefyre]** pour répertorier le contenu généré par l’utilisateur publié directement dans le flux. Sélectionnez **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** ou **[!UICONTROL RSS]** incluez le contenu extrait dans vos applications à partir de ces sources.

* **Indicateurs** La sélection d’indicateurs vous permet de filtrer par **[!UICONTROL User Flags]** (indésirable, hors rubrique, offensant ou en désaccord), **[!UICONTROL System Flags]** appliqué par SAFE (Profanité, Indésirable ou Modéré Magiquement) ou **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Date/Heure** Vous permet de déterminer le moment où le contenu a été initialement **[!UICONTROL Created]** (ou extrait dans l’application via SocialSync ou un flux) ou le dernier **[!UICONTROL Modified]** (modifié, marqué ou l’état modifié).

* **Auteur** Vous permet de filtrer selon l’ **[!UICONTROL IP]** adresse de l’auteur, **[!UICONTROL Display Name]** (dans le panneau Utilisateurs ou au-dessus du contenu publié par l’auteur) ou **[!UICONTROL User ID]**(dans le panneau Utilisateurs).

* **Contient** Permet de filtrer les 90 derniers jours du contenu par **[!UICONTROL Keyword]** ou **[!UICONTROL Content Tag]**. Cochez la **[!UICONTROL Media]** case pour renvoyer uniquement le contenu contenant le média. (Pour rechercher tout le contenu, faites défiler la liste vers le bas, puis cliquez sur **[!UICONTROL Search full data]**.)

   **** Remarque : La recherche de plusieurs mots-clés et balises de contenu n’est pas prise en charge. Si plusieurs mots-clés ou balises sont entrés, le dernier mot sera utilisé pour la recherche.

   Lorsque vous effectuez une recherche par balise de contenu, les balises suggérées sont automatiquement renseignées lorsque vous entrez dans le champ de recherche. Les résultats de la recherche renvoient tout le contenu auquel la balise a été affectée. (Utilisez ce champ pour rechercher du contenu phare ou cliquez sur l’ **[!UICONTROL Featured]** étiquette d’un contenu phare dans Studio.)

   **** Remarque : Utilisez un signe moins (-) avant le nom d’une balise pour rechercher du contenu qui n’inclut pas cette balise. Par exemple : Recherchez "-Miley" pour rechercher tout le contenu qui n’inclut pas la balise "-Miley".

* **Application** Vous permet de filtrer par **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]** ou ID **** parent. Le filtrage par ID parent renvoie tout le contenu qui est une réponse à l’ID de contenu d’entrée. (Filtrez par plusieurs balises en saisissant des balises séparées par une virgule.)

* **Droits** Vous permet de filtrer par état Demandes de droits :** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]** ou **[!UICONTROL Expired]**.

## Contenu Bozo {#section_afl_vqm_zz}

Dans les applications, **[!UICONTROL Bozo]** le contenu s’affiche uniquement à l’auteur du contenu. Cela permet à l’utilisateur de croire que son contenu a été approuvé, tout en le masquant à tous les autres utilisateurs et modérateurs.

>[!NOTE]
>
>Le contenu social provenant de SocialSync ou de Streams **[!UICONTROL cannot]** doit être défini sur Bozo.

Vous pouvez utiliser du contenu Bozo pour les raisons suivantes :

* Le contenu identifié comme indésirable par SAFE est automatiquement défini sur l’état Bozo.
* Tout le contenu des utilisateurs interdits est automatiquement défini sur Bozo.
* Le contenu peut être marqué Bozo depuis Studio.
* Les modérateurs peuvent Bozo du contenu directement dans le flux.

## Afficher l’historique du contenu {#section_ayz_tqm_zz}

Le panneau de contenu vous permet de consulter l’historique de tout le contenu répertorié, y compris la prémodération, le filtrage des messages indésirables, la date de publication et les indicateurs ou notes utilisateur affectés à l’élément.

Utilisez les onglets situés dans la partie inférieure du panneau de contenu pour afficher son historique.

* **[!UICONTROL More Info:]** répertorie toutes les activités sur ce contenu, y compris l’envoi, la modification, la vérification des messages indésirables, la modification de l’état et les notes. L’ID de contenu Livefyre et l’adresse IP de l’utilisateur sont également affichés dans cette section.
* **[!UICONTROL Replies:]** répertorie un maximum de 6 réponses. Cliquez sur **[!UICONTROL Show all replies]** pour afficher toutes les réponses à la publication.

* **[!UICONTROL Flags & Reports:]** répertorie tous les indicateurs d’utilisateur, avec l’avatar de l’utilisateur qui a marqué le contenu et tous les rapports (notes ajoutées par l’utilisateur lors du marquage du contenu).
* **[!UICONTROL Add a note:]** vous permet d’ajouter une note visible par d’autres administrateurs ou modérateurs.
* **[!UICONTROL Request Rights:]** ouvre la **[!UICONTROL New Rights Request]** boîte de dialogue à partir de laquelle une demande de droits peut être émise.

* **[!UICONTROL Save as Asset:]**ouvre la **[!UICONTROL Advanced Options]** boîte de dialogue qui vous permet d’enregistrer l’élément sélectionné dans votre bibliothèque de fichiers, de le publier sur une application ou de demander des droits de réutilisation à son auteur.

![](assets/PublishedMoreInfo-1024x462.png)

## Ajouter une balise au contenu {#section_xb4_mxr_rdb}

Le balisage de contenu vous permet de classer et d’organiser le contenu pour faciliter la récupération et la personnalisation du style, ou de marquer le contenu comme une fonctionnalité.

Pour ajouter des balises, cliquez simplement sur l’icône Plus ( **[!UICONTROL +]**) sous Contenu. Entrez une nouvelle balise ou sélectionnez-la dans la liste des balises existantes.

![](assets/PublishedAddTag-1024x338.png)

## Recherche d’images dans tous les fichiers {#section_zxf_hsf_wcb}

Une fois que vous avez ajouté le contenu à la bibliothèque, vous pouvez effectuer des recherches dans le contenu par balises actives.

Dans la bibliothèque, sous Tous les fichiers, vous pouvez rechercher des images existantes en cliquant sur **[!UICONTROL Show Filters]** puis sur :

* Saisie de texte à rechercher dans le champ de recherche
* Tri par pertinence
* Saisir du texte dans le **[!UICONTROL Tags]** champ pour effectuer une recherche par balises actives. L’algorithme de classement Balises dynamiques filtre le contenu à l’aide d’un score de confiance des balises actives, de la nouveauté du contenu et du nombre d’étoiles qu’un utilisateur a attribué au contenu.

## Contenu proposé {#section_emb_kqm_zz}

Sélectionnez la **[!UICONTROL Featured]** balise par défaut pour marquer le contenu comme étant présenté et mettez-le en évidence comme important pour vos utilisateurs. Une fois balisé, utilisez les options de style personnalisées pour personnaliser le contenu proposé dans vos applications.

## Pour Fonctionner ou désactiver le contenu {#section_ojx_3qm_zz}

* Dans Studio, cliquez sur le **[!UICONTROL +]** signe en regard d’un élément de contenu, sélectionnez la **[!UICONTROL Featured]** balise dans la liste déroulante, puis cliquez **[!UICONTROL Enter]** sur Fonctionner le contenu. La balise sera enregistrée et affichée à côté de l’élément de contenu.

* Pour désactiver la fonctionnalité, cliquez sur la **[!UICONTROL x]** balise **[!UICONTROL Featured]** affichée sur l’élément de contenu.

* Dans un commentaire, un blog en direct ou une application de révisions, passez la souris sur le contenu que vous souhaitez présenter, puis cliquez sur **[!UICONTROL Feature]**. Pour annuler la fonctionnalité, passez simplement la souris sur le contenu, puis cliquez sur **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>En raison des contraintes d’espace, le contenu de la messagerie instantanée peut uniquement être présenté ou non à l’aide de Studio et ne pas être présenté depuis l’application elle-même.

## Modification du contenu proposé {#section_pyw_hqm_zz}

La plupart des actions régulières sur le contenu peuvent être effectuées sur le contenu proposé, à l’exception des actions suivantes :

* Le contenu proposé ne peut pas être balisé.
* Les utilisateurs ne peuvent pas modifier leur contenu une fois qu’il a été proposé, même s’ils peuvent le supprimer s’ils le souhaitent. Les modérateurs peuvent modifier le contenu phare.

