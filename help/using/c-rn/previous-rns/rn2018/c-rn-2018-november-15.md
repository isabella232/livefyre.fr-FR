---
description: Notes de mise à jour de la version du 15 novembre 2018.
seo-description: Notes de mise à jour de la version du 15 novembre 2018.
seo-title: Notes de mise à jour
solution: Experience Manager
title: Notes de mise à jour
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: 573e815799fbae2c2c4f1d98a01ea0ae04108a34

---


# Notes de mise à jour{#release-notes}

Notes de mise à jour de la version du 15 novembre 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les nouvelles fonctionnalités suivantes ont été publiées dans la version de production de cette version :

* **Mises à jour de la recherche et du flux Instagram.** Vous pouvez utiliser un compte *professionnel* Instagram pour :

   * Effectuez une recherche sur les réseaux sociaux Instagram par utilisateur (l&#39;utilisateur doit également être un compte professionnel Instagram).

   * Créez des flux Instagram à partir d’un compte utilisateur Instagram spécifique (le compte doit également être un compte professionnel), y compris le vôtre.

   * Demandez des droits pour les ressources à Instagram à l’aide d’un processus partiellement automatisé.

   * Pour plus d&#39;informations sur le type de comptes Instagram que vous devez configurer et demander des droits à Instagram, consultez [A propos des comptes](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)Instagram.

* **Surveillance automatique des réponses aux demandes de droits d’utilisation pour les recherches basées sur un compte d’entreprise.** Pour les recherches basées sur les comptes d’entreprise uniquement, vous pouvez contrôler automatiquement les réponses aux demandes de droits et mettre à jour l’historique des activités dans Livefyre.

Pour plus d&#39;informations sur la demande de droits pour les comptes Instagram, consultez [Envoyer manuellement](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) une demande de droits Instagram et [Envoyer une demande](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)de droits Instagram partiellement automatisée.

* **Intégration Adobe Target.** Ajout d’une intégration à Adobe Cible vous permettant de partager directement les applications Livefyre dans votre bibliothèque d’Offres d’Cibles Adobe. Pour plus d’informations sur l’utilisation de Livefyre avec Adobe Cible, voir la documentation [sur les](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html)Cibles.

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

### Version de production

| Type de problème | Composant | Note de mise à jour |
|--- |--- |--- |
| Problème | AppService : Identité Livefyre | Correction d’un problème en raison duquel cliquer sur [! UICONTROL Reset to Default] (Réinitialiser par défaut) n&#39;a pas réinitialisé le logo sous Login Modal dans Studio > Integration Settings (Paramètres d&#39;intégration) > Livefyre Identity (Identité Livefyre) sur l&#39;image par défaut. |
| Problème | Bibliothèque | Correction d’un problème en raison duquel une vidéo téléchargée dans la bibliothèque, puis affichée dans les détails de la ressource, ne s’affichait pas correctement. |
| Problème | Flux | Correction d’un problème en raison duquel les produits ne s’affichaient pas dans une règle de diffusion en continu. |
| Problème | Flux | Correction d’un problème en raison duquel les balises de produit n’étaient pas disponibles pour une règle de diffusion en continu. |
| Amélioration | Studio | Correction d’un problème en raison duquel l’ID de produit ne s’affichait pas dans Livefyre Studio. |
| Problème | Studio : ModQ | Correction d’un problème en raison duquel le contenu supprimé s’affichait toujours dans ModQ après sa suppression. |

### Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Problème | Composant social : Carrousel | Correction d’un problème en raison duquel le lien Partager ne répondait pas et ne copiait pas l’URL comme prévu dans IE11 et Mozilla Firefox. |