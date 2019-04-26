---
description: Notes de mise à jour pour la version du 23 mars 2018.
seo-description: Notes de mise à jour pour la version du 23 mars 2018.
seo-title: 23 mars 2018
solution: Experience Manager
title: 23 mars 2018
uuid: b 69 b 8715-ace 4-48 e 0-8 f 54-ce 4 e 12170 ef 3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 23 mars 2018{#march}

Notes de mise à jour pour la version du 23 mars 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les fonctionnalités suivantes sont nouvelles dans la version de production de cette version :

* **Nouveau en production :** Facebook a créé une mise à jour de sécurité de la connexion Facebook qui provoquera le mauvais fonctionnement de la connexion Facebook d'un client. Pour résoudre ce problème, vous devez :

   1. Ajoutez l'URL suivante au **[!UICONTROL Valid OAuth redirect URIs]** champ dans Paramètres oauth client. Remplacez `<networkname>` le nom du réseau correct :
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Passez **[!UICONTROL Use Strict Mode for Redirect URI]****[!UICONTROL Yes]**à.

* **Nouveau dans UAT :** Vous pouvez désormais choisir le seuil de confiance pour les balises dynamiques dans les flux. La définition du score de précision (0-100) pour les balises permet de contrôler l'exactitude des ressources que nous récupérons.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Mur multimédia | Correction d'un problème dans le mur multimédia en raison duquel les balises n'étaient pas cliquables lorsqu'une publication Instagram était ajoutée à partir d'une règle de diffusion en continu. |
| Bogue | Modq | Correction d'un problème en raison duquel modq ne se chargeait pas correctement. |
| Bogue | Modq | Correction d'un problème en raison duquel l'incorporation de l'audio empêchait le fonctionnement de modq. |

## Version UAT

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Amélioration | Film fixe | Correction de certains problèmes pour rendre le film fixe plus accessible. |
| Amélioration | Studio | Vous pouvez désormais vous connecter à Livefyre à l'aide d'une connexion IMS. |

