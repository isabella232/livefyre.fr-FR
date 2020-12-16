---
description: Permet aux utilisateurs de sélectionner leur fréquence et leur contenu de notification.
seo-description: Permet aux utilisateurs de sélectionner leur fréquence et leur contenu de notification.
seo-title: Notifications électroniques
solution: Experience Manager
title: Notifications électroniques
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 1%

---


# Notifications électroniques{#email-notifications}

Permet aux utilisateurs de sélectionner leur fréquence et leur contenu de notification.

**Activez les notifications par courrier électronique pour vos utilisateurs et modérateurs.**

Les applications Livefyre vous permettent d’activer les notifications par courrier électronique pour vos utilisateurs et modérateurs, en fonction d’actions spécifiques. Les notifications sont basées sur le moment où le contenu est publié dans le flux, ce qui permet à vos utilisateurs de rester engagés dans des conversations qui les intéressent et d’être avertis lorsqu’une personne aime ou répond à l’un de leurs commentaires.

Les utilisateurs et les modérateurs peuvent opt-in ou sortir de la notification électronique et peuvent définir la fréquence de réception des courriers électroniques. Cette section décrit comment configurer et personnaliser ces notifications par courrier électronique.

* Options de courriel de l’utilisateur : options de notification des utilisateurs disponibles.
* Options de courriel du modérateur : options de notification du modérateur disponibles.
* Options des courriels d&#39;identité Livefyre : e-mails envoyés dans le cadre de l&#39;identité Livefyre. Ces courriels ne concernent que les clients d’identité Livefyre.
* Synchronisation des données avec Livefyre : maintien de la synchronisation des préférences avec Livefyre.
* Personnalisation des courriers électroniques : personnalisations de courrier électronique disponibles.

Utilisez les options **Paramètres > Paramètres d’intégration > Configuration de la notification par courrier électronique** pour personnaliser les notifications par courrier électronique pour votre réseau.

>[!NOTE]
>
>Pour vous assurer que vos utilisateurs finaux ne reçoivent pas de courrier indésirable, aucune notification électronique n’est envoyée depuis l’environnement Livefyre UAT.

**Options de messagerie utilisateur**

Livefyre vous permet de permettre aux utilisateurs de recevoir des notifications par courrier électronique d&#39;activité au site. Utilisez les paramètres d’intégration du Profil d’utilisateur fournis par Livefyre pour permettre aux utilisateurs de sélectionner leurs préférences pour les calendriers de notification.

>[!NOTE]
>
>Les courriers électroniques sont envoyés uniquement pour le contenu publié manuellement dans le flux, et non pour le contenu extrait de SocialSync.

Pour permettre aux utilisateurs de définir leurs préférences de notification, incluez une section Notification par courriel dans les Paramètres utilisateur de votre système de profil d’utilisateurs. Ajoutez les champs correspondants à votre schéma de base de données de profils d’utilisateurs, puis gérez vos paramètres d’utilisateur à l’aide de Ping for Pull. (Consultez votre gestionnaire d’intégration technique pour définir les fréquences par défaut de votre réseau. Si vous êtes client d’entreprise Profils, transmettez les valeurs par défaut sélectionnées à votre équipe Livefyre diffusion pour configuration dans la base de données Livefyre.)

Les utilisateurs de votre site peuvent ensuite suivre une conversation et commencer à recevoir des notifications électroniques en cliquant sur le bouton **[!UICONTROL +Follow]** de l’éditeur de commentaires. Les préférences de notification sont définies au niveau du réseau Livefyre. Tous les paramètres utilisateur s&#39;appliquent à tous les sites et conversations de votre réseau.

**Valeurs par défaut recommandées**

* Quelqu&#39;un a commenté dans une conversation que je suis :** digest horaire**
* Quelqu&#39;un aime un de mes commentaires :** digest horaire**
* Quelqu&#39;un a répondu à un de mes commentaires :** immédiatement**
* Suivi automatique des conversations lorsque je laisse un commentaire :** off** (non coché)

**Remarque** : Les notifications par courrier électronique dépendent du moment où le contenu est approuvé pour l’inclusion dans le flux.

Livefyre offre deux options de fréquence des courriers électroniques :

* Immédiatement
* Résumé horaire

**Immédiatement**

Les courriels envoyés affichent immédiatement le texte de la publication, le titre de l’article, le nom d’utilisateur de l’auteur et un lien **Répondre** qui conduit l’utilisateur au contenu de la page. Ces courriels incluent également un lien **unsubscription** dans le pied de page, ce qui permet aux utilisateurs de se désabonner des notifications par courrier électronique pour cette collection. En cliquant sur **annuler l’abonnement **vous les amènerez à une page de confirmation leur indiquant qu’ils ont été désabonnés de la collection.

**Résumé horaire**

Les courriels envoyés dans un résumé horaire affichent tout le contenu, les réponses au contenu et les mentions J’aime sur le contenu au cours de la dernière heure (ou plus) par application que l’utilisateur suit. Si l’utilisateur suit plusieurs applications sur votre réseau, il reçoit un courrier électronique de résumé pour chaque application.

>[!NOTE]
>
>Dans les conversations sans nouveau contenu pendant plus de plusieurs heures, les utilisateurs dont le résumé horaire est activé reçoivent immédiatement un avis dès qu’une nouvelle publication de contenu est publiée.

**Options de courriel du modérateur**

Les modérateurs peuvent opt-in recevoir des courriers électroniques pour le contenu publié dans une application qu’ils suivent et pour les commentaires signalés comme indésirables ou Offensifs dans une application qu’ils modérent. **Remarque :** aucun message électronique n’est envoyé lorsque les utilisateurs signalent un commentaire avec Désaccord ou Non sujet, car ces catégories ne sont pas jugées importantes pour la notification du modérateur.

Les champs modérateur_commentaires et modérateur_indicateurs doivent également être ajoutés au schéma de base de données des paramètres de profil d’utilisateur du modérateur afin de permettre aux modérateurs de mettre à jour la fréquence de leurs notifications par courrier électronique et opt-out s’ils le souhaitent. Livefyre vous recommande de définir ces deux champs de notification électronique du modérateur sur **jamais**. Les options incluent **jamais** (par défaut), **immédiatement** et **souvent**.

**E-mail du modérateur (contenu marqué) :**

Lorsque le contenu est marqué dans une application modérée, le courrier électronique envoyé au modérateur affiche le contenu marqué, le nom d’utilisateur qui a marqué le contenu et un lien renvoyant à la page de contenu.

Lorsqu’un utilisateur modifie ses préférences de notification par courrier électronique sur votre site dans votre système de profil, synchronisez la mise à jour vers le système de profil distant Livefyre à l’aide de Ping for Pull de Livefyre.

**Synchronisation des données avec Livefyre**

## Personnalisation des courriers électroniques {#section_jxb_c5k_yy}

Plusieurs champs des modèles de notification par courrier électronique peuvent être modifiés en fonction de votre style et de votre marque.

* **[!UICONTROL From Email Address]**

   L’&quot;adresse de courriel de départ&quot; pour toutes les notifications par courriel peut être personnalisée pour être compatible avec votre marque. Livefyre recommande **noreply@customerdomain.com**, en remplaçant **customerdomain** par votre nom de domaine. (La valeur par défaut est **noreply@livefyre.com**.) Veuillez transmettre votre &quot;adresse électronique&quot; préférée à votre gestionnaire d&#39;intégration technique pour une configuration dans la base de données Livefyre de votre réseau.

   >[!NOTE]
   >
   >Ne renseignez pas ce champ pour désactiver les notifications électroniques pour votre réseau.

* **[!UICONTROL Email Logo]**

   Le logo affiché dans les notifications par courrier électronique peut être personnalisé pour afficher le logo de votre société, plutôt que le logo Livefyre par défaut, à l’aide de l’onglet Marque de la page **Paramètres réseau** de Studio. Cette personnalisation n&#39;est disponible qu&#39;au niveau du réseau, et non au niveau du site, et n&#39;est disponible que pour les clients Livefyre rémunérés.

* **[!UICONTROL Custom Templates]**

   Si vous le souhaitez, il est possible de mettre en oeuvre un modèle de courrier électronique entièrement personnalisé. Toutefois, cela exigera un certain effort de développement et peut entraîner des coûts de services professionnels. Pour plus d&#39;informations, contactez votre gestionnaire de compte.



Applications qui utilisent cette fonctionnalité :

* [Carrousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Carte des fonctionnalités](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mur multimédia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Critiques](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

