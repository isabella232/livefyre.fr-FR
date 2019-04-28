---
description: Gestion du contenu sur votre réseau Livefyre.
seo-description: Gestion du contenu sur votre réseau Livefyre.
seo-title: Onglet Contenu de l'application
solution: Experience Manager
title: Onglet Contenu de l'application
uuid: 65 b 23085-2 b 79-4 a 6 f -96 c 9-44 b 421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Onglet Contenu de l&#39;application{#app-content-tab}

Gestion du contenu sur votre réseau Livefyre.

L&#39;onglet Contenu de l&#39;application de votre bibliothèque permet de rechercher et de modérer le contenu publié dans vos applications. **[!UICONTROL App Content]** L&#39;onglet permet de définir plusieurs filtres de recherche avec une recherche à caractère générique pour vous permettre de définir plus rapidement et plus facilement vos paramètres de recherche.

Utilisez l&#39;onglet Contenu de l&#39;application pour :

* Recherche de contenu
* Afficher l&#39;historique du contenu
* Modérer le contenu
* Ajouter une balise
* Contenu des fonctionnalités
* Associer le contenu à des produits du catalogue de produits

Pour plus d&#39;informations sur la modération du contenu à l&#39;aide de l&#39;onglet Contenu de l&#39;application, voir [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Recherche générique {#section_jvr_ntm_zz}

Les champs de recherche Livefyre prennent en charge les caractères génériques qui vous permettent d&#39;ajouter un astérisque (*) aux mots (ou fragments de mots) pour capturer des correspondances partielles.

Par exemple :

* ball renvoie uniquement ball
* ball * renvoie ball et ballon
* * ball renvoie ball et football
* * ball * renvoie ball et uniforme et snowball

## Recherche de contenu {#section_fw1_mtm_zz}

Le panneau Contenu de l&#39;application permet de limiter la recherche à l&#39;aide de plusieurs options de filtrage de contenu différentes.

![](assets/PublishedState-1024x367.png)

Utilisez la **[!UICONTROL Quick Filters]** conversion pour restreindre le contenu renvoyé à **[!UICONTROL All Content]****[!UICONTROL All Sidenotes]****[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]** ou **[!UICONTROL Pending]****[!UICONTROL Rights Requests]** à l&#39;état. Sélectionnez ensuite **[!UICONTROL Filter by]** une option, puis utilisez les cases à cocher ou les champs d&#39;entrée disponibles pour restreindre la recherche.

Utilisez le menu déroulant pour trier le contenu de la liste par **[!UICONTROL Newest]**, **[!UICONTROL Oldest]****[!UICONTROL Recently updated]****[!UICONTROL Most flags]** ou **[!UICONTROL Most liked]**.

## Filtrage par options {#section_aqn_xqm_zz}

Utilisez **[!UICONTROL Filter by]** la barre pour filtrer selon les options suivantes :

* **Etat** Vous permet de filtrer en fonction de l&#39;état de modération actuel du contenu : ** [!UICONTROL All Content]** **[!UICONTROL Approved]**, **[!UICONTROL Pending]** ou **[!UICONTROL Bozo]**.

* **Source** Vous permet de filtrer par source du contenu. Sélectionnez **[!UICONTROL Livefyre]** cette option pour répertorier le contenu généré par l&#39;utilisateur publié directement dans le flux. Sélectionnez **[!UICONTROL Facebook]** ou **[!UICONTROL Twitter]****[!UICONTROL RSS]** pour inclure le contenu extrait dans vos applications à partir de ces sources.

* **Les indicateurs** de sélection d&#39;indicateurs vous permettent de filtrer par **[!UICONTROL User Flags]** (indésirable, hors rubrique, injurieux ou non), **[!UICONTROL System Flags]** appliqués par SAFE (Profanity, Spam ou Modérément modéré) ou **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Date/Heure** Vous permet de pointer par moment où le contenu a été initialement **[!UICONTROL Created]** (ou extrait dans l&#39;application par le biais de la synchronisation de socialync ou d&#39;un flux) ou de la dernière **[!UICONTROL Modified]** (modifié, marqué ou l&#39;état modifié).

* **Auteur** Vous permet de filtrer par **[!UICONTROL IP]** adresse de l&#39;auteur ( **[!UICONTROL Display Name]** situé dans le panneau Utilisateurs ou depuis le contenu publié par l&#39;auteur) ou **[!UICONTROL User ID]**(situé dans le panneau Utilisateurs).

* **Contains** Permet de filtrer les 90 jours de contenu les plus récents par **[!UICONTROL Keyword]** ou **[!UICONTROL Content Tag]**. Cochez la **[!UICONTROL Media]** case permettant de renvoyer uniquement le contenu contenant le média. (Pour rechercher tout le contenu, faites défiler l&#39;ensemble du contenu de la liste, puis cliquez **[!UICONTROL Search full data]** sur.)

   **Remarque :** La recherche de plusieurs mots-clés et balises de contenu n&#39;est pas prise en charge. Si plusieurs mots-clés ou balises sont entrés, le dernier mot est utilisé pour la recherche.

   Lors de la recherche par balise de contenu, les balises suggérées sont automatiquement renseignées lorsque vous tapez dans le champ de recherche. Les résultats de la recherche renvoient tout le contenu auquel la balise a été affectée. (Utilisez ce champ pour rechercher du contenu incitatif ou cliquez sur l&#39; **[!UICONTROL Featured]** étiquette d&#39;un contenu incitatif dans Studio.)

   **Remarque :** Utilisez un signe moins (-) avant un nom de balise pour rechercher le contenu qui n&#39;inclut pas cette balise. Par exemple : Recherchez « -miley » pour rechercher tout le contenu qui n&#39;inclut pas la balise « Miley ».

* **Application** Vous permet de filtrer par **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]** ou ID **parent**. Le filtrage par ID parent renvoie tout le contenu qui correspond à une réponse à l&#39;ID de contenu d&#39;entrée. (Filtrez par balises multiples en saisissant des balises séparées par une virgule).

* **Rights** Allows You to filter by Rights Requests status : ** [!UICONTROL Requested]** **[!UICONTROL Granted]**, **[!UICONTROL Replied]** ou **[!UICONTROL Expired]**.

## Bozo Content {#section_afl_vqm_zz}

Dans les applications, **[!UICONTROL Bozo]** le contenu s&#39;affiche uniquement pour l&#39;auteur du contenu. Cela permet à l&#39;utilisateur de croire que son contenu a été approuvé, tout en le masquant auprès de tous les autres utilisateurs et modérateurs.

>[!NOTE]
>
>Le contenu Social provenant de socialsync ou de flux **[!UICONTROL cannot]** est défini sur Bozo.

Vous pouvez utiliser un contenu Bozo pour les raisons suivantes :

* Le contenu identifié comme indésirable par SAFE est automatiquement défini sur l&#39;état Bozo.
* Tous les contenus d&#39;Utilisateurs interdits sont automatiquement définis sur Bozo.
* Le contenu peut être marqué comme Bozo depuis Studio.
* Les modérateurs peuvent utiliser un contenu bozo directement dans le flux.

## Afficher l&#39;historique du contenu {#section_ayz_tqm_zz}

Le panneau de contenu vous permet de vérifier l&#39;historique de tout le contenu répertorié, y compris la prémodération, le filtrage des messages indésirables, la date de publication et les indicateurs ou remarques associés à l&#39;article.

Utilisez les onglets au bas du panneau de contenu pour afficher son historique.

* **[!UICONTROL More Info:]** répertorie toutes les activités sur ce contenu, y compris l&#39;envoi, la modification, la vérification des messages indésirables, la modification d&#39;état et les remarques. L&#39;ID de contenu Livefyre et l&#39;adresse IP de l&#39;utilisateur sont également affichés dans cette section.
* **[!UICONTROL Replies:]** répertorie un maximum de 6 réponses. Cliquez sur **[!UICONTROL Show all replies]** pour afficher toutes les réponses à la publication.

* **[!UICONTROL Flags & Reports:]** répertorie tous les indicateurs d&#39;utilisateur, avec l&#39;avatar de l&#39;utilisateur qui a marqué le contenu et les rapports (notes ajoutées par l&#39;utilisateur lors du marquage du contenu).
* **[!UICONTROL Add a note:]** vous permet d&#39;ajouter une note visible pour d&#39;autres administrateurs ou modérateurs.
* **[!UICONTROL Request Rights:]** ouvre **[!UICONTROL New Rights Request]** la boîte de dialogue, à partir de laquelle une demande de droits peut être émise.

* ****[!UICONTROL Save as Asset:]ouvre **[!UICONTROL Advanced Options]** la boîte de dialogue qui vous permet d&#39;enregistrer l&#39;élément sélectionné dans votre bibliothèque de fichiers, de le publier dans une application ou de demander des droits de réutilisation à son auteur.

![](assets/PublishedMoreInfo-1024x462.png)

## Ajouter une balise au contenu {#section_xb4_mxr_rdb}

Le balisage du contenu vous permet de classer et d&#39;organiser le contenu pour faciliter la récupération et la personnalisation des styles, ou encore marquer le contenu comme indiqué.

Pour ajouter des balises, il vous suffit de cliquer sur l&#39;icône Plus ( **[!UICONTROL +]**) sous Contenu. Entrez une nouvelle balise ou sélectionnez-la dans la liste des balises existantes.

![](assets/PublishedAddTag-1024x338.png)

## Recherche d&#39;images dans tous les fichiers {#section_zxf_hsf_wcb}

Une fois que vous avez ajouté le contenu à la bibliothèque, vous pouvez effectuer des recherches dans le contenu par balises intelligentes.

Dans la bibliothèque, sous Tous les fichiers, vous pouvez rechercher des images existantes en cliquant sur **[!UICONTROL Show Filters]** puis sur :

* Saisie du texte à rechercher dans le champ de recherche
* Tri par pertinence
* Saisie du texte dans **[!UICONTROL Tags]** le champ pour effectuer une recherche par balises dynamiques. L&#39;algorithme de classement des balises intelligent filtre le contenu à l&#39;aide d&#39;un score de confiance des balises intelligentes, de la nouvelle taille du contenu et du nombre d&#39;étoiles que l&#39;utilisateur a attribué au contenu.

## Contenu incitatif {#section_emb_kqm_zz}

Sélectionnez **[!UICONTROL Featured]** la balise par défaut pour marquer le contenu comme indiqué et mettez-la en évidence pour vos utilisateurs. Une fois balisé, utilisez des options de style personnalisées pour personnaliser le contenu incitatif dans vos applications.

## Pour présenter ou annuler la fonctionnalité du contenu {#section_ojx_3qm_zz}

* A partir de Studio, cliquez sur **[!UICONTROL +]** le signe en regard d&#39;un élément de contenu, sélectionnez la **[!UICONTROL Featured]** balise dans la liste déroulante et cliquez **[!UICONTROL Enter]** sur le contenu de la fonctionnalité. La balise sera enregistrée et affichée à côté de l&#39;élément de contenu.

* Pour annuler la fonctionnalité, cliquez sur la **[!UICONTROL x]****[!UICONTROL Featured]** balise affichée sur l&#39;élément de contenu.

* Dans un commentaires, un blog en direct ou une application de révision, passez la souris sur le contenu que vous souhaitez présenter, puis cliquez **[!UICONTROL Feature]** sur. Pour annuler la fonctionnalité, passez la souris sur le contenu et cliquez **[!UICONTROL Unfeature]** sur.

>[!NOTE]
>
>En raison des contraintes d&#39;espace, le contenu de la messagerie peut uniquement être incitatif ou non utilisé dans Studio et peut ne pas être présenté à partir de l&#39;application elle-même.

## Modification du contenu incitatif {#section_pyw_hqm_zz}

La plupart des actions courantes sur le contenu peuvent être exécutées sur le contenu incitatif, à l&#39;exception des actions suivantes :

* Le contenu incitatif ne peut pas être marqué.
* Les utilisateurs ne peuvent pas modifier leur contenu une fois qu&#39;ils ont été présentés, bien qu&#39;ils puissent toujours le supprimer s&#39;ils le souhaitent. Les modérateurs peuvent modifier le contenu incitatif.

