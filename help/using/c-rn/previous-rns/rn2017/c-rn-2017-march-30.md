---
description: Notes de mise à jour pour la version du 30 mars 2017.
seo-description: Notes de mise à jour pour la version du 30 mars 2017.
seo-title: 30 mars 2017
title: 30 mars 2017
uuid: 2 adf 04 a 9-6 c 52-4 fa 1-a 0 c 9-b 2 d 3886305 e 9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 30 mars 2017{#march}

Notes de mise à jour pour la version du 30 mars 2017.

## Version de production

| Type de publication | Composant | Note de version |
|---|---|---|
| Bogue | Recherche sociale | Correction d'un bogue qui empêchait la publication des ressources Youtube enregistrées dans la recherche sociale. |
| Amélioration | Synchronisation sociale | Obsolète synchronisation de Twitter Social. |
| Amélioration | Storify 2 | Ajout d'une amélioration pour afficher le message « Aucun résultat trouvé » sur la recherche de rubrique Facebook lorsqu'aucun résultat n'est trouvé. |
| Amélioration | Flux | Ajout de règles de résumé pour les règles SAFE en bas d'une page de flux Twitter. |
| Bogue | Flux | Ajout d'une amélioration de la visibilité de la case à cocher « Utilisateur vérifié » sur les règles de diffusion en continu Twitter lorsque des auteurs exclus sont fournis. |
| Bogue | Flux | Correction d'un bogue qui autorisait l'utilisation de mots-clés anding et d'un filtre Emplacement dans une règle Twitter. |
| Bogue | Studio | Correction d'un bogue qui empêchait l'enregistrement correct de la « balise de fonctionnalité » lorsqu'elle était appliquée. |

## Version UAT

| Type de publication | Composant | Note de version |
|---|---|---|
| Bogue | Contenu de l'application | Modification du comportement de « Plus d'informations » de sorte que s'il existe plusieurs événements d'indicateur anonymes sur un élément de contenu donné, l'événement le plus ancien est toujours affiché. |
| Bogue | Bibliothèque | Correction d'un bogue qui entraînait l'échec intermittent des recherches effectuées dans la bibliothèque avec des hashtags. |
| Bogue | Cartes | Correction d'un bogue de Carte afin de prendre en charge un grand nombre de contenus dans des grappes sur les appareils ios. |
| Amélioration | Mosaic | Ajout de la possibilité de configurer les applications Mosaic pour qu'elles puissent cliquer n'importe où sur une carte de contenu pour ouvrir le modal par type `none` d'animation dans Designer et `cardAnimation: 'off'`, s'il est instancié via le SDK. |
| Bogue | Mosaic | Correction d'un bogue permettant aux utilisateurs de modifier les applications Mosaic dans Designer. |
| Amélioration | Demande de droits | Ajout d'un nouvel état de demande de droits nommé « Échec de la demande » pour mettre en évidence l'échec de l'envoi des messages de demande de droits. |
| Amélioration | Paramètres | Possibilité de créer des règles de modération indésirable dans les paramètres. |
| Amélioration | Recherche sociale | Correction d'un bogue qui empêchait l'affichage des VK.com de publication par l'intermédiaire des recherches sur les réseaux sociaux d'URL. |
| Amélioration | Recherche sociale | Lors de la recherche du contenu Instagram depuis Studio, si la recherche est due à un jeton API Instagram expiré, le message d'erreur indique désormais ce type de message. |
| Bogue | Flux | Correction d'un bogue en raison duquel une bannière « L'application n'acceptait pas de nouvelle bannière de contenu » s'affichait faussement sur les pages de règles de diffusion en continu. |
| Amélioration | Flux | Modification de la valeur par défaut des règles de flux nouvellement créées pour appliquer les règles SAFE, le cas échéant. |
| Amélioration | Flux (anciennement, Règles de traitement) | Suppression de l'option Vines uniquement des règles Flux Twitter/Traitement, tandis que Vines s'affichait désormais sous forme de vidéos Twitter. |
| Bogue | Studio Studio | Correction d'un bogue de sorte que Livefyre Studio se chargeait si https:// était explicitement précédé de l'URL. |

