---
description: Utilisez l'onglet Modération pour définir des règles de prémodération pour le contenu entrant, y compris les listes de profilité, les règles de marquage et les adresses IP interdites.
seo-description: Utilisez l'onglet Modération pour définir des règles de prémodération pour le contenu entrant, y compris les listes de profilité, les règles de marquage et les adresses IP interdites.
seo-title: Définition - Modération consécutive
solution: Experience Manager
title: Définition - Modération consécutive
uuid: 0 ec 53 fdb -08 c 2-4058-88 cb -2 f 6 f 4 b 56 a 95 b
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Définition - Modération consécutive{#setting-up-moderation}

Utilisez l&#39;onglet Modération pour définir des règles de prémodération pour le contenu entrant, y compris les listes de profilité, les règles de marquage et les adresses IP interdites.

## Fonctionnement de la modération {#section_kyf_gvc_t1b}

Vous pouvez modérer le contenu comme suit :

* Prémodérez automatiquement le contenu afin de filtrer le contenu indésirable en fonction des règles que vous configurez avant de publier le contenu.
* Supprimez ou approuvez manuellement le contenu marqué par la prémodération automatique à l&#39;aide du modq ou du contenu de l&#39;application dans la bibliothèque.
* Identifiez les visiteurs du site qui publient constamment du contenu injurieux pour les empêcher de publier en interdisant des utilisateurs Livefyre spécifiques, des utilisateurs de réseaux sociaux ou des adresses IP.
* Identifiez les personnes et le contenu qui peuvent toujours s&#39;afficher en balisant les utilisateurs ou en désactivant les filtres pour des flux, sites ou réseaux spécifiques.

Vous pouvez automatiquement prémodérer le contenu comme suit :

* Configurez les règles pour marquer automatiquement certains types de contenu :

   * Définissez les règles d&#39;indicateur pour le contenu marqué par les visiteurs du site à l&#39;aide de **[!UICONTROL Settings > Moderation > Rules]**
   * Configuration de règles sécurisées à l&#39;aide de **[!UICONTROL Settings > Moderation > Rules]**
   * Bannissez certains utilisateurs Twitter en utilisant **[!UICONTROL Settings > Streams]**
   * Interdiction des adresses IP à l&#39;aide de **[!UICONTROL Settings > Bans]**
   * Bannissez les régions IP par code de pays par demande. Le contenu interdit sera marqué comme INDÉSIRABLE.

* Créez une liste de mots que vous considérez comme profilés dans la liste Profanity sous **[!UICONTROL Settings > Moderation > Rules]** pour votre réseau ou site.
* Utilisateurs autorisés (toujours autoriser le contenu de ces utilisateurs à s&#39;afficher) en utilisant ou désactivant des filtres pour des flux, sites ou réseaux spécifiques.

Après avoir configuré les listes de profanity, les filtres SAFE et les règles, vous pouvez choisir de prémodérer le contenu et d&#39;appliquer les filtres SAFE dans les flux. Pour plus d&#39;informations, voir Options de règle [de diffusion en continu pour toutes les règles de diffusion en continu](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

Livefyre marque le contenu en tant **[!UICONTROL Approved]** que **[!UICONTROL Pending]****[!UICONTROL Junk]**, etc. selon l&#39;origine du contenu, sa publication et les règles que vous avez configurées dans votre système. Le tableau suivant décrit les actions de Livefyre, en fonction de ces facteurs, en détails.

## Fonctionnement de la modération

| Contenu de : | Envoi de contenu à : | État d&#39;approbation |
|--- |--- |--- |
| Bibliothèque | Application | Contenu approuvé |
| Recherche sociale | Application | Contenu approuvé |
| Règle de diffusion en continu | Application | Le contenu est-il marqué comme indésirable par filtre SAFE ? <br><ul><li>Non - Flux de modération de flux vers l&#39;application</li><li>Oui - Suppression du contenu</li></ul> |
| Bibliothèque | Dossier | Aucun état (dans le dossier, pas publié, pas suivi) |
| Recherche sociale | Dossier | Aucun état (dans le dossier, pas publié, pas suivi) |
| Règle de diffusion en continu | Dossier | Le contenu est-il marqué comme indésirable par filtre SAFE ? <br><ul><li>Non - Aucun état (dans le dossier, pas publié, pas suivi)</li><li>Oui - Suppression du contenu</li></ul> |
| Publication d&#39;application | Application | Le contenu est-il marqué comme indésirable par filtre SAFE ? <br><ul><li>Non - Processus de modération post-application</li><li>Oui - Suppression du contenu</li></ul> |

## Flux de modération de flux vers l&#39;application {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Avant que le contenu d&#39;un flux ne soit publié dans une application, Livefyre effectue les vérifications suivantes pour déterminer les actions à effectuer :

1. Si SAFE signale le contenu comme indésirable ou déposé, Livefyre tronque le contenu.
1. Si SAFE ne signale pas le contenu comme indésirable, Livefyre vérifie si la prémodération est activée.
1. Si la prémodération est activée, Livefyre marque le contenu comme étant en attente.
1. Si vous configurez les règles modq, Livefyre envoie le contenu à modq.
1. Si la prémodération n&#39;est pas activée, Livefyre vérifie si SAFE BAGGED le contenu.
1. Si SAFE a marqué le contenu, Livefyre approuve le contenu et publie le contenu dans l&#39;application.
1. Si SAFE signale le contenu et que vous n&#39;avez pas configuré de règles SAFE, Livefyre approuve le contenu et publie le contenu dans l&#39;application.
1. Si SAFE signale le contenu et que vous configurez les règles SAFE, Livefyre vérifie si vous configurez les règles SAFE pour le flux.
1. Si vous configurez des règles SAFE pour le flux, Livefyre approuve le contenu et le publie dans l&#39;application. Si vous n&#39;avez pas configuré de règles SAFE pour le flux, Livefyre utilise les règles de modération SAFE pour déterminer comment traiter le contenu (envoyer à modq, Corbeille, etc.).

## Processus de modération post-application {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Avant que le contenu d&#39;une publication d&#39;application ne soit publié dans une application, Livefyre effectue les vérifications suivantes pour déterminer les actions à effectuer :

1. Si le filtre SAFE indique que le contenu est déposé, Livefyre abandonne le contenu.
1. Si SAFE ne signale pas le contenu comme déposez, Livefyre vérifie si la prémodération est activée. Si la prémodération est activée, Livefyre marque le contenu comme étant en attente. Si vous définissez les règles modq, Livefyre envoie alors le contenu à modq en tant qu&#39;en attente. Dans le cas contraire, le contenu reste dans un état en attente dans le contenu de l&#39;application dans la bibliothèque.
1. Si la prémodération n&#39;est pas activée, Livefyre vérifie si SAFE BAGGED le contenu. Dans le cas contraire, Livefyre approuve le contenu et le publie dans l&#39;application.
1. Si SAFE signale le contenu et que vous configurez les règles SAFE, Livefyre utilise la règle SAFE pour déterminer comment traiter le contenu (envoyer à modq, Corbeille, etc.). Si SAFE signale le contenu et que vous n&#39;avez pas configuré de règles SAFE, Livefyre approuve le contenu et publie le contenu dans l&#39;application.

## Filtres en vrac {#section_lyk_ktx_vy}

Le filtre en vrac recherche le contenu répétitif publié sur tous les réseaux Livefyre dans une courte période. S&#39;il est détecté, ce contenu est signalé comme Bloc, puis coupé par défaut. Alors que le contenu en vrac peut être généré par l&#39;utilisateur (par exemple, « Le contact !  » » publié à plusieurs reprises dans une conversation au cours d&#39;un jeu de football populaire), la plupart d&#39;entre elles sont associées à des campagnes de messages indésirables. Ce filtre est indépendant de la langue et fonctionne avec n&#39;importe quelle langue. Pour personnaliser le filtre en vrac, vous devez contacter la prise en charge de Livefyre.

## Règles {#section_gqz_ksk_f1b}

Utilisez la section Règles pour créer des règles de pré-modération basées sur les indicateurs de sécurité et d&#39;utilisateur. Ce panneau propose deux types de règles :

* **[!UICONTROL Flag Rules:]** spécifiez une action qui doit être effectuée sur un commentaire marqué par les utilisateurs un nombre défini de fois.
* ****[!UICONTROL SAFE Rules:]combine des indicateurs SAFE avec des actions à prendre sur le contenu marqué.

Pour créer des règles d&#39;indicateur, sélectionnez l&#39;indicateur (Offensif, Rubrique, Exclusion ou Indésirable), entrez le nombre de fois qu&#39;il doit être appliqué à un élément de contenu et sélectionnez l&#39;action à exécuter. Vous pouvez définir une règle d&#39;indicateur pour chaque option d&#39;indicateur (Offensive, Rubrique désactivée, Non-respect ou Indésirable).

Vous pouvez créer des règles aux niveaux Réseau, Site et Flux. Les règles de niveau site héritent des règles réseau, sauf si vous configurez les règles du site différemment. Les règles de diffusion en continu héritent des règles du site, sauf si vous les configurez différemment.

Actions disponibles :

* ****[!UICONTROL Trash it:]envoie le commentaire marqué à la corbeille.
* **[!UICONTROL Bozo it:]** masque le commentaire marqué de tous les utilisateurs, à l&#39;exception de son auteur, auquel il reste visible.
* **[!UICONTROL Pending:]** définit le contenu comme étant en attente. Si vous définissez la prémodération sur ON sous **[!UICONTROL Settings > ModQ]**, elle se trouvera dans le modq. Sinon, il ne sera disponible que dans le contenu de l&#39;application.

>[!NOTE]
>
>Livefyre vous recommande de créer des règles aux commentaires Bozo signalés comme indésirable ou offensif par cinq utilisateurs.

## Recommandations de modération {#section_ec3_vr3_2cb}

Vous pouvez utiliser des recommandations de modération pour vous aider à déterminer comment modérer le contenu publié par les visiteurs du site dans les applications Livefyre. L&#39;indicateur de recommandation de modération recommande le moment où un élément de contenu est susceptible d&#39;être coupé, en fonction des actions que vous avez précédemment entreprises sur du contenu similaire. Pour utiliser les recommandations de modération :

1. Activez la fonctionnalité Recommandations de modération en contactant votre assistance technique Adobe Livefyre.
1. Configuration des recommandations de modération dans Paramètres réseau.

   Configurez les recommandations de modération à l&#39;aide du **[!UICONTROL Livefyre Recommends Trash]** paramètre sous **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Configurez une règle SAFE pour indiquer à Livefyre ce que vous devez faire avec le contenu que la recommandation de modération identifie comme contenu susceptible d&#39;être tronqué. Pour plus d&#39;informations sur la configuration d&#39;une règle SAFE pour l&#39; **[!UICONTROL Livefyre Recommends Trash]** option, voir [Modération](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Utilisez le **[!UICONTROL Moderation Recommendation Indicator]** paramètre modq ou Contenu de l&#39;application pour filtrer le contenu que la recommandation de modération identifie comme susceptible d&#39;être tronquée.

   Dans modq, l&#39;indicateur ressemble à ceci : ![](assets/mod_reco1.png)

   Pour plus d&#39;informations sur l&#39;utilisation des recommandations de modération pour modérer le contenu dans modq, voir [modq](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   Dans le contenu de l&#39;application, les recommandations de modération se présentent comme suit : ![](assets/modreco3.png)

   Pour plus d&#39;informations sur l&#39;utilisation des recommandations de modération dans le contenu de l&#39;application, voir [Modération du contenu à l&#39;aide du contenu de l&#39;application](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).
