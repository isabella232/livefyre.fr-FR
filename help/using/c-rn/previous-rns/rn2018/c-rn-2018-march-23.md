---
description: Notes de mise à jour de la version du 23 mars 2018.
seo-description: Notes de mise à jour de la version du 23 mars 2018.
seo-title: 23 mars 2018
solution: Experience Manager
title: 23 mars 2018
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 7%

---


# 23 mars 2018{#march}

Notes de mise à jour de la version du 23 mars 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* **Nouveau en production :** Facebook a créé une mise à jour de sécurité de la connexion à Facebook qui entraîne le mauvais fonctionnement de la connexion à Facebook d’un client. Pour résoudre ce problème, vous devez :

   1. Ajoutez l’URL suivante au champ **[!UICONTROL Valid OAuth redirect URIs]** dans Paramètres OAuth du client. Remplacez `<networkname>` par le nom réseau correct :
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Basculez **[!UICONTROL Use Strict Mode for Redirect URI]** sur **[!UICONTROL Yes]**.

* **Nouveau dans UAT :** Vous pouvez désormais choisir le seuil de confiance pour les balises actives dans les flux. La définition du score de précision (0-100) pour les balises permet de contrôler la précision des ressources que nous récupérons.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Mur multimédia | Correction d’un problème dans le mur multimédia en raison duquel les balises ne pouvaient pas être cliquées lorsqu’une publication Instagram était ajoutée à partir d’une règle de diffusion en continu. |
| bogue | ModQ | Correction d’un problème en raison duquel ModQ ne se chargeait pas correctement. |
| bogue | ModQ | Correction d’un problème en raison duquel l’incorporation d’audio entraînait l’arrêt du fonctionnement de ModQ. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | Filmstrip | Correction de certains problèmes pour rendre Filmstrip plus accessible. |
| Amélioration | Studio | Vous pouvez désormais vous connecter à Livefyre à l’aide d’une connexion IMS. |

