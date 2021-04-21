---
description: Notes de mise à jour de la version du 9 août 2018.
title: 9 août 2018
exl-id: 7b2fb562-33bf-4c34-ab83-5fc34f5d1f4f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 8%

---

# 9 août 2018{#august}

Notes de mise à jour de la version du 9 août 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

**Balises dynamiques vidéo :** les utilisateurs peuvent désormais afficher les balises actives pour les vidéos de moins de 50 Mo.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Contenu de l’application | Correction d’un problème qui empêchait les administrateurs et les gestionnaires de contenu de modifier le contenu dans l’application Contenu. |
| Amélioration | Applications | Les réseaux sociaux ont apporté des modifications à la vie privée qui signifient que les mentions sociales ne seront plus prises en charge pour Facebook ou Twitter. |
| Amélioration | Applications | Les réseaux sociaux ont apporté des changements à la vie privée. La fonction &quot;Publier vers&quot; qui publie automatiquement du contenu sur les réseaux sociaux (Facebook, LinkedIn, Twitter) a été supprimée. |
| Amélioration | RGPD | Suppression de la bascule pour le mode Détails de la page des détails de la requête sous Paramètres > Confidentialité. La bascule du mode Détails est toujours accessible en ajoutant /dbg à la fin de l&#39;URL. |
| bogue | Intégration : AEM | Correction d’un problème en raison duquel le glisser-déplacer des applications Livefyre dans AEM apparaissait comme créant plusieurs applications. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel une ressource n’était pas correctement enregistrée dans la bibliothèque. |
| bogue | Identité Livefyre | Correction d’un problème d’identité LF qui provoquait des erreurs 403 lors de la connexion. |
| bogue | Recherche sociale | Correction d’un problème en raison duquel les utilisateurs ne pouvaient pas rechercher des publications Facebook publiques à l’aide de l’option URL dans la recherche sociale. |
| Amélioration | Social Sync | Les réseaux sociaux ont apporté des modifications à la vie privée qui signifient que Social Sync ne sera plus pris en charge pour Facebook. |
| Amélioration | Flux | Désormais, lorsque vous supprimez une application, vous supprimez tous les flux associés à cette application. |
| Amélioration | Studio | Les clients ont désormais la possibilité d&#39;émettre des événements Livefyre à Adobe Analytics individuellement, par opposition aux lots. |
| Amélioration | Studio | Les fenêtres modales qui s’affichent dans les applications de conversation pour les réseaux sociaux seront désormais des fenêtres modales du réseau social au lieu de Adobe Experience Manager Livefyre ou d’autres fenêtres modales de marque. |

## Version UAT

Les problèmes des tableaux suivants ont été résolus dans la version UAT.

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | RGPD | Correction d’un problème en raison duquel les messages d’exclusion ne s’affichaient pas pour certaines vidéos Instagram. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel une carte dotée de droits accordés affichait manuellement le mauvais état de demande de droits. |
| bogue | Bibliothèque | Correction d’un problème en raison duquel un fichier ne pouvait pas être enregistré dans un dossier. |
| bogue | Bibliothèque/Recherche | Restauration de la capacité de rechercher des URL à partir d’Instagram dans Social Search. |
| bogue | ModQ | Correction d’un problème en raison duquel le menu Plus d’informations dans ModQ ne s’affichait pas comme prévu. |
| bogue | Rights Management | Correction d’un problème en raison duquel le tri dans ModQ devait se trouver dans une position fixe lors du défilement de la page. |
| bogue | Flux | Correction d’un problème d’affichage des flux sur l’environnement d’évaluation. |
| Amélioration | Flux | Ajouté une bascule SFW (Safe For Work) et Not Safe For Work (NSFW) pour basculer dans Streams. |
| Amélioration | Studio | Ajouté la fonctionnalité de balises actives au contenu téléchargé vers la bibliothèque Livefyre Studio via FileStack (fonctionnalité de téléchargement dans tous les fichiers). |
