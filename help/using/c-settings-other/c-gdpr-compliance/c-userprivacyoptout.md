---
description: Ajoutez l'indicateur userprivacyoptout à la page pour permettre à un visiteur du site de se désinscrire de ce suivi.
seo-description: Ajoutez l'indicateur userprivacyoptout à la page pour permettre à un visiteur du site de se désinscrire de ce suivi.
seo-title: Userprivacyoptout
title: Userprivacyoptout
uuid: a 043 c 50 e -0 a 02-4 c 83-bbce -54 b 9 b 51316 a 5
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacyoptout{#userprivacyoptout}

Ajoutez l&#39; `userPrivacyOptOut` indicateur à la page pour permettre à un visiteur du site de se désinscrire de ce suivi.

Livefyre fournit des événements JavaScript pour effectuer le suivi de l&#39;activité des utilisateurs dans vos applications Livefyre.

Si vous incorporez des applications Livefyre et qu&#39;un visiteur n&#39;accepte pas le suivi, vous pouvez configurer Livefyre de manière dynamique pour désactiver la fonctionnalité de confidentialité du visiteur.

Une fois configuré, Livefyre procédera comme suit :

* Désactivez la prise en charge de l&#39;authentification dans les applications.
* Désactivation de la génération de Livecount et de l&#39;événement
* Supprimer les cookies existants créés par les applications qui se trouvent sur la page
* Média proxy avec images provenant de domaines tiers pour empêcher des tiers de créer des cookies
* Activer le clic publicitaire sur les vidéos tierces pour les vidéos tierces qui nécessitent un clic supplémentaire

## Configuration d&#39;une page pour exclusion

Les intégrations incorporées à Livefyre Apps peuvent configurer Livefyre lorsqu&#39;un visiteur du site n&#39;a pas accordé de consentement à l&#39;aide d&#39;une variable JavaScript unique.

Instructions :

1. Ajoutez l&#39; `userPrivacyOptOut` indicateur à la page avant `Livefyre.js` le script JavaScript :

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Ajoutez `Livefyre.js` à la page n&#39;importe où après `userPrivacyOptOut`.

   Les applications Livefyre instancient avec les paramètres de confidentialité élevés.

   >[!NOTE]
   >
   >Ne modifiez pas la valeur des `userPrivacyOptOut` applications Livefyre chargées.

Assurez-vous que le processus de consentement définit `userPrivacyOptOut` la valeur true si un visiteur du site choisit de se désinscrire.
