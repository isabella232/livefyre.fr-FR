---
description: Ajoutez une balise d’utilisateur à un compte pour ajouter un utilisateur à un groupe.
seo-description: Ajoutez une balise d’utilisateur à un compte pour ajouter un utilisateur à un groupe.
seo-title: Ajout d’utilisateurs à des groupes
solution: Experience Manager
title: Ajout d’utilisateurs à des groupes
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Adding Users to Groups{#adding-users-to-groups}

Ajoutez une balise d’utilisateur à un compte pour ajouter un utilisateur à un groupe.

Les balises d’utilisateur peuvent être implémentées pour les systèmes de profil propriétaire et d’entreprise et peuvent être ajoutées aux comptes par plusieurs moyens :

* La création de propriétaires et de modérateurs via Studio attribue la balise d’utilisateur "modérateur" au compte.
* La création de groupes d’utilisateurs et l’ajout d’utilisateurs à ces groupes via Studio appliquent automatiquement aux utilisateurs sélectionnés des balises d’utilisateur avec le nom du groupe.
* Les balises d’utilisateur peuvent également être appliquées directement aux comptes à l’aide de l’appel HTTP [](https://api.livefyre.com/docs#add-user-tag) Ajouter une balise d’utilisateur ou Ping for Pull.

>[!NOTE]
>
>Les deux méthodes d’API, l’appel HTTP Add User Tag et la méthode Ping for Pull, écrasent toutes les balises précédemment attribuées au compte par d’autres moyens. Par conséquent, sélectionnez une méthode et utilisez-la de manière cohérente tout au long du processus.

## Ajout d’un utilisateur à un groupe à partir de la page Utilisateurs dans Studio {#section_qgq_nbw_xz}

* Cliquez sur **[!UICONTROL Add Group]** ou sur le libellé du groupe sous un nom d’utilisateur quelconque pour ouvrir le menu des groupes.
* Faites défiler la liste et recherchez le groupe auquel vous souhaitez ajouter l’utilisateur. Vous pouvez saisir un nom de groupe dans la **[!UICONTROL Search]** zone située en haut de la liste déroulante.
* Cochez la case en regard du ou des groupes auxquels l’utilisateur doit être ajouté, puis appuyez sur Retour.

Le profil de l’utilisateur affiche soit le nom du groupe (si l’utilisateur se trouve dans un seul groupe), soit le nombre de groupes auxquels il appartient.

## Ajouter un utilisateur à un groupe à l’aide de l’appel Ajouter une balise utilisateur {#section_kn3_gbw_xz}

Transmettez le code LFToken de l’utilisateur et le nom de balise sélectionné dans la requête POST.

Par exemple :

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Pour plus d’informations, voir Référence API &gt; [Ajouter une balise](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)utilisateur.

## Ajout d’un utilisateur à un groupe à l’aide de Ping for Pull {#section_kyj_11w_xz}

Utilisez le tableau de balises pour affecter des utilisateurs à des groupes d’utilisateurs. (Les balises peuvent comporter de 1 à 63 caractères alphanumériques et de soulignement.)

Par exemple :

```
"tags": ["moderator", "brand_advocate"],
```

## Ajout d’un utilisateur à un groupe à l’aide de profils distants {#section_uyn_scv_xz}

Ajoutez des balises d’utilisateur au profil distant, utilisé pour synchroniser les données d’utilisateur entre votre système de profil personnalisé et Livefyre, pour les utilisateurs spécifiques.
