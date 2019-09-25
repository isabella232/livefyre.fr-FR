---
description: Décrit les options permettant d’ajouter l’authentification des utilisateurs aux applications Livefyre, y compris Janrain Capture ou votre propre service d’identité.
seo-description: Décrit les options permettant d’ajouter l’authentification des utilisateurs aux applications Livefyre, y compris Janrain Capture ou votre propre service d’identité.
seo-title: Intégration d’identité
solution: Experience Manager
title: Intégration d’identité
uuid: 079dc9c7-656a-49d0-920d-9e5a421a319c
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Intégration d’identité{#identity-integration}

Décrit les options permettant d’ajouter l’authentification des utilisateurs aux applications Livefyre, y compris Janrain Capture ou votre propre service d’identité.

## Intégration d’identité {#t_about_identity_integration}

Décrit les options permettant d’ajouter l’authentification des utilisateurs aux applications Livefyre, y compris Janrain Capture ou votre propre service d’identité.

Les applications Livefyre comprennent une fonction interactive riche, comme la publication d’un commentaire, l’écriture d’une critique ou le contenu qui vous plaît. Pour que vos utilisateurs interagissent avec les applications Livefyre, vous devez intégrer Livefyre à un service d’identité à l’aide de Livefyre.js Auth.

Livefyre.js Auth fournit une authentification centralisée pour toutes les applications Livefyre de votre site et vous confie la responsabilité de la manière exacte dont les utilisateurs doivent se connecter et s’inscrire. Ajoutez Auth globalement au modèle de votre site et utilisez-le sur toutes les pages, ou ajoutez-le une fois par page, et lorsque vos utilisateurs se connectent dans Livefyre JS Auth diffusera automatiquement les informations de l’utilisateur à toutes les applications de la page.

Que vous ayez créé un service d'identité personnalisé ou que vous utilisiez un service d'identité tiers comme Janrain Capture, cette section traite de tout ce que vous devez savoir pour intégrer.
