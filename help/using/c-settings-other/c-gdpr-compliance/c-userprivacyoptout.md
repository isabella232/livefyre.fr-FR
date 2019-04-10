---
description: Ajoutez l'indicateur userprivacyoptout à la page pour permettre à un
  visiteur du site de se désinscrire de ce suivi.
seo-description: Ajoutez l'indicateur userprivacyoptout à la page pour permettre à
  un visiteur du site de se désinscrire de ce suivi.
seo-title: Userprivacyoptout
title: Userprivacyoptout
uuid: a 043 c 50 e -0 a 02-4 c 83-bbce -54 b 9 b 51316 a 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyoptout{#userprivacyoptout}

Ajoutez l' `userPrivacyOptOut` indicateur à la page pour permettre à un visiteur du site de se désinscrire de ce suivi.

Livefyre fournit des événements JavaScript pour effectuer le suivi de l'activité des utilisateurs dans vos applications Livefyre.

Si vous incorporez des applications Livefyre et qu'un visiteur n'accepte pas le suivi, vous pouvez configurer Livefyre de manière dynamique pour désactiver la fonctionnalité de confidentialité du visiteur.

Une fois configuré, Livefyre procédera comme suit :

* Désactivez la prise en charge de l'authentification dans les applications.
* Désactivation de la génération de Livecount et de l'événement
* Supprimer les cookies existants créés par les applications qui se trouvent sur la page
* Média proxy avec images provenant de domaines tiers pour empêcher des tiers de créer des cookies
* Activer le clic publicitaire sur les vidéos tierces pour les vidéos tierces qui nécessitent un clic supplémentaire

## Configuration d'une page pour exclusion

Les intégrations incorporées à Livefyre Apps peuvent configurer Livefyre lorsqu'un visiteur du site n'a pas accordé de consentement à l'aide d'une variable JavaScript unique.

Instructions :

1. Ajoutez l' `userPrivacyOptOut` indicateur à la page avant `Livefyre.js` le script JavaScript :

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Ajoutez `Livefyre.js` à la page n'importe où après `userPrivacyOptOut`.

   Les applications Livefyre instancient avec les paramètres de confidentialité élevés.

   >[!NOTE]
   >
   >Ne modifiez pas la valeur des `userPrivacyOptOut` applications Livefyre chargées.

Assurez-vous que le processus de consentement définit `userPrivacyOptOut` la valeur true si un visiteur du site choisit de se désinscrire.
