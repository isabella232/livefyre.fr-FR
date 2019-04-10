---
description: Découvrez les conventions Livefyre et comment Livefyre organise le contenu.
seo-description: Découvrez les conventions Livefyre et comment Livefyre organise le
  contenu.
seo-title: Architecture
solution: Experience Manager
title: Architecture
uuid: 94358 e 6 c -954 a -4 a 52-9 bb 2-d 800 b 2933130
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Architecture{#architecture}

Découvrez les conventions Livefyre et comment Livefyre organise le contenu.

Cette section présente l'architecture réseau Livefyre.

## Présentation des réseaux et des sites

Livefyre organise les utilisateurs et le contenu par réseau et par site. Chaque réseau peut avoir un ou plusieurs comptes utilisateur associés et chaque réseau peut inclure un ou plusieurs sites Livefyre. Un site Livefyre est un groupement arbitraire de collections. Une collection correspond à un ID d'article dans votre CMS.

## Présentation des réseaux {#section_hqt_4m4_xz}

Les clients qui disposent de plusieurs domaines peuvent partager des comptes d'utilisateurs sur tous les domaines à l'aide d'un réseau Livefyre unique. Les clients qui souhaitent conserver des comptes utilisateur distincts pour différents domaines nécessitent des réseaux Livefyre distincts.

Les paramètres de configuration peuvent s'appliquer aux sites, réseaux et collections (appelés conversation dans l'illustration ci-dessus).

>[!NOTE]
>
>Certains paramètres sont disponibles uniquement au niveau du réseau (par exemple, préférences de notification par courrier électronique, courriel de l'adresse et logos personnalisés par courrier électronique). Si vous souhaitez que ces paramètres soient différents pour chaque domaine, vous devez utiliser plusieurs réseaux.

## Présentation des sites {#section_vjw_nm4_xz}

Un site est un groupement arbitraire d'articles. Le regroupement est utile car il vous permet d'affecter différents modérateurs à différents groupes de contenu. Les modérateurs et les propriétaires peuvent être configurés pour modérer le contenu et configurer les paramètres d'administration au niveau du réseau ou du site. Si vous souhaitez que certains modérateurs ne voient que certaines collections, ces collections peuvent être configurées comme un site Livefyre distinct.

>[!NOTE]
>
>Le nombre de sites que vous pouvez avoir sous votre réseau personnalisé n'est pas limité.

## Diagramme de séquence d'applications {#section_mw2_lm4_xz}

Que vous souhaitiez mettre en œuvre une fonction personnalisée avec Livefyre fourni des endpoints de fin ou simplement déboguer un problème, il vous aide à comprendre comment fonctionne le flux de demande/réponse de l'application Livefyre.

![](assets/appsequencediagram.png)

1. Lorsque votre client atteint votre site, instanciez l'application Livefyre avec l'ID de site et l'ID d'article.
1. Si vous souhaitez authentifier l'utilisateur (pour l'évaluation du trafic, ainsi que pour la protection du site), envoyez Livefyre les informations sur le site et le jeton de profil utilisateur.
1. Envoyez Livefyre l'ID de site et l'ID d'article pour initialiser l'application.

   Livefyre renvoie le contenu initial.

   Envoyez ce contenu à la page et affichez l'application.

1. Pour mettre à jour le contenu affiché sur la page, envoyez Livefyre au dernier ID d'événement de votre page. Si un nouveau contenu est disponible, il est renvoyé.

   Rechargez votre page avec un nouveau contenu et répétez le processus indéfiniment.

1. Si vous autorisez les utilisateurs à publier du nouveau contenu, déclenchez un événement lorsque le nouveau contenu est publié sur votre site pour publier le contenu vers Livefyre. Livefyre renverra un flux mis à jour, que vous pouvez utiliser pour mettre à jour votre site.
