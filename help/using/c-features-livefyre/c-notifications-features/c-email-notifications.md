---
description: Permet aux utilisateurs de sélectionner leur fréquence et leur contenu.
seo-description: Permet aux utilisateurs de sélectionner leur fréquence et leur contenu.
seo-title: Notifications électroniques
solution: Experience Manager
title: Notifications électroniques
uuid: 27 dad 133-bd 8 d -4949-8146-1254 c 160 d 3 af
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Notifications électroniques{#email-notifications}

Permet aux utilisateurs de sélectionner leur fréquence et leur contenu.

**Activez les notifications par courrier électronique pour vos utilisateurs et modérateurs.**

Les applications Livefyre permettent d'activer des notifications par courrier électronique pour vos utilisateurs et modérateurs, en fonction des actions spécifiques. Les notifications sont basées sur le moment où le contenu est publié sur le flux, ce qui permet aux utilisateurs de rester impliqués dans des conversations qu'ils aiment et d'être averti lorsqu'un utilisateur aime ou répond à l'un de ses commentaires.

Les utilisateurs et les modérateurs peuvent choisir d'inclure ou non les notifications par courrier électronique et de définir la fréquence de réception des courriers électroniques. Cette section décrit comment configurer et personnaliser ces notifications par courrier électronique.

* Options de courrier électronique utilisateur : options de notification utilisateur disponibles.
* Options de courrier électronique du modérateur : options de notification du modérateur disponibles.
* Options de courriel d'identité Livefyre : courriers électroniques envoyés dans le cadre de Livefyre Identity. Ces courriers électroniques ne concernent que les clients Livefyre Identité.
* Synchronisation des données avec Livefyre : maintenance de la synchronisation des préférences avec Livefyre.
* Personnalisation des courriels : personnalisations de courrier électronique disponibles.

Utilisez **les options Paramètres > Paramètres d'intégration > Configuration** de la notification par courriel pour personnaliser les notifications par courrier électronique de votre réseau.

>[!NOTE]
>
>Pour vous assurer que les utilisateurs ne reçoivent pas de message indésirable, aucune notification par courrier électronique n'est envoyée de l'environnement UAT Livefyre.

**Options de courriel utilisateur**

Livefyre permet aux utilisateurs de recevoir des notifications par courrier électronique de l'activité du site. Utilisez les paramètres d'intégration Profil utilisateur fournis avec Livefyre pour permettre aux utilisateurs de sélectionner leurs préférences pour les calendriers de notification.

>[!NOTE]
>
>Les courriels sont envoyés uniquement pour le contenu publié manuellement dans le flux, et non pour le contenu extrait de socialsync.

Pour autoriser les utilisateurs à définir leurs préférences de notification, insérez une section Notification par courriel dans les Paramètres utilisateur pour votre système de profils utilisateur. Ajoutez les champs correspondants à votre schéma de base de données de profil utilisateur, puis gérez vos paramètres utilisateur à l'aide de Ping for Pull. (Avec votre gestionnaire d'intégration technique, définissez les fréquences par défaut pour votre réseau. Si vous êtes client de profils d'entreprise, transmettez la valeur par défaut sélectionnée à votre équipe Livefyre pour la configuration dans la base de données Livefyre.)

Les utilisateurs de votre site peuvent ensuite suivre une conversation et commencer à recevoir des notifications par courrier électronique en cliquant sur le **[!UICONTROL +Follow]** bouton dans l'éditeur de commentaires. Les préférences de notification sont définies au niveau du réseau Livefyre. Tous les paramètres utilisateur s'appliquent à tous les sites et conversations sur votre réseau.

**Valeurs par défaut recommandées**

* Un commentaire dans une conversation que je suis après : ** digest digest**
* Quelqu'un aime l'un de mes commentaires : ** digest digest**
* Quelqu'un répond à l'un de mes commentaires : ** immédiatement**
* Suivez les conversations automatiquement lorsque je laisse un commentaire : ** off** (désactivé)

**Remarque**: Les notifications électroniques sont basées sur le contenu de l'heure approuvée pour être incluses dans le flux.

Livefyre propose deux options de fréquence d'e-mail :

* Immédiatement
* Résumé horaire

**Immédiatement**

Les courriers électroniques envoyés immédiatement affichent le texte de la publication, le titre de l'article, le nom d'utilisateur de l'auteur et un **lien de réponse** qui dirige l'utilisateur vers le contenu de la page. Ces courriers électroniques incluent également un lien **de désabonnement** dans le pied de page, ce qui permet aux utilisateurs de se désabonner des notifications par courrier électronique pour cette collection. En cliquant** unsubscribe**, vous les conduirez vers une page de confirmation leur indiquant qu'ils ont été désabonné de la collection.

**Résumé horaire**

Les courriers électroniques envoyés au cours d'un résumé horaire affichent tout le contenu, les réponses au contenu et j'aime sur le contenu de la dernière heure (par exemple) par application que l'utilisateur suit. Si l'utilisateur suit plusieurs applications sur votre réseau, il reçoit un courrier électronique digest pour chaque application.

>[!NOTE]
>
>Dans les conversations sans nouveau contenu pendant plus de plusieurs heures, les utilisateurs dont le digest est activé par heure reçoivent immédiatement une notification lors d'une publication de contenu.

**Options de courriel du modérateur**

Les modérateurs peuvent choisir de recevoir des courriers électroniques pour le contenu publié dans une application, et pour les commentaires marqués comme indésirable ou injurieux dans une application qu'ils modérent. **Remarque :** Aucun courriel ne sera envoyé lorsque les utilisateurs signalent un commentaire avec Accord ou Hors rubrique, car ces catégories ne sont pas considérées comme importantes pour la notification du modérateur.

Les champs Modérateur_ commentaires et Modérateur_ indicateurs doivent également être ajoutés au schéma de base de données des pages de votre modérateur pour permettre à vos modérateurs de mettre à jour la fréquence de leurs notifications par courrier électronique et de désactiver le service s'ils le souhaitent. Livefyre recommande de ne **jamais définir ces deux champs de notification par courrier électronique**. Les options incluent **jamais** (par défaut), **immédiatement**et **souvent**.

**Courrier électronique du modérateur (contenu marqué) :**

Lorsque le contenu est marqué dans une application modérée, le courrier électronique envoyé au modérateur affiche le contenu marqué, le nom d'utilisateur qui a marqué le contenu et un lien renvoyant à la page de contenu.

Lorsqu'un utilisateur modifie ses préférences de notification par courrier électronique sur votre site, synchronisez la mise à jour du système de profil distant Livefyre à l'aide de Ping for Pull Livefyre.

**Synchronisation des données avec Livefyre**

## Personnalisation des courriels {#section_jxb_c5k_yy}

Plusieurs champs des modèles de notification par courriel peuvent être modifiés en fonction de votre style et de votre marque.

* **[!UICONTROL From Email Address]**

   La « adresse électronique » de toutes les notifications par courrier électronique peut être personnalisée pour être cohérente avec votre marque. Livefyre recommande **noreply@customerdomain.com**, en remplaçant **customerdomainwith**your domain name. (La valeur par défaut est **noreply@livefyre.com**.) Veuillez transmettre votre « adresse électronique » préférée à votre gestionnaire d'intégration technique pour la configuration dans la base de données Livefyre pour votre réseau.

   >[!NOTE]
   >
   >Laissez ce champ vide pour désactiver les notifications par courrier électronique pour votre réseau

* **[!UICONTROL Email Logo]**

   Le logo affiché dans les notifications par courrier électronique peut être personnalisé pour afficher le logo de votre société, plutôt que le logo Livefyre par défaut, à l'aide de l'onglet Identité graphique de la **page Paramètres** réseau de Studio. Cette personnalisation est disponible uniquement au niveau du réseau, et non au niveau du site ; elle est disponible uniquement pour les clients Livefyre payants.

* **[!UICONTROL Custom Templates]**

   Si vous le souhaitez, vous pouvez mettre en œuvre un modèle de courrier électronique entièrement personnalisé. Toutefois, cela nécessitera un effort de développement et peut entraîner des coûts de services professionnels. Pour plus d'informations, contactez votre gestionnaire de compte.



Applications utilisant cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Carte de fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Révisions](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

