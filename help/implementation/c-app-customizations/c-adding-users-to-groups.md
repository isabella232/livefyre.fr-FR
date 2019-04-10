---
description: Ajoutez une balise d'utilisateur à un compte pour ajouter un utilisateur
  à un groupe.
seo-description: Ajoutez une balise d'utilisateur à un compte pour ajouter un utilisateur
  à un groupe.
seo-title: Ajout d'utilisateurs aux groupes
solution: Experience Manager
title: Ajout d'utilisateurs aux groupes
uuid: 3633 f 2 df -8 d 60-4 cdd-b 9 a 2-3807218 c 74 a 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Ajout d'utilisateurs aux groupes{#adding-users-to-groups}

Ajoutez une balise d'utilisateur à un compte pour ajouter un utilisateur à un groupe.

Les balises utilisateur peuvent être implémentées pour les systèmes de profils propriétaires et d'entreprise et peuvent être ajoutées aux comptes de plusieurs manières :

* La création de propriétaires et de modérateurs via Studio affecte la balise d'utilisateur du modérateur au compte.
* La création de groupes d'utilisateurs et leur ajout à l'aide de l'utilitaire Studio applique automatiquement les balises utilisateur avec le nom du groupe aux utilisateurs sélectionnés.
* Les balises utilisateur peuvent également être appliquées directement aux comptes à l'aide de [l'appel HTTP](https://api.livefyre.com/docs#add-user-tag) de balise d'utilisateur ou Ping pour Pull.

>[!NOTE]
>
>Les deux méthodes d'API, l'appel HTTP Ajout de balise utilisateur et la méthode Ping pour pull, remplacent toutes les balises précédemment attribuées au compte par d'autres moyens. Par conséquent, sélectionnez une méthode et utilisez-la de manière cohérente tout au long de votre processus.

## Ajout d'un utilisateur à un groupe depuis la page Utilisateurs de Studio {#section_qgq_nbw_xz}

* Cliquez **[!UICONTROL Add Group]** sur ou sur le libellé du groupe sous n'importe quel nom d'utilisateur pour ouvrir le menu des groupes.
* Faites défiler la liste et recherchez le groupe auquel vous souhaitez ajouter l'utilisateur. Vous pouvez entrer un nom de groupe dans **[!UICONTROL Search]** la zone située en haut de la liste déroulante.
* Cochez la case en regard du ou des groupes auxquels l'utilisateur doit être ajouté et cliquez sur Retour.

Le profil de l'utilisateur affiche le nom du groupe (si l'utilisateur est dans un seul groupe) ou le nombre de groupes auxquels l'utilisateur appartient.

## Ajout d'un utilisateur à un groupe à l'aide de l'appel Ajouter une balise utilisateur {#section_kn3_gbw_xz}

Transmettre le fichier lftoken de l'utilisateur et le nom de balise sélectionné avec la requête POST

Par exemple :

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Pour plus d'informations, voir Référence API > [Ajouter une balise utilisateur](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Ajout d'un utilisateur à un groupe à l'aide de Ping for Pull {#section_kyj_11w_xz}

Utilisez le tableau des balises pour affecter des utilisateurs aux groupes d'utilisateurs. (Les balises peuvent comprendre 1 à 63 caractères alphanumériques et de soulignement.)

Par exemple :

```
"tags": ["moderator", "brand_advocate"],
```

## Ajout d'un utilisateur à un groupe à l'aide de profils distants {#section_uyn_scv_xz}

Ajoutez des balises utilisateur au profil distant, utilisé pour synchroniser les données utilisateur entre votre système de profils personnalisé et Livefyre pour les utilisateurs spécifiques.
