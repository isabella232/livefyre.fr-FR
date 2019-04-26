---
description: Ce que vous pouvez attendre de mettre en œuvre Livefyre Studio.
seo-description: Ce que vous pouvez attendre de mettre en œuvre Livefyre Studio.
seo-title: Processus de mise en œuvre
solution: Experience Manager
title: Processus de mise en œuvre
uuid: 9 a 0 f 394 e -3467-47 d 1-9816-45 e 2130 db 440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Processus de mise en œuvre{#implementation-process}

La durée de mise en œuvre de Livefyre dépend de votre implémentation et de votre portée de travail.

## Présentation de l'architecture réseau Livefyre {#section_dgj_l32_rbb}

Livefyre utilise les termes suivants pour discuter de l'architecture réseau :

* Réseau. Domaine de niveau supérieur sur lequel vous envisagez d'utiliser Livefyre.
* Sites. Sous-domaine ou section du site qui fait partie du réseau.
* Applications. Rendu du contenu sur votre site. Le contenu s'affiche visuellement dans les applications à l'aide des applications visualisation (Mosaïque, Carrousel, Carte de fonctionnalités, etc.). ou au format texte, à l'aide d'applications de conversation (commentaires, révisions, chat, etc.). Vous pouvez placer une ou plusieurs applications sur vos sites.
* Flux. Les flux sont des filtres qui recherchent les médias sociaux et d'autres sites pour rassembler automatiquement le contenu pour la modération ou la publication directe dans une application.
* Contenu (UGC, commentaires, par exemple). Ce qui s'affiche dans les applications. Le contenu peut être visuel (photo ou vidéo, par exemple), audio uniquement ou texte.

Le diagramme suivant montre les relations entre le réseau, les sites, les applications et le contenu.

![](assets/network_site_architecture.png)

Vous disposez de votre propre instance Livefyre qui est votre tableau de bord central pour la modération du contenu, la gestion des utilisateurs, etc. Contactez votre CSM pour accéder à votre instance Livefyre.

## Étapes d'intégration {#section_s2j_d2x_tz}

L'intégration de Livefyre comprend trois étapes principales :

* Intégration d'applications

   Lorsque vous implémentez Livefyre, le style d'implémentation dépend de votre cas d'utilisation. Pour [plus d'informations sur chaque type d'implémentation](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Intégration d'authentification

   Vous devez intégrer votre système de gestion des utilisateurs existant à Livefyre pour les applications de conversation et les autres applications nécessitant une authentification de l'utilisateur final sur votre site. Si vous n'utilisez pas actuellement d'outil de gestion des utilisateurs, vous pouvez utiliser Livefyre Identity. Pour [plus d'informations sur l'identité de Livefyre, ce qu'il est et comment le configurer](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personnalisation

   La personnalisation est facultative, mais la plupart des clients personnalisent les applications en fonction de leur marque.

