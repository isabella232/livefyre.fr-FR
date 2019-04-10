---
description: Générez la réponse Ping pour pull pour transmettre les informations de
  l'utilisateur mises à jour à Livefyre.
seo-description: Générez la réponse Ping pour pull pour transmettre les informations
  de l'utilisateur mises à jour à Livefyre.
seo-title: Créer le ping pour réponse pull
solution: Experience Manager
title: Créer le ping pour réponse pull
uuid: f 90871 d 5-601 f -40 dc-b 3 d 2-ab 78635 e 4 a 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Créer le ping pour réponse pull{#build-the-ping-for-pull-response}

Générez la réponse Ping pour pull pour transmettre les informations de l'utilisateur mises à jour à Livefyre.

| Type | Propriété | Description |
|--- |--- |--- |
| Chaîne *requise* | id | Utilisateur - id de l'utilisateur dans votre système de profils. Elle doit être unique pour tous les utilisateurs de votre réseau et ne doit jamais changer. |
| Chaîne *requise* | display_ name | Nom d'affichage de l'utilisateur. Elle sera générée avec le contenu Livefyre publié par l'utilisateur. |
| Objet *facultatif, mais recommandé* | name | Chaînes permettant de définir le format, le milieu, le milieu et le nom de l'utilisateur. |
| Chaîne *facultative, mais recommandée* | email | Adresse électronique de l'utilisateur. Utilisé pour envoyer des notifications par courrier électronique. |
| Chaîne *facultative, mais recommandée* | image_ url | URL à un avatar à afficher pour l'utilisateur. Livefyre met à l'échelle les images transférées à 100 × 100, 75 × 75 ou 50 × 50 pixels, selon le cas. Pour un résultat optimal, les utilisateurs doivent télécharger une image carrée, à 100 × 100 pixels. Pour garantir la mise à jour de l'image de l'avatar dans Livefyre, modifiez l'URL_ url pour chaque mise à jour de l'image afin que Ping pour Pull détecte que l'image a été modifiée. Par exemple, joignez un horodatage au nom de fichier ou incrémentez l'image. Remarque : Toutes les URL doivent être complètes et accessibles. |
| Chaîne *facultative, mais recommandée* | profile_ url | URL de la page de profil de l'utilisateur sur votre site. |
| Chaîne *facultative, mais recommandée* | settings_ url | URL d'une page où les utilisateurs peuvent configurer les paramètres de profil de l'utilisateur pour votre site. |
| Tableau *facultatif, mais recommandé* | balises | Utilisé pour affecter des utilisateurs aux groupes d'utilisateurs. Les balises peuvent comprendre entre 1 et 63 caractères alphanumériques et de soulignement. |
| Booléen *optionnel, mais recommandé* | autofollow_ conversations | Indique si un utilisateur souhaite suivre automatiquement une collection après sa publication. Lorsque vous suivez une collection, les utilisateurs reçoivent des notifications par courrier électronique lorsque d'autres utilisateurs participent. Peut être vrai ou faux. Par défaut, true. |
| Objet *facultatif, mais recommandé* | email_ notifications | Définit la fréquence des notifications électroniques Livefyre disponibles. Différentes fréquences peuvent être définies pour chaque type de notification. Par défaut, aucune notification ne sera envoyée. <br><ul><li> envoie immédiatement les notifications immédiatement à l'événement répertorié. </li><li>envoie souvent des notifications par lots. </li><li> n'enverra jamais de notification par courrier électronique pour l'activité. </li><li>*commentaires*: Définit le moment où des notifications sont envoyées lorsque d'autres utilisateurs publient du contenu dans des collections que cet utilisateur suit. </li><li>*réponses*: Définit le moment où les notifications sont envoyées lorsqu'un autre utilisateur répond au contenu de cet utilisateur.</li><li>*mentions « J'aime* » : Définit le moment où les notifications sont envoyées lorsqu'un autre utilisateur aime le contenu de cet utilisateur.</li><li>*modérator_ comments*: Définit le moment où les notifications sont envoyées aux modérateurs lorsque les utilisateurs publient du contenu vers une collection dans le réseau.</li><li>*modérator_ flags*: Définit le moment où les notifications sont envoyées aux modérateurs lorsque d'autres utilisateurs signalent le contenu d'une collection dans le réseau.</li></ul> |
| Chaîne *facultative* | emplacement | Emplacement envoyé par l'utilisateur. |
| Chaîne *facultative* | biographie | Autobiographie envoyée par l'utilisateur. |
| Tableau *facultatif* | sites Web | Tableau de sites envoyés par l'utilisateur. Max = 2. |
| Objet *facultatif* | display_ rules | Définit les propriétés de profil visibles publiquement par d'autres utilisateurs. Chaque paramètre disponible prend la valeur booléenne true ou false. Paramètres disponibles : <br><ul><li>biographie </li><li> emplacement</li><li>  sexe </li><li>nameimage </li><li> remote_ profile_ url</li></ul> |
| Valeur booléenne *facultative* | modérateur | Indique si l'utilisateur dispose de privilèges de modérateur sur le réseau. |
| Valeur booléenne *facultative* | gravatar_ disabled | Indique si l'utilisation d'une gravatar par Livefyre est désactivée si aucune URL image_ url n'est fournie. |

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
