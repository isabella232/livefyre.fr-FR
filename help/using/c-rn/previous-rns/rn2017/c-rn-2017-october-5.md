---
description: Notes de mise à jour de la version du 5 octobre 2017.
title: 5 octobre 2017
exl-id: 6e39a86e-82dd-47ff-ad68-2b483f8b1921
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 4%

---

# 5 octobre 2017{#october}

Notes de mise à jour de la version du 5 octobre 2017.

## Version de production

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| bogue | Identité Livefyre | Les clients qui utilisaient l’identité Livefyre pour se connecter rencontraient des problèmes d’affichage ou de mise à jour de leurs avatars lors de la publication de commentaires sur des applications. Ce problème a été corrigé car les avatars sont désormais visibles et disponibles pour la mise à jour. |
| bogue | Rights Management | Correction d’un bogue d’affichage de noms d’utilisateur longs dans l’onglet Modèle de droits. |
| Amélioration | Flux | Ajoute la possibilité d’appuyer sur la touche de tabulation dans un champ de texte Flux pour terminer un terme de recherche. |

## Version UAT

| **Type de problème** | **Composant** | **Note de mise à jour** |
|---|---|---|
| Amélioration | Filmstrip | Lorsqu’un client déploie une application de bande de film, l’UGC nouvellement diffusé aura une &quot;nouvelle&quot; étiquette à côté de celle-ci afin de les identifier rapidement. |
| Amélioration | Filmstrip | Filmstrip est une toute nouvelle application de visualisation, principalement conçue pour présenter l’UGC dans des scénarios de commerce électronique, tels que des pages de produits ou des sites Web transactionnels. Film Strip aligne horizontalement l&#39;UGC pour qu&#39;il s&#39;affiche sous forme de pellicule, une pièce à la fois. Les utilisateurs finaux peuvent naviguer dans le film strip en cliquant sur les flèches latérales pour faire défiler le contenu disponible. |
| Amélioration | Bibliothèque | Les fichiers téléchargés dans la bibliothèque par un client seront automatiquement autorisés. Il s’agit d’une fonctionnalité utile lorsque les utilisateurs ont activé le filtre &quot;Exiger des droits accordés&quot; dans leurs applications. |
| Amélioration | Identité Livefyre | Les clients peuvent désormais utiliser leurs identifiants Github pour se connecter à l&#39;Identité Livefyre et participer à nos applications de commentaires. |
| bogue | Rights Management | Correction d’un bogue en raison duquel l’insertion de caractères Unicode dans les messages de demande de droits pouvait contourner la validation. |
| Amélioration | SÉCURITÉ | Des améliorations mineures ont été apportées à la détection des messages indésirables dans le logiciel SAFE. |
| bogue | Service | Les utilisateurs qui ne disposent pas de courriers électroniques valides ont créé des courriers électroniques à leur intention. Correction d’un problème des journaux de production en raison duquel le système n’envoyait pas de messages électroniques à ces utilisateurs. |
| Amélioration | Studio | Mise à jour du lien Aide de Livefyre dans la barre de navigation supérieure. |
| Amélioration | UGC Commerce | En tant que client, je peux maintenant créer une seule application Livefyre (Mosaic, FilmStrip ou Media Wall) et l’incorporer dans plusieurs pages de produits, qui filtres dynamiquement l’UGC approprié pour chaque page de produits (par exemple UGC avec chaussures pour une page de produits Chaussures). |
| Amélioration | UGC Commerce | Les clients peuvent désormais télécharger manuellement un catalogue de produits Google dans le studio Livefyre à l’aide d’une exportation de fichiers JSON. Cela permet au client d&#39;associer UGC aux produits de ce catalogue et de les visualiser dans nos applications commerciales. |
| Amélioration | UGC Commerce | Les clients peuvent sélectionner les dossiers de produits à utiliser lors du filtrage de leur application de commerce électronique par ID de produit. Par exemple, je veux que ma nouvelle pellicule apparaisse dans les pages de mes produits chaussures pour femme et sacs pour femme, par conséquent, je ne sélectionnerai que les dossiers de produit &quot;Collection de chaussures pour femme&quot; et &quot;Sacs pour femme&quot;. |
| Amélioration | UGC Commerce | Les clients de Livefyre ne peuvent désormais filtrer l’UGC publié sur leurs applications que s’ils ont obtenu des droits. Par exemple, un client peut traiter et publier une sélection d’éléments, mais ces éléments ne seront rendus dans l’application qu’une fois les droits accordés par l’auteur. Cela est particulièrement important dans les cas d&#39;utilisation du commerce électronique, où l&#39;UGC est utilisé à des fins commerciales. |
