---
description: Ajoutez une balise d'utilisateur à un compte pour ajouter un utilisateur à un groupe.
seo-description: Ajoutez une balise d'utilisateur à un compte pour ajouter un utilisateur à un groupe.
seo-title: Ajout d'utilisateurs aux groupes
solution: Experience Manager
title: Ajout d'utilisateurs aux groupes
uuid: 3633 f 2 df -8 d 60-4 cdd-b 9 a 2-3807218 c 74 a 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Ajout d&#39;utilisateurs aux groupes{#adding-users-to-groups}

Ajoutez une balise d&#39;utilisateur à un compte pour ajouter un utilisateur à un groupe.

Les balises utilisateur peuvent être implémentées pour les systèmes de profils propriétaires et d&#39;entreprise et peuvent être ajoutées aux comptes de plusieurs manières :

* La création de propriétaires et de modérateurs via Studio affecte la balise d&#39;utilisateur du modérateur au compte.
* La création de groupes d&#39;utilisateurs et leur ajout à l&#39;aide de l&#39;utilitaire Studio applique automatiquement les balises utilisateur avec le nom du groupe aux utilisateurs sélectionnés.
* Les balises utilisateur peuvent également être appliquées directement aux comptes à l&#39;aide de [l&#39;appel HTTP](https://api.livefyre.com/docs#add-user-tag) de balise d&#39;utilisateur ou Ping pour Pull.

>[!NOTE]
>
>Les deux méthodes d&#39;API, l&#39;appel HTTP Ajout de balise utilisateur et la méthode Ping pour pull, remplacent toutes les balises précédemment attribuées au compte par d&#39;autres moyens. Par conséquent, sélectionnez une méthode et utilisez-la de manière cohérente tout au long de votre processus.

## Ajout d&#39;un utilisateur à un groupe depuis la page Utilisateurs de Studio {#section_qgq_nbw_xz}

* Cliquez **[!UICONTROL Add Group]** sur ou sur le libellé du groupe sous n&#39;importe quel nom d&#39;utilisateur pour ouvrir le menu des groupes.
* Faites défiler la liste et recherchez le groupe auquel vous souhaitez ajouter l&#39;utilisateur. Vous pouvez entrer un nom de groupe dans **[!UICONTROL Search]** la zone située en haut de la liste déroulante.
* Cochez la case en regard du ou des groupes auxquels l&#39;utilisateur doit être ajouté et cliquez sur Retour.

Le profil de l&#39;utilisateur affiche le nom du groupe (si l&#39;utilisateur est dans un seul groupe) ou le nombre de groupes auxquels l&#39;utilisateur appartient.

## Ajout d&#39;un utilisateur à un groupe à l&#39;aide de l&#39;appel Ajouter une balise utilisateur {#section_kn3_gbw_xz}

Transmettre le fichier lftoken de l&#39;utilisateur et le nom de balise sélectionné avec la requête POST

Par exemple :

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Pour plus d&#39;informations, voir Référence API &gt; [Ajouter une balise utilisateur](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Ajout d&#39;un utilisateur à un groupe à l&#39;aide de Ping for Pull {#section_kyj_11w_xz}

Utilisez le tableau des balises pour affecter des utilisateurs aux groupes d&#39;utilisateurs. (Les balises peuvent comprendre 1 à 63 caractères alphanumériques et de soulignement.)

Par exemple :

```
"tags": ["moderator", "brand_advocate"],
```

## Ajout d&#39;un utilisateur à un groupe à l&#39;aide de profils distants {#section_uyn_scv_xz}

Ajoutez des balises utilisateur au profil distant, utilisé pour synchroniser les données utilisateur entre votre système de profils personnalisé et Livefyre pour les utilisateurs spécifiques.
