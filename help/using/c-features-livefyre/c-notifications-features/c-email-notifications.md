---
description: Permet aux utilisateurs de sélectionner leur fréquence de notification et leur contenu.
seo-description: Permet aux utilisateurs de sélectionner leur fréquence de notification et leur contenu.
seo-title: Notifications électroniques
solution: Experience Manager
title: Notifications électroniques
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Notifications électroniques{#email-notifications}

Permet aux utilisateurs de sélectionner leur fréquence de notification et leur contenu.

**Activez les notifications par courrier électronique pour vos utilisateurs et modérateurs.**

Les applications Livefyre vous permettent d’activer les notifications par courrier électronique pour vos utilisateurs et modérateurs, en fonction d’actions spécifiques. Les notifications sont basées sur le moment où le contenu est publié dans le flux, ce qui permet à vos utilisateurs de rester engagés dans des conversations qui les intéressent et d’être avertis lorsqu’un utilisateur aime ou répond à l’un de leurs commentaires.

Les utilisateurs et les modérateurs peuvent s’inscrire ou non à la notification par courriel et peuvent définir la fréquence de réception des courriers électroniques. Cette section décrit comment configurer et personnaliser ces notifications par courrier électronique.

* Options de messagerie de l’utilisateur : options de notification utilisateur disponibles.
* Options de courriel du modérateur : options de notification du modérateur disponibles.
* Options des courriels d'identité Livefyre : e-mails envoyés dans le cadre de Livefyre Identity. Ces courriels ne sont pertinents que pour les clients d’identité Livefyre.
* Synchronisation des données avec Livefyre : synchronisation des préférences avec Livefyre.
* Personnalisation des courriers électroniques : personnalisations de courrier électronique disponibles.

Utilisez les options **Paramètres &gt; Paramètres d’intégration &gt; Configuration** de la notification par courrier électronique pour personnaliser les notifications par courrier électronique pour votre réseau.

>[!NOTE]
>
>Pour vous assurer que vos utilisateurs finaux ne reçoivent pas de courrier indésirable, aucune notification par courrier électronique n’est envoyée depuis l’environnement Livefyre UAT.

**Options de messagerie utilisateur**

Livefyre vous permet de permettre aux utilisateurs de recevoir des notifications par courrier électronique sur l’activité du site. Utilisez les paramètres d’intégration de profil utilisateur fournis par Livefyre pour permettre aux utilisateurs de sélectionner leurs préférences pour les calendriers de notification.

>[!NOTE]
>
>Les courriers électroniques sont envoyés uniquement pour le contenu publié manuellement dans le flux continu, et non pour le contenu extrait de SocialSync.

Pour permettre aux utilisateurs de définir leurs préférences de notification, incluez une section Notification par courrier électronique dans les Paramètres utilisateur de votre système de profil utilisateur. Ajoutez les champs correspondants au schéma de votre base de données de profil utilisateur, puis gérez vos paramètres utilisateur à l’aide de Ping for Pull. (Consultez votre Gestionnaire d’intégration technique pour définir les fréquences par défaut de votre réseau. Si vous êtes un client Enterprise Profiles, transmettez les valeurs par défaut sélectionnées à votre équipe Livefyre pour configuration dans la base de données Livefyre.)

Les utilisateurs de votre site peuvent ensuite suivre une conversation et commencer à recevoir des notifications par courrier électronique en cliquant sur le **[!UICONTROL +Follow]** bouton de l’éditeur de commentaires. Les préférences de notification sont définies au niveau du réseau Livefyre. Tous les paramètres utilisateur s’appliquent à tous les sites et conversations de votre réseau.

**Valeurs par défaut recommandées**

* Quelqu'un commente dans une conversation que je suis :** digest horaire**
* Quelqu'un aime l'un de mes commentaires :** digest horaire**
* Quelqu'un répond à l'un de mes commentaires :** immédiatement**
* Suivi automatique des conversations lorsque je laisse un commentaire :** off** (non coché)

**Remarque**: Les notifications par courrier électronique sont basées sur l’heure à laquelle le contenu est approuvé pour inclusion dans le flux.

Livefyre propose deux options de fréquence des courriers électroniques :

* Immédiatement
* Résumé horaire

**Immédiatement**

Les courriers électroniques envoyés affichent immédiatement le texte de la publication, le titre de l’article, le nom d’utilisateur de l’auteur et un lien de **réponse** qui conduit l’utilisateur au contenu de la page. Ces courriers électroniques comprennent également un lien de **désabonnement** dans le pied de page, permettant aux utilisateurs de se désabonner des notifications par courrier électronique pour cette collection. En cliquant sur **annuler l’abonnement **vous les amènerez à une page de confirmation leur indiquant qu’ils ont été désinscrits de la collection.

**Résumé horaire**

Les courriers électroniques envoyés dans un résumé horaire affichent tout le contenu, les réponses au contenu et les mentions "J’aime" sur le contenu au cours de la dernière heure (ou plus) par application que l’utilisateur suit. Si l’utilisateur suit plusieurs applications sur votre réseau, il recevra un courrier électronique condensé pour chaque application.

>[!NOTE]
>
>Dans les conversations sans nouveau contenu pendant plus de plusieurs heures, les utilisateurs dont le résumé horaire est activé recevront immédiatement un avis sur une nouvelle publication de contenu.

**Options de messagerie du modérateur**

Les modérateurs peuvent choisir de recevoir des courriers électroniques pour le contenu publié dans une application qu’ils suivent et pour les commentaires marqués comme indésirable ou Offensive dans une application qu’ils modérent. **** Remarque : Aucun courrier électronique ne sera envoyé lorsque les utilisateurs signalent un commentaire avec Désaccord ou Absence de rubrique, car ces catégories ne sont pas considérées comme importantes pour la notification du modérateur.

Les champs modérateur_commentaires et modérateur_flags doivent également être ajoutés au schéma de base de données des paramètres de votre profil utilisateur modérateur afin de permettre aux modérateurs de mettre à jour la fréquence de leurs notifications par courrier électronique et de s’exclure s’ils le souhaitent. Livefyre vous recommande de définir ces deux champs de notification par courrier électronique du modérateur sur **jamais**. Les options incluent **jamais** (par défaut), **immédiatement** et **souvent**.

**E-mail du modérateur (contenu marqué) :**

Lorsque le contenu est marqué dans une application modérée, le courrier électronique envoyé au modérateur affiche le contenu marqué, le nom d’utilisateur qui a marqué le contenu et un lien renvoyant à la page de contenu.

Lorsqu’un utilisateur modifie ses préférences de notification par courrier électronique sur votre site dans votre système de profil, synchronisez la mise à jour avec le système de profil distant Livefyre à l’aide de Ping for Pull de Livefyre.

**Synchronisation des données avec Livefyre**

## Personnalisation des courriers électroniques {#section_jxb_c5k_yy}

Plusieurs champs des modèles de notification par courrier électronique peuvent être modifiés en fonction de votre style et de votre marque.

* **[!UICONTROL From Email Address]**

   L’"adresse de courriel de départ" de toutes les notifications par courriel peut être personnalisée pour être compatible avec votre marque. Livefyre recommande **noreply@customerdomain.com**, en remplaçant **** customerdomainen par votre nom de domaine. (La valeur par défaut est **noreply@livefyre.com**.) Veuillez transmettre votre "adresse électronique" préférée à votre gestionnaire d’intégration technique pour une configuration dans la base de données Livefyre de votre réseau.

   >[!NOTE]
   >
   >Laissez ce champ vide pour désactiver les notifications par courrier électronique pour votre réseau

* **[!UICONTROL Email Logo]**

   Le logo affiché dans les notifications par courrier électronique peut être personnalisé pour afficher le logo de votre entreprise, plutôt que le logo Livefyre par défaut, à l’aide de l’onglet Marque de la page Paramètres **du** réseau de Studio. Cette personnalisation est disponible uniquement au niveau du réseau, et non au niveau du site, et n’est disponible que pour les clients Livefyre payants.

* **[!UICONTROL Custom Templates]**

   Il est possible de mettre en oeuvre un modèle de courrier électronique entièrement personnalisé si vous le souhaitez. Toutefois, cela nécessitera des efforts de développement et pourrait entraîner des coûts de services professionnels. Contactez votre gestionnaire de compte pour plus de détails.



Applications qui utilisent cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Critiques](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

