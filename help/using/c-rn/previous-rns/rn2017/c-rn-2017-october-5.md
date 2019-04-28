---
description: Notes de mise à jour pour la version du 5 octobre 2017.
seo-description: Notes de mise à jour pour la version du 5 octobre 2017.
seo-title: 5 octobre 2017
title: 5 octobre 2017
uuid: 62 e 9 e 4 ee -1644-4 d 22-9589-2 e 208 a 68 aaeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 5 octobre 2017{#october}

Notes de mise à jour pour la version du 5 octobre 2017.

## Version de production

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Bogue | Identité Livefyre | Les clients qui utilisent l&#39;identité Livefyre pour se connecter rencontrent des problèmes lors de la consultation ou de la mise à jour de leurs avatars lors de la publication dans des applications de commentaire. Désormais, les avatars sont maintenant visibles et disponibles pour la mise à jour. |
| Bogue | Rights Management | Correction d&#39;un bogue de l&#39;affichage des longs noms d&#39;utilisateur dans l&#39;onglet Droits des droits. |
| Amélioration | Flux | Ajout de la capacité d&#39;atteindre la touche de tabulation dans un champ de texte Flux pour terminer un terme de recherche. |

## Version UAT

| **Type de publication** | **Composant** | **Note de version** |
|---|---|---|
| Amélioration | Film fixe | Lorsqu&#39;un client déploie une application Strip Strip, l&#39;UGC nouvellement diffusée en flux continu dispose d&#39;une étiquette « nouvelle » pour les identifier rapidement. |
| Amélioration | Film fixe | Filmstrip est une nouvelle application de visualisation de marque, principalement conçue pour présenter UGC dans des scénarios de commerce électronique, tels que des pages de produits ou des sites Web transactionnels. La bande de film aligne horizontalement l&#39;UGC à afficher sous forme de pellicule, une partie à la fois. Fin : les utilisateurs peuvent parcourir le film fixe en cliquant sur les flèches latérales pour faire défiler le contenu disponible. |
| Amélioration | Bibliothèque | Les fichiers téléchargés dans la bibliothèque par un client sont automatiquement autorisés. Il s&#39;agit d&#39;une fonctionnalité utile lorsque les utilisateurs ont activé le filtre « Requiert des droits » dans leur application. |
| Amélioration | Identité Livefyre | Les clients peuvent désormais utiliser leurs informations d&#39;identification Github pour se connecter à livefyre Identité et participer à nos applications de commentaires. |
| Bogue | Rights Management | Correction d&#39;un bogue qui autorisait l&#39;insertion de caractères Unicode dans les messages de demande de droits pour contourner la validation. |
| Amélioration | SAFE | Améliorations mineures apportées à la détection SAFE Spam. |
| Bogue | Service | Les utilisateurs qui ne disposent pas de courriers électroniques valides ont des e-mails construits pour eux. Correction d&#39;un problème lié aux journaux de production, en raison duquel le système n&#39;envoyait pas de courrier électronique à ces utilisateurs. |
| Amélioration | Studio | Mise à jour du lien Aide Livefyre dans la barre de navigation supérieure. |
| Amélioration | Commerce UGC | En tant que client, je peux désormais créer une application Livefyre unique (Mosaic, filmstrip ou Media Wall) et l&#39;incorporer dans plusieurs pages de produits, qui filtre dynamiquement le contenu UGC approprié pour chaque page de produit (par exemple UGC avec chaussures pour une page de produit Chaussures). |
| Amélioration | Commerce UGC | Les clients peuvent désormais transférer manuellement un catalogue de produits Google dans un studio Livefyre en utilisant une exportation de fichiers JSON. Cela permet au client de regrouper UGC avec des produits provenant de ce catalogue et de les visualiser dans nos applications commerciales. |
| Amélioration | Commerce UGC | Les clients peuvent sélectionner les dossiers de produits à utiliser lors du filtrage de leur application e-commerce par - ID du produit. Par exemple, je souhaite que mon nouveau film fixe apparaisse dans les pages des produits pour femme et que les femmes contiennent des pages de produits. Je sélectionne donc uniquement les dossiers « Collection pour femmes » et « Sacs pour femmes ». |
| Amélioration | Commerce UGC | Les clients Livefyre peuvent désormais filtrer l&#39;UGC publié dans leurs applications uniquement s&#39;ils ont été autorisés. Par exemple, un client peut traiter et publier une sélection d&#39;éléments, mais ces éléments ne sont rendus dans l&#39;application qu&#39;une fois les droits accordés par l&#39;auteur. Cela est particulièrement important pour les cas d&#39;utilisation du commerce électronique, où le protocole UGC est utilisé à des fins commerciales. |

