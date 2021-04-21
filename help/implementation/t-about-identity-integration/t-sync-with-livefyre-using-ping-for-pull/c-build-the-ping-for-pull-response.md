---
description: Créez la réponse Ping for Pull pour transmettre les informations utilisateur mises à jour à Livefyre.
title: Créer un ping pour une réponse à extraction
exl-id: 81c398fd-2acb-4e39-a2b3-c96921b1192b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# Créer le ping pour une réponse à extraction{#build-the-ping-for-pull-response}

Créez la réponse Ping for Pull pour transmettre les informations utilisateur mises à jour à Livefyre.

| Type | Propriété | Description |
|--- |--- |--- |
| Chaîne *requise* | l’id | ID utilisateur de l’utilisateur dans votre système de profil. Cette variable doit être unique pour tous les utilisateurs de votre réseau et ne doit jamais changer. |
| Chaîne *requise* | display_name | Nom d’affichage de l’utilisateur. Ceci sera rendu avec le contenu Livefyre publié par l’utilisateur. |
| Objet *facultatif mais recommandé* | name | Chaînes permettant de définir les noms formatés, les prénoms, les noms intermédiaires et les noms de l’utilisateur. |
| Chaîne *facultative mais recommandée* | adresse électronique | Adresse électronique de l’utilisateur. Permet d’envoyer des notifications par courrier électronique. |
| Chaîne *facultative mais recommandée* | image_url | URL d’un avatar à afficher pour l’utilisateur. Livefyre redimensionne les images téléchargées à 100 × 100, 75 × 75 ou 50 × 50 pixels, selon le cas. Pour un résultat optimal, les utilisateurs doivent télécharger une image carrée, à 100 × 100 pixels. Pour que l’image d’avatar soit mise à jour dans Livefyre, modifiez l’URL image_url pour chaque mise à jour d’image afin que Ping for Pull détecte que l’image a été modifiée. Par exemple, ajoutez un horodatage au nom de fichier ou incrémentez les modifications d’image. Remarque :  Toutes les URL doivent être entièrement qualifiées et accessibles. |
| Chaîne *facultative mais recommandée* | profil_url | URL de la page de profil de l’utilisateur sur votre site. |
| Chaîne *facultative mais recommandée* | settings_url | URL vers une page sur laquelle les utilisateurs peuvent configurer les paramètres de profil de l’utilisateur pour votre site. |
| Tableau *facultatif mais recommandé* | balises | Permet d’affecter des utilisateurs à des groupes d’utilisateurs. Les balises peuvent contenir de 1 à 63 caractères alphanumériques et des caractères de soulignement. |
| Boolean *facultatif mais recommandé* | autofollow_conversations | Définit si un utilisateur souhaite suivre automatiquement une collection après y avoir publié des données. Lors de l’exécution d’une collection, les utilisateurs reçoivent des notifications par courrier électronique lorsque d’autres utilisateurs participent. Peut être vrai ou faux. La valeur par défaut est true. |
| Objet *facultatif mais recommandé* | email_notifications | Définit la fréquence des notifications par courrier électronique Livefyre disponibles. Différentes fréquences peuvent être définies pour chaque type de notification. Par défaut, aucune notification n’est envoyée. <br><ul><li> envoie immédiatement des notifications au événement indiqué. </li><li>génère souvent des notifications par lots. </li><li> jamais n&#39;enverra de notification par courrier électronique pour l&#39;activité. </li><li>*commentaires* : Définit le moment où les notifications sont envoyées lorsque d’autres utilisateurs publient du contenu dans les collections que cet utilisateur suit. </li><li>*réponses* : Définit le moment où des notifications sont envoyées lorsqu’un autre utilisateur répond au contenu de cet utilisateur.</li><li>*aime* : Définit le moment où les notifications sont envoyées lorsqu’un autre utilisateur aime le contenu de cet utilisateur.</li><li>*modérator_commentaires* : Définit le moment où les notifications sont envoyées aux modérateurs lorsque les utilisateurs publient du contenu dans une collection du réseau.</li><li>*modérator_flags* : Définit le moment où les notifications sont envoyées aux modérateurs lorsque d’autres utilisateurs signalent le contenu dans une collection du réseau.</li></ul> |
| Chaîne *facultative* | emplacement | Emplacement envoyé par l’utilisateur. |
| Chaîne *facultative* | bio | autobiographie envoyée par l’utilisateur. |
| Tableau *facultatif* | sites Web | Tableau de sites envoyés par les utilisateurs. Max = 2. |
| Objet *facultatif* | display_rules | Définit les propriétés du profil qui sont publiquement visibles par les autres utilisateurs. Chaque paramètre disponible prend la valeur Boolean input true ou false. Paramètres disponibles :  <br><ul><li>bio </li><li> emplacement</li><li>  sexe </li><li>image nomimage </li><li> remote_profil_url</li></ul> |
| Booléen *facultatif* | modérateur | Définit si l’utilisateur dispose de privilèges de modérateur sur l’ensemble du réseau. |
| Booléen *facultatif* | gravatar_disabled | Définit si Livefyre doit désactiver l’utilisation d’un gravatar si aucune image_url n’est fournie. |

## Exemple de réponse {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
