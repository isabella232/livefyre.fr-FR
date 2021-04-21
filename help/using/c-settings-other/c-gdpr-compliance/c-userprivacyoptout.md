---
description: Ajoutez l'indicateur userPrivacyOptOut sur la page pour permettre à un visiteur de site de opt-out de ce suivi.
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

Ajoutez l&#39;indicateur `userPrivacyOptOut` sur la page pour autoriser un visiteur de site à opt-out de ce suivi.

Livefyre fournit des événements JavaScript pour suivre l’activité des utilisateurs dans vos applications Livefyre.

Si vous incorporez des applications Livefyre et qu’un visiteur n’accepte pas le suivi, vous pouvez configurer de manière dynamique Livefyre pour désactiver cette fonctionnalité afin d’assurer la confidentialité du visiteur.

Une fois configurée, Livefyre :

* Désactivez la prise en charge de l’authentification dans les applications.
* Désactiver Livecount et génération de événements
* Supprimez les cookies existants créés par toute application se trouvant sur la page.
* Média proxy avec images provenant de domaines tiers pour empêcher des tiers de créer des cookies
* Activer le clic publicitaire de masque vidéo pour les vidéos tierces qui nécessitent un clic supplémentaire vers la vue

## Configuration d’une page pour l’exclusion

Les intégrations incorporant des applications Livefyre peuvent configurer Livefyre lorsqu’un visiteur de site n’a pas accordé de consentement à l’aide d’une variable JavaScript unique.

Instructions:

1. Ajoutez l&#39;indicateur `userPrivacyOptOut` sur la page avant le script JavaScript `Livefyre.js` :

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Ajoutez `Livefyre.js` sur la page n’importe où après `userPrivacyOptOut`.

   Les applications Livefyre instancient avec les paramètres de confidentialité élevés.

   >[!NOTE]
   >
   >Ne modifiez pas la valeur de `userPrivacyOptOut` une fois que les applications Livefyre ont été chargées.

Assurez-vous que votre processus de consentement définit la valeur `userPrivacyOptOut` sur true si un visiteur de site choisit de opt-out.
