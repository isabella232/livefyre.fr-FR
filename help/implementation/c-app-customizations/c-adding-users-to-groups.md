---
description: Ajoutez une balise d’utilisateur à un compte pour ajouter un utilisateur à un groupe.
seo-description: Ajoutez une balise d’utilisateur à un compte pour ajouter un utilisateur à un groupe.
seo-title: Ajouter des utilisateurs aux groupes
solution: Experience Manager
title: Ajouter des utilisateurs aux groupes
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# Ajouter des utilisateurs aux groupes{#adding-users-to-groups}

Ajoutez une balise d’utilisateur à un compte pour ajouter un utilisateur à un groupe.

Les balises d&#39;utilisateur peuvent être mises en oeuvre pour les systèmes de profil propriétaire et d&#39;entreprise et peuvent être ajoutées aux comptes par plusieurs moyens :

* La création de propriétaires et de modérateurs via Studio attribue la balise d’utilisateur &quot;Modérateur&quot; au compte.
* La création de groupes d’utilisateurs et l’ajout d’utilisateurs à ces groupes via Studio appliquent automatiquement aux utilisateurs sélectionnés des balises d’utilisateur portant le nom du groupe.
* Les balises d’utilisateur peuvent également être appliquées directement aux comptes à l’aide de l’appel [Ajouter la balise d’utilisateur HTTP](https://api.livefyre.com/docs#add-user-tag) ou de l’appel Ping for Pull.

>[!NOTE]
>
>Les deux méthodes d’API, l’appel de balise d’utilisateur d’Ajoute HTTP et la méthode Ping for Pull, remplaceront toutes les balises précédemment attribuées au compte par d’autres moyens. Par conséquent, sélectionnez une méthode et utilisez-la de manière cohérente tout au long de votre processus.

## Ajouter un utilisateur à un groupe à partir de la page Utilisateurs de Studio {#section_qgq_nbw_xz}

* Cliquez sur **[!UICONTROL Add Group]** ou sur l&#39;étiquette de groupe sous un nom d&#39;utilisateur quelconque pour ouvrir le menu des groupes.
* Faites défiler la liste et recherchez le groupe auquel vous souhaitez ajouter l’utilisateur. Vous pouvez entrer un nom de groupe dans la zone **[!UICONTROL Search]** située en haut de la liste déroulante.
* Cochez la case en regard du ou des groupes auxquels l’utilisateur doit être ajouté, puis appuyez sur Retour.

Le profil de l’utilisateur affiche soit le nom du groupe (si l’utilisateur se trouve dans un seul groupe), soit le nombre de groupes auxquels il appartient.

## Ajouter un utilisateur à un groupe à l’aide de l’appel Ajouter la balise d’utilisateur {#section_kn3_gbw_xz}

Transmettez le jeton LFToken de l’utilisateur et le nom de balise sélectionné avec la demande du POST.

Par exemple :

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Pour plus d’informations, voir Référence de l’API > [Ajouter la balise d’utilisateur](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Ajouter un utilisateur à un groupe à l’aide de Ping for Pull {#section_kyj_11w_xz}

Utilisez le tableau de balises pour affecter des utilisateurs à des groupes d’utilisateurs. (Les balises peuvent contenir de 1 à 63 caractères alphanumériques et des caractères de soulignement.)

Par exemple :

```
"tags": ["moderator", "brand_advocate"],
```

## Ajouter un utilisateur à un groupe à l’aide de Profils distants {#section_uyn_scv_xz}

Ajoutez des balises d’utilisateur au Profil distant, utilisé pour synchroniser les données d’utilisateur entre votre système de profil personnalisé et Livefyre, pour les utilisateurs spécifiques.
