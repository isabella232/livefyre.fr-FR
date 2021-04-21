---
description: Utilisez l’onglet Modération pour définir des règles de prémodération pour le contenu entrant, y compris les listes de profil, les règles d’indicateur et les adresses IP interdites.
title: Configuration de la modération
exl-id: 09fc44c4-7ee1-47fd-ae68-885532a6f03f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 0%

---

# Configuration de la modération{#setting-up-moderation}

Utilisez l’onglet Modération pour définir des règles de prémodération pour le contenu entrant, y compris les listes de profil, les règles d’indicateur et les adresses IP interdites.

## Fonctionnement de la modération {#section_kyf_gvc_t1b}

Vous pouvez modérer le contenu de l’une des manières suivantes :

* Prémodérer automatiquement le contenu pour filtrer le contenu indésirable en fonction des règles que vous avez définies avant de le publier.
* Supprimez ou approuvez manuellement le contenu marqué à l’aide de la prémodération automatique à l’aide de ModQ ou du contenu de l’application dans la bibliothèque.
* Identifiez les visiteurs du site qui publient régulièrement du contenu offensant afin de les empêcher de publier en interdisant certains utilisateurs de Livefyre, utilisateurs de réseaux sociaux ou adresses IP spécifiques.
* Identifiez les personnes et le contenu qui peuvent toujours s’afficher en plaçant sur la liste autorisée les utilisateurs ou en désactivant les filtres de flux, de sites ou de réseaux spécifiques.

Vous pouvez prémodérer automatiquement le contenu de l’une des manières suivantes :

* Configurez des règles pour marquer automatiquement certains types de contenu :

   * Configurez les règles d&#39;indicateur pour le contenu marqué par l&#39;indicateur visiteur du site à l&#39;aide de **[!UICONTROL Settings > Moderation > Rules]**
   * Configurez les règles SAFE à l&#39;aide de **[!UICONTROL Settings > Moderation > Rules]**
   * Interdire des utilisateurs Twitter spécifiques à l&#39;aide de **[!UICONTROL Settings > Streams]**
   * Interdire les adresses IP à l&#39;aide de **[!UICONTROL Settings > Bans]**
   * Interdire les régions IP par code de pays sur demande. Le contenu interdit sera signalé comme SPAM.

* Créez une liste de mots que vous considérez comme profanation dans la Liste Profanité sous **[!UICONTROL Settings > Moderation > Rules]** pour votre réseau ou site.
* Placer sur la liste autorisée les utilisateurs (toujours autoriser l’affichage du contenu de ces utilisateurs) en utilisant ou en désactivant les filtres pour des flux, sites ou réseaux spécifiques.

Après avoir configuré vos listes de profanation, filtres SÛR et règles, vous pouvez choisir de modérer le contenu et d’appliquer les filtres SÛR dans les flux. Pour plus d’informations, voir [Options de règle de diffusion pour toutes les règles de diffusion](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

Livefyre marque le contenu comme **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, **[!UICONTROL Junk]**, etc. selon l’origine du contenu, l’emplacement de sa publication et les règles que vous avez configurées dans votre système. Le tableau suivant décrit en détail les actions entreprises par Livefyre, en fonction de ces facteurs.

## Fonctionnement de la modération

| Le Contenu Provient De : | Envoi de contenu à : | Statut d&#39;approbation |
|--- |--- |--- |
| Bibliothèque | Appli | Contenu approuvé |
| Recherche sociale | Appli | Contenu approuvé |
| Règle de diffusion | Appli | Le contenu est-il marqué comme indésirable par le filtre SAFE ? <br><ul><li>Non - Flux de travaux de modération de flux vers l’application</li><li>Oui - Contenu copié</li></ul> |
| Bibliothèque | Dossier | Aucun état (dans le dossier, non publié, pas supprimé) |
| Recherche sociale | Dossier | Aucun état (dans le dossier, non publié, pas supprimé) |
| Règle de diffusion | Dossier | Le contenu est-il marqué comme indésirable par le filtre SAFE ? <br><ul><li>Non - Aucun état (dans le dossier, pas publié, pas supprimé)</li><li>Oui - Contenu copié</li></ul> |
| Publication de l’application | Appli | Le contenu est-il marqué comme indésirable par le filtre SAFE ? <br><ul><li>Non - Processus de modération post-application</li><li>Oui - Contenu copié</li></ul> |

## Flux de travaux de modération de flux vers l’application {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Avant que le contenu d’un flux ne soit publié sur une application, Livefyre effectue les vérifications suivantes pour déterminer ce qu’il faut faire avec le contenu :

1. Si SAFE désigne le contenu comme indésirable ou déposé, Livefyre bloque le contenu.
1. Si SAFE ne désigne pas le contenu comme indésirable, Livefyre vérifie si la prémodération est activée.
1. Si la prémodération est activée, Livefyre marque le contenu comme étant en attente.
1. Si vous définissez des règles ModQ, Livefyre envoie le contenu à ModQ.
1. Si la prémodération n’est pas activée, Livefyre vérifie si SAFE a marqué le contenu.
1. Si SAFE a marqué le contenu, Livefyre approuve le contenu et le publie dans l’application.
1. Si SAFE marque le contenu et que vous n’avez pas défini de règles SAFE, Livefyre approuve le contenu et le publie dans l’application.
1. Si SAFE marque le contenu et que vous définissez des règles SAFE, Livefyre vérifie si vous avez configuré des règles SAFE pour le flux.
1. Si vous définissez des règles SAFE pour le flux, Livefyre approuve le contenu et le publie dans l’application. Si vous n’avez pas défini de règles SAFE pour le flux, Livefyre utilise les règles SAFE de modération pour déterminer comment gérer le contenu (envoyer à ModQ, corbeille, etc.).

## Processus de modération post-application {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Avant que le contenu d’une publication d’application ne soit publié sur une application, Livefyre effectue les vérifications suivantes pour déterminer ce qu’il faut faire avec le contenu :

1. Si le filtre SAFE marque le contenu comme une goutte d&#39;eau, Livefyre supprime le contenu.
1. Si le paramètre SAFE n’indique pas le contenu comme une goutte, Livefyre vérifie si la prémodération est activée. Si la prémodération est activée, Livefyre marque le contenu comme étant en attente. Si vous configurez des règles ModQ, Livefyre envoie alors le contenu à ModQ en attente. Si ce n’est pas le cas, le contenu reste en attente dans Contenu de l’application dans la bibliothèque.
1. Si la prémodération n’est pas activée, Livefyre vérifie si SAFE a marqué le contenu. Dans le cas contraire, Livefyre approuve le contenu et le publie dans l’application.
1. Si SAFE marque le contenu et que vous définissez des règles SAFE, Livefyre utilise la règle SAFE pour déterminer comment gérer le contenu (envoyer à ModQ, corbeille, etc.). Si SAFE marque le contenu et que vous n’avez pas défini de règles SAFE, Livefyre approuve le contenu et le publie dans l’application.

## Filtres en vrac {#section_lyk_ktx_vy}

Le filtre en masse recherche le contenu répétitif publié sur tous les réseaux Livefyre dans un court laps de temps. Si ce contenu est détecté, il est signalé comme étant en bloc, puis détruit par défaut. Bien que le contenu en vrac puisse être généré par l’utilisateur (par exemple, &quot;Touchdown !&quot;) posté à plusieurs reprises dans un Chat lors d&#39;un match de football populaire), la plupart proviennent de campagnes de spam. Ce filtre est indépendant de la langue et fonctionne avec n’importe quelle langue. Pour personnaliser le filtre en vrac, vous devez contacter l’assistance Livefyre.

## Règles {#section_gqz_ksk_f1b}

Utilisez la section Règles pour créer des règles de prémodération basées sur les indicateurs SAFE et appliqués par l’utilisateur. Ce panneau offre deux types de règles :

* **[!UICONTROL Flag Rules:]** spécifiez une action qui doit être exécutée sur un commentaire marqué par les utilisateurs un nombre défini de fois.
* **[!UICONTROL SAFE Rules:]**combiner des indicateurs SAFE avec des actions pour exécuter le contenu marqué.

Pour créer des règles d’indicateur, sélectionnez l’indicateur (Offensive, Off Topic, Disokay ou Spam), entrez le nombre d’applications à appliquer à un élément de contenu et sélectionnez l’action à exécuter. Vous pouvez définir une règle d’indicateur pour chaque option d’indicateur (Offensive, Off Topic, Disokay ou Spam).

Vous pouvez créer des règles aux niveaux Réseau, Site et Flux. Les règles au niveau du site héritent des règles réseau, sauf si vous les configurez différemment. Les règles de diffusion en continu héritent des règles du site, sauf si vous les configurez différemment.

Actions disponibles :

* **[!UICONTROL Trash it:]**envoie le commentaire marqué à la corbeille.
* **[!UICONTROL Bozo it:]** masque le commentaire marqué de tous les utilisateurs, à l’exception de son auteur, à qui il reste visible.
* **[!UICONTROL Pending:]** définit le contenu comme étant en attente. Si vous définissez la prémodération sur ON sous **[!UICONTROL Settings > ModQ]**, elle sera alors dans le ModQ. Sinon, il sera uniquement dans Contenu de l’application.

>[!NOTE]
>
>Livefyre vous recommande de créer des règles pour les commentaires Bozo signalés comme indésirables ou offensants par cinq utilisateurs.

## Recommendations de modération {#section_ec3_vr3_2cb}

Vous pouvez utiliser des recommandations de modération pour déterminer comment modérer le contenu publié par les visiteurs du site dans les applications Livefyre. L’indicateur de recommandation de modération recommande lorsqu’un élément de contenu est susceptible d’être haché, en fonction des actions que vous avez effectuées précédemment sur du contenu similaire. Pour utiliser Modération Recommendations :

1. Activez la fonctionnalité Recommendations de modération en contactant votre professionnel de l’assistance Adobe Livefyre.
1. Configurez les recommandations de modération dans Paramètres réseau.

   Configurez les recommandations de modération en utilisant le paramètre **[!UICONTROL Livefyre Recommends Trash]** sous **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Configurez une règle SAFE pour indiquer à Livefyre ce qu’il faut faire du contenu identifié par la recommandation de modération comme contenu susceptible d’être supprimé. Pour plus d&#39;informations sur la configuration d&#39;une règle SAFE pour l&#39;option **[!UICONTROL Livefyre Recommends Trash]**, voir [Modération](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Utilisez l’**[!UICONTROL Moderation Recommendation Indicator]** dans ModQ ou dans App Content pour filtrer le contenu que la recommandation de modération identifie comme susceptible d’être corrompu.

   Dans ModQ, l’indicateur se présente comme suit :  ![](assets/mod_reco1.png)

   Pour plus d’informations sur l’utilisation de la Recommendations de modération pour modérer le contenu dans ModQ, voir [ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   Dans le contenu de l’application, les recommandations de modération se présentent comme suit :  ![](assets/modreco3.png)

   Pour plus d’informations sur l’utilisation de la Recommendations de modération dans le contenu de l’application, voir [Modération du contenu à l’aide du contenu de l’application](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).
