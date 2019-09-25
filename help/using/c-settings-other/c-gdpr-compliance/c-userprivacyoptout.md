---
description: Ajoutez l’indicateur userPrivacyOptOut à la page pour permettre à un visiteur du site de s’exclure de ce suivi.
seo-description: Ajoutez l’indicateur userPrivacyOptOut à la page pour permettre à un visiteur du site de s’exclure de ce suivi.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

Ajoutez l’ `userPrivacyOptOut` indicateur à la page pour permettre à un visiteur du site de s’exclure de ce suivi.

Livefyre fournit des événements JavaScript pour suivre l’activité des utilisateurs dans vos applications Livefyre.

Si vous incorporez des applications Livefyre et qu’un visiteur ne consent pas au suivi, vous pouvez configurer Livefyre de manière dynamique pour désactiver cette fonctionnalité afin d’assurer la confidentialité du visiteur.

Une fois configurée, Livefyre :

* Désactivez la prise en charge de l’authentification dans les applications.
* Désactiver Livecount et génération d’événements
* Supprimez les cookies existants créés par les applications de la page.
* Modules proxy avec images de domaines tiers pour empêcher des tiers de créer des cookies
* Activer le clic publicitaire de masque vidéo pour les vidéos tierces qui nécessitent un clic supplémentaire pour l’affichage

## Configuration d’une page pour l’exclusion

Les intégrations incorporant des applications Livefyre peuvent configurer Livefyre lorsqu’un visiteur du site n’a pas accordé de consentement à l’aide d’une variable JavaScript unique.

Instructions:

1. Ajoutez l’ `userPrivacyOptOut` indicateur à la page avant le `Livefyre.js` script JavaScript :

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Ajouter `Livefyre.js` à la page n’importe où après `userPrivacyOptOut`.

   Les applications Livefyre instancient avec les paramètres de confidentialité élevés.

   >[!NOTE]
   >
   >Ne modifiez pas la valeur d’une `userPrivacyOptOut` fois que les applications Livefyre ont été chargées.

Assurez-vous que votre processus de consentement définit la valeur `userPrivacyOptOut` sur true si un visiteur du site choisit de s’exclure.
