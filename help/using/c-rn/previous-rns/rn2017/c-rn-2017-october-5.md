---
description: Notes de mise à jour de la version du 5 octobre 2017.
seo-description: Notes de mise à jour de la version du 5 octobre 2017.
seo-title: 5 octobre 2017
title: 5 octobre 2017
uuid: 62e9e4ee-1644-4d22-9589-2e208a68aaeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# October 5, 2017{#october}

Notes de mise à jour de la version du 5 octobre 2017.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Identité Livefyre | Les clients qui utilisaient l’identité Livefyre pour se connecter rencontraient des problèmes d’affichage ou de mise à jour de leurs avatars lors de la publication de commentaires dans des applications. Ce problème a été résolu, car les avatars sont désormais visibles et disponibles pour la mise à jour. |
| bogue | Rights Management | Correction d’un bogue d’affichage de noms d’utilisateur longs dans l’onglet Modèle de droits. |
| Amélioration | Flux | Ajout de la capacité d’appuyer sur la touche de tabulation dans un champ de texte Flux pour terminer un terme de recherche. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | Filmstrip | Lorsqu’un client déploie une application de pellicule, le nouveau fichier UGC en flux continu aura une "nouvelle" étiquette à côté de celle-ci afin de les identifier rapidement. |
| Amélioration | Filmstrip | Filmstrip est une toute nouvelle application de visualisation, principalement conçue pour présenter les CU dans des scénarios de commerce électronique, tels que des pages de produits ou des sites Web transactionnels. Film Strip aligne horizontalement l’UGC pour qu’il s’affiche sous forme de pellicule, une pièce à la fois. Les utilisateurs finaux peuvent naviguer dans le film fixe en cliquant sur les flèches latérales pour faire défiler le contenu disponible. |
| Amélioration | Bibliothèque | Les fichiers téléchargés dans la bibliothèque par un client seront automatiquement autorisés. Il s’agit d’une fonctionnalité utile lorsque les utilisateurs ont activé le filtre "exiger des droits accordés" dans leurs applications. |
| Amélioration | Identité Livefyre | Les clients peuvent désormais utiliser leurs identifiants Github pour se connecter à l’Identité Veyre et participer à nos applications de commentaires. |
| bogue | Rights Management | Correction d’un bogue en raison duquel l’insertion de caractères Unicode dans les messages de demande de droits pouvait contourner la validation. |
| Amélioration | SÛR | Améliorations mineures ajoutées à la détection des messages indésirables SAFE. |
| bogue | Service | Les utilisateurs qui ne possèdent pas de courrier électronique valide ont créé des courriers électroniques à leur intention. Correction d’un problème des journaux de production en raison duquel le système n’envoyait pas de courriers électroniques à ces utilisateurs. |
| Amélioration | Studio | Mise à jour du lien Aide de Livefyre dans la barre de navigation supérieure. |
| Amélioration | UGC Commerce | En tant que client, je peux désormais créer une application Livefyre unique (Mosaic, FilmStrip ou Media Wall) et l’incorporer dans plusieurs pages de produits, qui filtre dynamiquement l’UGC approprié pour chaque page de produits (par exemple, UGC avec chaussures pour une page de produits de chaussures). |
| Amélioration | UGC Commerce | Les clients peuvent désormais télécharger manuellement un catalogue de produits Google dans le studio Livefyre à l’aide d’une exportation de fichiers JSON. Cela permet au client d'associer UGC aux produits de ce catalogue et de les visualiser dans nos applications commerciales. |
| Amélioration | UGC Commerce | Les clients peuvent sélectionner les dossiers de produits qu’ils souhaitent utiliser lors du filtrage de leur application de commerce électronique par ID de produit. Par exemple, je veux que ma nouvelle pellicule apparaisse dans les pages de produits chaussures pour femmes et sacs pour femmes de mes femmes, donc je vais sélectionner uniquement les dossiers de produits "Collection chaussures pour femmes" et "Sacs pour femmes". |
| Amélioration | UGC Commerce | Les clients de Livefyre peuvent désormais filtrer l’UGC publié dans leurs applications uniquement s’ils ont obtenu des droits. Par exemple, un client peut traiter et publier une sélection d’éléments, mais ces éléments ne seront rendus dans l’application qu’une fois les droits attribués par l’auteur. Cela est particulièrement important pour les cas d'utilisation du commerce électronique, où l'UGC est utilisé à des fins commerciales. |

