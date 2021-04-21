---
description: Notes de mise à jour de la version du 15 novembre 2018.
title: Notes de mise à jour
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 6%

---

# Notes de mise à jour{#release-notes}

Notes de mise à jour de la version du 15 novembre 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les nouvelles fonctionnalités suivantes ont été publiées dans la version de production de cette version :

* **Mises à jour de la recherche et du flux Instagram.** Vous pouvez utiliser un  *compte* commercial Instagram pour :

   * Effectuez une recherche sur les réseaux sociaux Instagram par utilisateur (l’utilisateur doit également être un compte commercial Instagram).

   * Créez des flux Instagram à partir d’un compte utilisateur Instagram spécifique (le compte doit également être un compte d’entreprise), y compris le vôtre.

   * Demandez des droits pour les ressources à Instagram en utilisant un processus partiellement automatisé.

   * Pour plus d’informations sur le type de comptes Instagram que vous devez configurer et demander des droits à Instagram, voir [À propos des comptes Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Surveillance automatique des réponses aux demandes de droits d’utilisation pour les recherches basées sur un compte d’entreprise.** Pour les recherches basées sur les comptes d’entreprise uniquement, vous pouvez contrôler automatiquement les réponses aux demandes de droits et mettre à jour l’historique des activités dans Livefyre.

Pour plus d’informations sur la façon de demander des droits pour les comptes Instagram, voir [Envoyer manuellement la demande de droits Instagram](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) et [Envoyer une demande de droits Instagram partiellement automatisée](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Intégration Adobe Target.** Intégration Ajoutée avec Adobe Target vous permettant de partager directement les applications Livefyre dans votre bibliothèque d’Offres Adobe Target. Pour plus d&#39;informations sur l&#39;utilisation de Livefyre avec Adobe Target, consultez la [documentation sur la Cible](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html).

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

### Version de production

| Type de problème | Composant | Note de mise à jour |
|--- |--- |--- |
| Problème | AppService : Identité Livefyre | Correction d’un problème en raison duquel le fait de cliquer sur [!UICONTROL Reset to Default] ne réinitialisait pas le logo sous Login Modal in Studio > Integration Settings > Livefyre Identity à l’image par défaut. |
| Problème | Bibliothèque | Correction d’un problème en raison duquel une vidéo téléchargée dans la bibliothèque, puis affichée dans les détails de la ressource, ne s’affichait pas correctement. |
| Problème | Flux | Correction d’un problème en raison duquel les produits ne s’affichaient pas dans une règle de diffusion en continu. |
| Problème | Flux | Correction d’un problème en raison duquel les balises de produit n’étaient pas disponibles pour une règle de diffusion en continu. |
| Amélioration | Studio | Correction d’un problème en raison duquel l’ID de produit ne s’affichait pas dans Livefyre Studio. |
| Problème | Studio : ModQ | Correction d’un problème en raison duquel le contenu supprimé s’affichait toujours dans ModQ après sa suppression. |

### Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Problème | Composant social : Carrousel | Correction d’un problème en raison duquel le lien Partager ne répondait pas et ne copiait pas l’URL comme prévu dans IE11 et Mozilla Firefox. |
