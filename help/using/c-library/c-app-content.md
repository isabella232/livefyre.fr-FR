---
description: Gestion du contenu sur votre réseau Livefyre.
title: Onglet Contenu de l’application
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
source-git-commit: 600c9712366f5de303de27cf39045beccd4145eb
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Onglet Contenu de l’application{#app-content-tab}

Gestion du contenu sur votre réseau Livefyre.

L’onglet Contenu de l’application de votre bibliothèque vous permet de rechercher et de modérer le contenu publié dans vos applications. Le **[!UICONTROL App Content]** L’onglet active plusieurs filtres de recherche avec recherche par caractères génériques, ce qui vous permet de définir plus rapidement et plus facilement vos paramètres de recherche.

Utilisez l’onglet Contenu de l’application pour :

* Recherche de contenu
* Afficher l’historique du contenu
* Modération de contenu
* Ajouter une balise
* Contenu de la fonctionnalité
* Association de contenu aux produits du catalogue de produits

Pour plus d’informations sur la manière de modérer le contenu à l’aide de l’onglet Contenu de l’application, voir [Modération de contenu à l’aide de l’onglet Contenu de l’application](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Recherche par caractères génériques {#section_jvr_ntm_zz}

Les champs de recherche Livefyre prennent en charge les caractères génériques, qui vous permettent d’ajouter un astérisque ( * ) aux mots (ou fragments de mot) pour capturer des correspondances partielles.

Par exemple :

* la balle renvoie uniquement la balle
* ball* renvoie balle et ballon
* *ballon retourne ballon et football
* *ball* renvoie la balle et l’uniball et la neige

## Recherche de contenu {#section_fw1_mtm_zz}

Le panneau Contenu de l’application vous permet d’affiner votre recherche à l’aide de plusieurs options de filtrage de contenu différentes.

![](assets/PublishedState-1024x367.png)

Utilisez la variable **[!UICONTROL Quick Filters]** Extraction pour limiter le contenu renvoyé à **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** ou **[!UICONTROL Rights Requests]** statut. Sélectionnez ensuite un **[!UICONTROL Filter by]** et utilisez les cases à cocher ou les champs de saisie disponibles pour affiner votre recherche.

Utilisez le menu déroulant pour trier le contenu de la liste par **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** ou **[!UICONTROL Most liked]**.

## Filtrage par options {#section_aqn_xqm_zz}

Utilisez la variable **[!UICONTROL Filter by]** pour filtrer selon les options suivantes :

* **État** Permet de filtrer selon l’état de modération actuel du contenu :** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]** ou **[!UICONTROL Bozo]**.

* **Source** Permet de filtrer selon la source du contenu. Sélectionner **[!UICONTROL Livefyre]** pour répertorier le contenu généré par l’utilisateur publié directement dans le flux. Sélectionner **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** ou **[!UICONTROL RSS]** pour inclure le contenu extrait dans vos applications à partir de ces sources.

* **Indicateurs** La sélection des indicateurs vous permet de filtrer par **[!UICONTROL User Flags]** (Indésirable, hors sujet, Offensive ou Désaccord), **[!UICONTROL System Flags]** appliquée par SAFE (profil, spam ou modération magique) ou **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Date/heure** Permet de filtrer le contenu à l’origine **[!UICONTROL Created]** (ou extrait dans l’application par le biais de SocialSync ou d’un flux), ou le dernier **[!UICONTROL Modified]** (modifié, marqué ou l’état modifié).

* **Auteur** Permet de filtrer selon le **[!UICONTROL IP]** adresse, **[!UICONTROL Display Name]** (dans le panneau Utilisateurs ou au-dessus du contenu publié par l’auteur), ou **[!UICONTROL User ID]**(dans le panneau Utilisateurs).

* **Contient** Permet de filtrer les 90 derniers jours de contenu en fonction des **[!UICONTROL Keyword]** ou **[!UICONTROL Content Tag]**. Sélectionnez la **[!UICONTROL Media]** pour renvoyer uniquement le contenu contenant Media. (Pour rechercher tout le contenu, faites défiler la liste vers le bas, puis cliquez sur **[!UICONTROL Search full data]**.)

   **Remarque :** La recherche de plusieurs mots-clés et balises de contenu n’est pas prise en charge. Si plusieurs mots-clés ou balises sont saisis, le dernier mot est utilisé pour la recherche.

   Lors de la recherche par balise de contenu, les balises suggérées sont automatiquement renseignées lorsque vous entrez dans le champ de recherche. Les résultats de la recherche renvoient tout le contenu auquel la balise a jamais été affectée. (Utilisez ce champ pour rechercher du contenu en vedette ou cliquez sur le bouton **[!UICONTROL Featured]** libellé sur tout contenu présenté dans Studio.)

   **Remarque :** Utilisez un signe moins (-) avant un nom de balise pour rechercher du contenu qui n’inclut pas cette balise. Par exemple : Recherchez &quot;-Miley&quot; pour rechercher tout le contenu qui n’inclut pas la balise &quot;Miley&quot;.

* **Application** Permet de filtrer par **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]** ou **ID parent**. Le filtrage par identifiant parent renvoie tout le contenu qui est une réponse à l’identifiant de contenu d’entrée. (Filtrez par plusieurs balises en saisissant des balises séparées par une virgule.)

* **Droits** Permet de filtrer par état Demandes de droits :** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]** ou **[!UICONTROL Expired]**.

## Contenu Bozo {#section_afl_vqm_zz}

Dans les applications, **[!UICONTROL Bozo]** Le contenu s’affiche uniquement pour l’auteur du contenu. Cela permet à l’utilisateur de croire que son contenu a été approuvé, tout en le masquant à tous les autres utilisateurs et modérateurs.

>[!NOTE]
>
>Contenu social provenant de SocialSync ou de flux **[!UICONTROL cannot]** Sois défini sur Bozo.

Vous pouvez Bozo du contenu pour les raisons suivantes :

* Le contenu identifié comme indésirable par SAFE est automatiquement défini sur l’état de Bozo.
* Tout le contenu des utilisateurs interdits est automatiquement défini sur Bozo.
* Le contenu peut être marqué Bozo depuis Studio.
* Les modérateurs peuvent Bozo du contenu directement dans le flux.

## Afficher l’historique du contenu {#section_ayz_tqm_zz}

Le panneau Contenu vous permet de consulter l’historique de tout le contenu répertorié, notamment la prémodération, le filtrage par courrier indésirable, la date de publication et les indicateurs utilisateur ou notes affectés à l’élément.

Utilisez les onglets au bas du panneau de contenu pour afficher son historique.

* **[!UICONTROL More Info:]** répertorie toutes les activités sur ce contenu, y compris l’envoi, la modification, le contrôle du spam, la modification de l’état et les notes. L’identifiant du contenu Livefyre et l’adresse IP de l’utilisateur sont également affichés dans cette section.
* **[!UICONTROL Replies:]** liste un maximum de 6 réponses. Cliquez sur **[!UICONTROL Show all replies]** pour afficher toutes les réponses à la publication.

* **[!UICONTROL Flags & Reports:]** répertorie tous les indicateurs utilisateur, avec l’avatar de l’utilisateur qui a marqué le contenu, ainsi que tous les rapports (notes ajoutées par l’utilisateur lors du marquage du contenu).
* **[!UICONTROL Add a note:]** vous permet d’ajouter une note visible par d’autres administrateurs ou modérateurs.
* **[!UICONTROL Request Rights:]** ouvre la fonction **[!UICONTROL New Rights Request]** , à partir de laquelle une demande de droits peut être émise.

* **[!UICONTROL Save as Asset:]**ouvre la variable **[!UICONTROL Advanced Options]** qui vous permet d’enregistrer l’élément sélectionné dans votre bibliothèque de ressources, de le publier dans une application ou de demander des droits de réutilisation à son auteur.

![](assets/PublishedMoreInfo-1024x462.png)

## Ajout d’une balise au contenu {#section_xb4_mxr_rdb}

Le balisage de contenu vous permet de classer et d’organiser le contenu pour faciliter la récupération et la personnalisation des styles, ou de marquer le contenu comme présenté.

Pour ajouter des balises, cliquez simplement sur le signe plus ( **[!UICONTROL +]**) sous le contenu. Entrez une nouvelle balise ou effectuez une sélection dans une liste de balises existantes.

![](assets/PublishedAddTag-1024x338.png)

## Recherche d’images dans toutes les ressources {#section_zxf_hsf_wcb}

Une fois que vous avez ajouté le contenu à la bibliothèque, vous pouvez rechercher le contenu par balises intelligentes.

Dans la bibliothèque, sous Toutes les ressources, vous pouvez rechercher des images existantes en cliquant sur **[!UICONTROL Show Filters]** puis :

* Saisie de texte à rechercher dans le champ de recherche
* Tri par pertinence
* Saisie de texte dans le **[!UICONTROL Tags]** champ à rechercher par balises intelligentes. L’algorithme de classement Balises intelligentes filtre le contenu à l’aide d’un score de confiance de balise intelligente, de la nouveauté du contenu et du nombre d’étoiles qu’un utilisateur a attribué au contenu.

## Contenu en vedette {#section_emb_kqm_zz}

Sélectionnez la valeur par défaut **[!UICONTROL Featured]** pour marquer le contenu comme présenté et le mettre en évidence comme important pour vos utilisateurs. Une fois balisé, utilisez des options de style personnalisées pour personnaliser le contenu en vedette dans vos applications.

## Fonctionnalité ou suppression de contenu {#section_ojx_3qm_zz}

* Dans Studio, cliquez sur **[!UICONTROL +]** en regard d’un élément de contenu, sélectionnez l’option **[!UICONTROL Featured]** dans la liste déroulante, puis cliquez sur **[!UICONTROL Enter]** au contenu de la fonctionnalité. La balise est enregistrée et affichée en regard de l’élément de contenu.

* Pour annuler la fonctionnalité, cliquez sur le bouton **[!UICONTROL x]** sur le **[!UICONTROL Featured]** balise affichée sur le contenu.

* Dans une application de commentaires, de blog en direct ou de révisions, passez la souris sur le contenu que vous souhaitez afficher, puis cliquez sur **[!UICONTROL Feature]**. Pour annuler la fonctionnalité, il vous suffit de pointer sur le contenu, puis de cliquer sur **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>En raison de contraintes d’espace, le contenu de la messagerie instantanée peut uniquement être présenté ou non à l’aide de Studio, et peut ne pas l’être dans l’application elle-même.

## Modification du contenu en vedette {#section_pyw_hqm_zz}

La plupart des actions régulières sur le contenu peuvent être effectuées sur le contenu En vedette, à l’exception des actions suivantes :

* Le contenu en vedette ne peut pas être marqué.
* Les utilisateurs ne peuvent pas modifier leur contenu une fois qu’il a été En vedette, bien qu’ils puissent toujours le supprimer s’ils le souhaitent. Les modérateurs peuvent modifier le contenu en vedette.
