---
description: Notes de mise à jour de la version du 15 novembre 2018.
title: Notes de mise à jour
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 6%

---

# Notes de mise à jour{#release-notes}

Notes de mise à jour de la version du 15 novembre 2018.

## Nouvelles fonctionnalités {#section_syx_mdt_wcb}

Les nouvelles fonctionnalités suivantes ont été publiées dans la version de production de cette version :

* **Mises à jour de la recherche et du flux Instagram.** Vous pouvez utiliser un compte  *Instagram pour* effectuer les opérations suivantes :

   * Effectuez une recherche sociale Instagram par utilisateur (l’utilisateur doit également être un compte commercial Instagram).

   * Créez des flux Instagram à partir d’un compte utilisateur Instagram spécifique (le compte doit également être un compte d’entreprise), y compris le vôtre.

   * Demandez des droits sur les ressources à Instagram à l’aide d’un workflow partiellement automatisé.

   * Pour plus d’informations sur le type de comptes Instagram que vous devez configurer et demander des droits à Instagram, voir [À propos des comptes Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Surveillance automatique des réponses de demandes de droits d’utilisation pour les recherches basées sur des comptes d’entreprise.** Pour les recherches basées sur des comptes professionnels uniquement : la possibilité de surveiller automatiquement les réponses aux demandes de droits et de mettre à jour l’historique des activités dans Livefyre est disponible.

Pour plus d’informations sur la demande de droits pour les comptes Instagram, voir [Envoi manuel d’une demande de droits Instagram](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) et [Envoi partiel d’une demande de droits Instagram](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Intégration Adobe Target.** Ajout de l’intégration à Adobe Target qui vous permet de partager directement les applications Livefyre dans votre bibliothèque d’offres Adobe Target. Pour plus d’informations sur l’utilisation de Livefyre avec Adobe Target, voir [Documentation Target](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html).

## Problèmes {#section_ehw_ndt_wcb}

Les problèmes des tableaux suivants ont été résolus dans cette version.

### Version de production

| Type de problème | Composant | Notes de mise à jour |
|--- |--- |--- |
| Problème | AppService : Livefyre Identity | Correction d’un problème en raison duquel le fait de cliquer sur [!UICONTROL Reset to Default] ne réinitialisait pas le logo sous Modal de connexion dans Studio > Paramètres d’intégration > Identité Livefyre à l’image par défaut. |
| Problème | Bibliothèque | Correction d’un problème en raison duquel une vidéo chargée dans la bibliothèque, puis affichée dans le détail de la ressource, ne s’affichait pas correctement. |
| Problème | Flux | Correction d’un problème qui empêchait l’affichage des produits dans une règle de diffusion en continu. |
| Problème | Flux | Correction d’un problème en raison duquel les balises de produit n’étaient pas disponibles pour une règle de diffusion en continu. |
| Amélioration | Studio | Correction d’un problème en raison duquel l’ID de produit ne s’affichait pas dans Livefyre Studio. |
| Problème | Studio : ModQ | Correction d’un problème en raison duquel le contenu supprimé s’affichait toujours dans ModQ après sa suppression. |

### Version UAT

| **Type de problème** | **Composant** | **Notes de mise à jour** |
|---|---|---|
| Problème | Composant Social : Carrousel | Correction d’un problème en raison duquel le lien Partager ne répondait pas et ne copiait pas l’URL comme prévu dans IE11 et Mozilla Firefox. |
