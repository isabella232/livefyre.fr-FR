---
description: Notes de mise à jour de la version du 21 septembre 2017.
seo-description: Notes de mise à jour de la version du 21 septembre 2017.
seo-title: 21 septembre 2017
title: 21 septembre 2017
uuid: 1132b48a-f85c-4e05-b312-0093db9ebc8f
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# September 21, 2017{#september}

Notes de mise à jour de la version du 21 septembre 2017.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | Commentaires | Les clients peuvent désormais définir la longueur maximale des commentaires dans le cadre de leur configuration réseau. |
| bogue | Applications mobiles | Ce bogue corrige un problème de rendu des réponses imbriquées dans Mobile lorsque les avatars étaient désactivés. |
| bogue | Mosaïque | Correction d’un bogue de production qui entraînait l’affichage des boîtes grises de Mosaic dans IE11 dans UGC. |
| Amélioration | Mosaïque | Les clients peuvent désormais spécifier le nombre de cartes à afficher dans l’application de visualisation Mosaic. |
| bogue | Rights Management | Correction d’un bogue empêchant un utilisateur Studio de demander des droits sur le contenu du carrousel Instagram. |
| bogue | Studio | Ajout de messages d’erreur plus clairs lors de la création de sites. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | Applications | Les clients peuvent désormais créer une application Livefyre unique (Mosaic, Filmstrip ou Media Wall) et l’incorporer dans plusieurs pages de produits, qui filtre dynamiquement l’UGC approprié pour chaque page de produits (par exemple, UGC balisé pour les affichages de chaussures sur la page de produits de chaussures). |
| Amélioration | Filmstrip | Dans l’application Filmstrip, il existe une bannière "Nouveau" qui signale le nouveau contenu dans l’application, de sorte que les utilisateurs finaux puissent rapidement identifier le nouveau contenu. |
| Amélioration | Identité Livefyre | Les clients peuvent désormais utiliser leurs identifiants Github pour se connecter à l’identité Livefyre et participer à nos applications de commentaires. |
| bogue | Rights Management | Correction d’un bogue en raison duquel l’insertion de caractères Unicode dans les messages de demande de droits pouvait contourner la validation. |
| Amélioration | Studio | Mise à jour du lien Aide de Livefyre dans la barre de navigation supérieure. |
| Amélioration | UGC Commerce | Les clients peuvent désormais télécharger manuellement un catalogue de produits Google dans le studio LF à l’aide d’une exportation de fichier JSON. Cela permet au client d'associer UGC aux produits de ce catalogue et de les visualiser dans nos applications commerciales. |
| Amélioration | UGC Commerce | Les clients peuvent sélectionner les dossiers de produits qu’ils souhaitent utiliser lors du filtrage de leur application de commerce électronique par ID de produit. Par exemple, je veux que ma nouvelle pellicule apparaisse dans les pages de produits pour chaussures pour femmes et sacs pour femmes, donc je ne sélectionnerai que les dossiers de produits "Collection de chaussures pour femmes" et "Sacs pour femmes". |
| Amélioration | UGC Commerce | Les clients de Livefyre peuvent désormais filtrer les UGC publiées dans leurs applications uniquement s’ils disposent de droits d’accès. Par exemple, un client peut traiter et publier une sélection d’éléments, mais ces éléments ne seront rendus dans l’application que lorsqu’ils auront été autorisés par l’auteur. Cela est particulièrement important pour les cas d'utilisation du commerce électronique, où l'UGC est utilisé à des fins commerciales. |

