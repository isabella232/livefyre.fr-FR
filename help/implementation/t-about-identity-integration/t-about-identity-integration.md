---
description: Décrit les options permettant d’ajouter l’authentification des utilisateurs aux applications Livefyre, y compris Janrain Capture ou votre propre service d’identité.
title: Intégration d’identité
exl-id: a3b849fc-0182-4fed-94b5-6d7199fc4e44
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Intégration d&#39;identité{#identity-integration}

Décrit les options permettant d’ajouter l’authentification des utilisateurs aux applications Livefyre, y compris Janrain Capture ou votre propre service d’identité.

## Intégration d&#39;identité {#t_about_identity_integration}

Décrit les options permettant d’ajouter l’authentification des utilisateurs aux applications Livefyre, y compris Janrain Capture ou votre propre service d’identité.

Les applications Livefyre offrent une fonction interactive complète, telle que la publication d’un commentaire, l’écriture d’une critique ou l’ajout de contenu. Pour que vos utilisateurs puissent interagir avec les applications Livefyre, vous devez intégrer Livefyre à un service d&#39;identité utilisant Livefyre.js Auth.

Livefyre.js Auth fournit une authentification centralisée pour toutes les applications Livefyre sur votre site et vous confie la responsabilité de la manière exacte dont les utilisateurs doivent se connecter et s&#39;inscrire. Ajoutez Auth globalement sur le modèle de votre site et utilisez-le sur toutes les pages, ou ajoutez-le une fois par page, et lorsque vos utilisateurs se connectent dans Livefyre JS Auth diffusera automatiquement les informations de l’utilisateur à toutes les applications de la page.

Que vous ayez créé un service d&#39;identité personnalisé ou que vous utilisiez un service d&#39;identité tiers comme Janrain Capture, cette section traite de tout ce que vous devez savoir pour intégrer.
