---
description: Build the Ping for Pull response to transmit updated user information to Livefyre.
seo-description: Build the Ping for Pull response to transmit updated user information to Livefyre.
seo-title: Build the Ping for Pull Response
solution: Experience Manager
title: Build the Ping for Pull Response
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Build the Ping for Pull Response{#build-the-ping-for-pull-response}

Build the Ping for Pull response to transmit updated user information to Livefyre.

| Type | Propriété | Description |
|--- |--- |--- |
| String required ** | l’id | The user ID of the user in your profile system. This must be unique across all users in your Network, and must never change. |
| String required ** | display_name | The display name of the user. This will be rendered with Livefyre Content posted by the user. |
| Object optional, but recommended ** | name | Strings to define the user’s formatted, first, middle, and last names. |
| Chaîne *facultative, mais recommandée* | adresse électronique | User’s email address. Utilisé pour envoyer des notifications par courrier électronique. |
| String optional, but recommended ** | image_url | URL d’un avatar à afficher pour l’utilisateur. Livefyre scales uploaded images to 100×100, 75×75, or 50×50 pixels, as appropriate. For best results, users should upload a square image, at 100×100 pixels. To ensure the avatar image is updated in Livefyre, modify the image_url for each image update so Ping for Pull detects that the image was changed. For example, attach a timestamp to the filename or increment the image changes. Remarque :  All URLs must be fully qualified and accessible. |
| String optional, but recommended ** | profile_url | URL de la page de profil de l’utilisateur sur votre site. |
| String optional, but recommended ** | settings_url | URL to a page where users may configure the user’s profile settings for your site. |
| Array optional, but recommended ** | balises | Used to assign users to user groups. Tags may include 1-63 alphanumeric and underscore characters. |
| Boolean optional, but recommended ** | autofollow_conversations | Defines whether a user wishes to automatically follow a Collection after posting to it. When following a Collection, users receive email notifications when other users participate. May be true or false. La valeur par défaut est true. |
| Object optional, but recommended ** | email_notifications | Defines the frequency of available Livefyre email notifications. Différentes fréquences peuvent être définies pour chaque type de notification. By default, no notifications will be sent. <br><ul><li> envoie immédiatement des notifications à l’événement répertorié. </li><li>génère souvent des notifications par lots. </li><li> ne jamais envoyer de notification par courrier électronique pour l’activité. </li><li>*commentaires*: Définit le moment où les notifications sont envoyées lorsque d’autres utilisateurs publient du contenu dans les collections que cet utilisateur suit. </li><li>*réponses*: Définit le moment où les notifications sont envoyées lorsqu’un autre utilisateur répond au contenu de cet utilisateur.</li><li>*aime*: Définit le moment où les notifications sont envoyées lorsqu’un autre utilisateur aime le contenu de cet utilisateur.</li><li>*modérator_commentaires*: Définit le moment où les notifications sont envoyées aux modérateurs lorsque les utilisateurs publient du contenu dans une collection du réseau.</li><li>*modérator_flags*: Définit le moment où les notifications sont envoyées aux modérateurs lorsque d’autres utilisateurs signalent le contenu dans une collection du réseau.</li></ul> |
| Chaîne *facultative* | emplacement | Emplacement envoyé par l’utilisateur. |
| Chaîne *facultative* | bio | autobiographie envoyée par l’utilisateur. |
| Tableau *facultatif* | sites Web | Tableau de sites envoyés par les utilisateurs. Max = 2. |
| Objet *facultatif* | display_Rules | Définit les propriétés de profil visibles publiquement par les autres utilisateurs. Chaque paramètre disponible prend la valeur de saisie booléenne true ou false. Paramètres disponibles :  <br><ul><li>bio </li><li> emplacement</li><li>  sexe </li><li>image nomimage </li><li> remote_profile_url</li></ul> |
| Booléen *facultatif* | modérateur | Définit si l’utilisateur dispose de privilèges de modérateur sur le réseau. |
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
