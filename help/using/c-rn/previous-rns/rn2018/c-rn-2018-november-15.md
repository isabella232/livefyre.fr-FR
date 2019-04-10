---
description: Notes de mise à jour pour la version du 15 novembre 2018.
seo-description: Notes de mise à jour pour la version du 15 novembre 2018.
seo-title: Notes de mise à jour
solution: Experience Manager
title: Notes de mise à jour
uuid: 34 e 64943-dea 6-46 ac -9 fcc -8 febeab 6 aa 42
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Notes de mise à jour{#release-notes}

Notes de mise à jour pour la version du 15 novembre 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les nouvelles fonctionnalités suivantes ont été publiées dans la version de production de cette version :

* **Mises à jour de la recherche et du flux Instagram.** Vous pouvez utiliser un *compte d'entreprise Instagram* pour :

   * Effectuez une recherche sociale Instagram par utilisateur (l'utilisateur doit être un compte d'entreprise Instagram également).

   * Créez des flux Instagram à partir d'un compte utilisateur Instagram spécifique (ce compte doit également être un compte professionnel), notamment le vôtre.

   * Demandez des droits pour les ressources d'Instagram à l'aide d'un processus partiellement automatisé.

   * Pour plus d'informations sur le type de comptes Instagram dont vous avez besoin pour configurer et demander des droits à partir d'Instagram, voir [A propos des comptes Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Surveillance automatique des réponses aux demandes de droits d'utilisation pour les recherches basées sur un compte professionnel.** Pour les recherches basées sur des comptes professionnels uniquement, la possibilité de surveiller automatiquement les réponses aux demandes de droits et de mettre à jour l'historique des activités dans Livefyre est disponible.

Pour plus d'informations sur la manière de demander des droits pour les comptes Instagram, voir [Envoi manuel de requêtes de droits Instagram](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) et [Envoi d'une demande de droits Instagram partiellement automatisée](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Intégration d'Adobe Target.** Ajout de l'intégration à Adobe Target vous permettant de partager des applications Livefyre directement dans votre bibliothèque d'offres Adobe Target. Pour plus d'informations sur l'utilisation de Livefyre avec Adobe Target, voir [la documentation Target](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html).

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

### Version de production

| Type de publication | Composant | Note de version |
|--- |--- |--- |
| Problème | Appservice : Identité Livefyre | Correction d'un problème [en raison duquel vous cliquiez sur ! UICONTROL Reset To Default] did not resinitithe the logo under Login Modal in Studio > Integration Settings > Livefyre Identity to the default image. |
| Problème | Bibliothèque | Correction d'un problème en raison duquel une vidéo téléchargée dans la bibliothèque n'affichait pas correctement les détails de la ressource. |
| Problème | Flux | Correction d'un problème qui empêchait l'affichage des produits dans une règle de diffusion en continu. |
| Problème | Flux | Correction d'un problème en raison duquel les balises de produit n'étaient pas disponibles pour une règle de diffusion en continu. |
| Amélioration | Studio | Correction d'un problème en raison duquel l'ID de produit ne s'affichait pas dans Livefyre Studio. |
| Problème | Studio : Modq | Correction d'un problème en raison duquel le contenu supprimé s'affichait toujours dans modq après sa suppression. |

### Version UAT

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Problème | Composant Social : Carrousel | Correction d'un problème en raison duquel le lien Partager n'avait pas répondu et copiait l'URL comme prévu dans IE 11 et Mozilla Firefox. |