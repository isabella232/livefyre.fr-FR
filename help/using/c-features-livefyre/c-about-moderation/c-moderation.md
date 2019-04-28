---
description: Le moteur de filtrage des messages indésirables et d'abus Livefyre (SAFE) est un processus d'arrière-plan qui analyse tous les contenus entrants et est activé pour tous les clients Livefyre.
seo-description: Le moteur de filtrage des messages indésirables et d'abus Livefyre (SAFE) est un processus d'arrière-plan qui analyse tous les contenus entrants et est activé pour tous les clients Livefyre.
seo-title: Règles SAFE
title: Règles SAFE
uuid: 2 f 91 d 0 d 4-dffe -4651-88 af -79 bbb 96 c 1 b 5 c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Règles SAFE{#safe-rules}

Le moteur de filtrage des messages indésirables et d&#39;abus Livefyre (SAFE) est un processus d&#39;arrière-plan qui analyse tous les contenus entrants et est activé pour tous les clients Livefyre.



SAFE utilise des règles de modèle ainsi que des modèles statistiques pour détecter les publications indésirables, injuriales, profilées et en masse (répétitives). Vous verrez qu&#39;il est référencé parfois dans d&#39;autres produits Livefyre, notamment les outils de modération de contenu et modq.

>[!NOTE]
>
>SAFE est en anglais uniquement, à l&#39;exception de la classification de publipostage en masse. Si vous avez besoin d&#39;assistance pour d&#39;autres langues, contactez votre gestionnaire de compte stratégique.

## Composants Studio utilisant SAFE {#section_k34_4tx_vy}

Les indicateurs appliqués par SAFE peuvent être utilisés avec les composants Studio suivants :

* Règles

   Vous pouvez définir des règles SAFE pour marquer automatiquement le contenu et définir le mode de traitement du contenu marqué dans **[!UICONTROL Network Settings]** le contenu.

   Par exemple, un site peut définir une tolérance très faible pour Profanity et définir des règles SAFE qui définissent tout le contenu marqué comme Profane comme étant Bozo&#39;d. D&#39;autres sites peuvent définir des règles qui définissent le contenu Profane à prémodérer avant de saisir le flux.

* Modq

   Vous pouvez modérer le contenu marqué par des règles SAFE et d&#39;autres règles de prémodération (par exemple, SPAM, profanity, etc.) dans le modq.

* Contenu de l&#39;application dans la bibliothèque

   Le contenu marqué par SAFE est répertorié dans le **[!UICONTROL Library]** contenu de l&#39;application Contenu de l&#39;application. Vous pouvez filtrer le contenu par indicateur pour modérer le contenu.

## OPTIONS DE FILTRE SAFE {#section_pg5_ttx_vy}

SAFE applique les indicateurs suivants au contenu filtré et peut être utilisé pour créer des règles et modérer le contenu à partir de Livefyre Studio.

* **[!UICONTROL Profanity List]**: Le contenu du profane, tel qu&#39;il est défini par une liste de mots-clés anglais, selon une utilisation courante.

   Le filtre Profanity recherche le profane, en fonction d&#39;une liste de mots testée. S&#39;il est détecté, le contenu est marqué comme Profane.

   >[!NOTE]
   >
   >Livefyre fournit également un second filtre Liste de profility que vous pouvez personnaliser aux niveaux Site et Réseau. Les règles créées avec la liste Profanity sont prioritaires par rapport aux règles automatisées provenant du filtre Profility SAFE. Pour plus d&#39;informations, reportez-vous à la section Liste du profilage de la documentation Paramètres.

* **[!UICONTROL Mild Profanity]**: Les mots et expressions ne sont généralement pas acceptables dans les conversations polite, mais sont généralement acceptables dans les conversations occasionnelles. En règle générale, ces mots et expressions sont autorisés sur la télévision réseau.
* **[!UICONTROL Strong Profanity]**: Une langue très forte, telle que des exposants et des expressions non autorisées sur la télévision réseau et utilisés avec parcimonie dans les films avec classement et la télévision par câble mature. En règle générale, ces mots ne sont pas utilisés par polite ou conversation occasionnelle et sont dits dans une conversation impolite avec un intention de nuire à l&#39;écouteur.
* **[!UICONTROL SPAM]**: Non sollicité, généralement contenu commercial. Il utilise un modèle statistique qui repose sur différentes fonctionnalités (y compris le contenu des commentaires et les URL) pour signaler un fragment de contenu comme INDÉSIRABLE. Vous pouvez ajuster les seuils des messages indésirables pour personnaliser les taux de balisage des messages indésirables pour votre réseau ou votre site, par demande.
* **[!UICONTROL Mild Insult]**: Insulter le contenu, tel que défini par la liste des mots-clés et des modèles de mots.
* **[!UICONTROL Strong Insult]**: Insulter le contenu, tel que défini par la liste des mots-clés et des modèles de mots.
* **[!UICONTROL Hate Speech]**: Insulte basée sur l&#39;ethnicité ou la religion, en particulier lorsque l&#39;appartenance du groupe cible est en minorité ou protégée.
* **[!UICONTROL ALL CAPS]**: Texte présenté en majuscules (lu comme yelling).
* **[!UICONTROL Mild Threat]**: Une menace ou une insulte qui comprend généralement un profilage léger dirigé vers une autre personne. Cette option signale plus souvent les menaces possibles, mais elle présente également un taux de faux positifs plus élevé que **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Une menace ou une insulte grave mentionnant les dommages bodieux à une ou plusieurs personnes, souvent avec un fort profilage. Cette option signale moins de menaces que possible, mais elle présente également un taux de faux positifs inférieur **[!UICONTROL Mild Threat]**à celui de.

* **[!UICONTROL Probable Nudity]**: Image présentant une nudité. Cette option signale moins de nudité, mais elle présente également un taux de faux positifs inférieur **[!UICONTROL Possible Nudity]**à celui de.

* **[!UICONTROL Possible Nudity]**: Image présentant une nudité. Cette option signale plus souvent la nudité, mais elle présente également un taux de faux positifs plus élevé que **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Informations d&#39;identification personnelle) : Informations qui peuvent identifier l&#39;utilisateur. Il peut s&#39;agir d&#39;une adresse électronique, d&#39;une adresse physique, d&#39;un numéro de sécurité sociale (pour les clients E.U.), d&#39;un numéro de carte de crédit, d&#39;un mot de passe ou tout ce qui peut être utilisé dans la fraude ou pour obtenir l&#39;identité d&#39;un utilisateur.
* **[!UICONTROL Livefyre Recommends Trash]**. Définissez l&#39;action que le système effectue lorsque la recommandation de modération automatisée identifie le contenu pour le rejet. ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Pour activer les recommandations de modération, contactez votre assistance technique Adobe Livefyre.

## Gestion du contenu non intercepté par SAFE {#section_pjy_5tx_vy}

Il existe plusieurs moyens pour gérer efficacement le contenu qui n&#39;est pas capturé par ce filtre. Les options ci-dessous sont répertoriées dans l&#39;ordre recommandé du processus.

1. En tant que modérateur, supprimez le contenu du flux.
1. Créez une règle de drapeau indiquant si un élément de contenu est signalé comme indésirable ou offensif par cinq utilisateurs, le définir sur Bozo.
1. Bannissez l&#39;utilisateur qui publie du contenu indésirable, de sorte que tout son contenu passe directement à l&#39;état Bozo.
1. Ajoutez des mots spécifiques qui doivent toujours être filtrés à votre liste de profilances.

>[!NOTE]
>
>Si un modérateur publie le contenu capturé par notre filtre de messages indésirables, il est toujours signalé comme indésirable, mais il est automatiquement approuvé et ne sera pas défini sur Bozo.

Si vous observez des tendances ou des schémas de contenu non intercepté par SAFE, envoyez vos fichiers CSM par courriel avec les ID de commentaires et le texte.



Applications utilisant cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Carte de fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Carte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Révisions](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Commentaires de sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Bouton Télécharger](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

