---
description: Notes de mise à jour de la version du 23 février 2017.
title: 23 février 2017
exl-id: 3a5708a1-4be6-447f-ae6e-8f5a37171ed7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 7%

---

# 23 février 2017{#february}

Notes de mise à jour de la version du 23 février 2017.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | SDK Android | Réorganisation du SDK Android afin de s’assurer que les répertoires d’implémentation de référence et d’exemple sont plus clairement identifiables par leur emplacement. |
| Amélioration | SDK Android | Le SDK Android a été modifié pour prendre désormais en charge une version minimale de SDK de 14 (moins de 16). |
| bogue | Applications de conversation | Amélioration des applications de conversation pour qu’elles se connectent toujours aux profils utilisateur, même sans intégration complète de l’authentification. |
| bogue | Mosaïque | Correction d’un bogue en raison duquel toutes les images Twitter étaient désormais accessibles via HTTPS. |
| Amélioration | Recherche et flux | Ajoute la possibilité de rechercher par Instagram Places (enregistrements) dans Library Instagram Search et Instagram Stream Rules. |
| bogue | Paramètres | Correction d’un bogue qui empêchait l’enregistrement des comptes sociaux Twitter. |
| bogue | Recherche sociale | Correction d’un bogue en raison duquel l’option &quot;Masquer les images explicites&quot; ne fonctionnait pas correctement. |
| Amélioration | Storify 2 | Amélioration de la fonctionnalité Storify 2 pour la prise en charge des liens permules l’ouverture d’un module modal (auparavant, l’application faisait défiler l’écran jusqu’à l’emplacement de publication sur la page). Dans Storify 2’s Designer, nous avons ajouté une configuration permettant de basculer entre le comportement de liaison de permalink de type Scroll et Modal. Le comportement par défaut sera celui du lien permalink modal. |
| Amélioration | Storify 2 | Amélioration de l’intégration Storify 2 de Google AMP pour produire un fichier CSS plus petit. |
| Amélioration | Flux | Correction d’un bogue des règles Facebook en raison duquel le contenu était extrait avec des métadonnées incomplètes. |
| bogue | Flux | Amélioration du contenu (images et vidéos) des règles de diffusion en continu des courriels pour qu’il soit disponible via HTTPS. |
| bogue | Flux | Ajouté une étiquette pour la valeur du rayon de mille dans les cartes dans les règles de flux Twitter. |
| bogue | Flux | Correction d’un bogue lié aux règles de gestion dynamique des pages Facebook et Facebook afin d’extraire correctement les publications avec plusieurs pièces jointes. |
| Amélioration | Flux | Ajouté une nouvelle fonctionnalité permettant aux utilisateurs de choisir d’appliquer ou de désactiver les règles SAFE par règle de flux. |
| Amélioration | Studio | Correction d’un bogue en raison duquel le contenu n’était pas publié ou enregistré correctement s’il existait déjà. |
| bogue | Studio | Correction d’un bogue en raison duquel plusieurs &amp;’s n’étaient pas ajoutés à l’URL lors de l’utilisation de filtres dans Studio. |
| bogue | Studio | Correction d’un bogue en raison duquel certaines cases à cocher des filtres Studio ne pouvaient pas être désactivées. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Applications | Correction d’un bogue pour afficher le contenu dans les modèles de médias avec les proportions correctes. |
| bogue | Mur multimédia | Correction d’un bogue en raison duquel Media Walls ne s’affichait pas si des caractères étrangers spécifiques étaient inclus. |
| bogue | Outils | Correction d’un bogue en raison duquel les pages se chargeaient incorrectement lors de la pagination dans les résultats de la recherche avec l’option &quot;Masquer les images explicites&quot; activée. |
| Amélioration | Studio | Augmentation du temps de session avant l’expiration des sessions de connexion utilisateur de Studio. Une fois qu’une session Studio expire, l’utilisateur est redirigé vers la connexion. |
| bogue | Studio | Correction d’un bogue qui empêchait parfois les utilisateurs d’enregistrer des informations d’identification Instagram. |
| bogue | Studio | Correction d’un bogue qui empêchait l’enregistrement correct de la &quot;balise de fonction&quot; lorsqu’elle était appliquée. |
