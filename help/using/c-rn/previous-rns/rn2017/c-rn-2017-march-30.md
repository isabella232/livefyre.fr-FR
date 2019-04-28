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
| Bogue | Recherche sociale | Correction d&#39;un bogue qui empêchait la publication des ressources Youtube enregistrées dans la recherche sociale. |
| Amélioration | Synchronisation sociale | Obsolète synchronisation de Twitter Social. |
| Amélioration | Storify 2 | Ajout d&#39;une amélioration pour afficher le message « Aucun résultat trouvé » sur la recherche de rubrique Facebook lorsqu&#39;aucun résultat n&#39;est trouvé. |
| Amélioration | Flux | Ajout de règles de résumé pour les règles SAFE en bas d&#39;une page de flux Twitter. |
| Bogue | Flux | Ajout d&#39;une amélioration de la visibilité de la case à cocher « Utilisateur vérifié » sur les règles de diffusion en continu Twitter lorsque des auteurs exclus sont fournis. |
| Bogue | Flux | Correction d&#39;un bogue qui autorisait l&#39;utilisation de mots-clés anding et d&#39;un filtre Emplacement dans une règle Twitter. |
| Bogue | Studio | Correction d&#39;un bogue qui empêchait l&#39;enregistrement correct de la « balise de fonctionnalité » lorsqu&#39;elle était appliquée. |

## Version UAT

| Type de publication | Composant | Note de version |
|---|---|---|
| Bogue | Contenu de l&#39;application | Modification du comportement de « Plus d&#39;informations » de sorte que s&#39;il existe plusieurs événements d&#39;indicateur anonymes sur un élément de contenu donné, l&#39;événement le plus ancien est toujours affiché. |
| Bogue | Bibliothèque | Correction d&#39;un bogue qui entraînait l&#39;échec intermittent des recherches effectuées dans la bibliothèque avec des hashtags. |
| Bogue | Cartes | Correction d&#39;un bogue de Carte afin de prendre en charge un grand nombre de contenus dans des grappes sur les appareils ios. |
| Amélioration | Mosaic | Ajout de la possibilité de configurer les applications Mosaic pour qu&#39;elles puissent cliquer n&#39;importe où sur une carte de contenu pour ouvrir le modal par type `none` d&#39;animation dans Designer et `cardAnimation: 'off'`, s&#39;il est instancié via le SDK. |
| Bogue | Mosaic | Correction d&#39;un bogue permettant aux utilisateurs de modifier les applications Mosaic dans Designer. |
| Amélioration | Demande de droits | Ajout d&#39;un nouvel état de demande de droits nommé « Échec de la demande » pour mettre en évidence l&#39;échec de l&#39;envoi des messages de demande de droits. |
| Amélioration | Paramètres | Possibilité de créer des règles de modération indésirable dans les paramètres. |
| Amélioration | Recherche sociale | Correction d&#39;un bogue qui empêchait l&#39;affichage des VK.com de publication par l&#39;intermédiaire des recherches sur les réseaux sociaux d&#39;URL. |
| Amélioration | Recherche sociale | Lors de la recherche du contenu Instagram depuis Studio, si la recherche est due à un jeton API Instagram expiré, le message d&#39;erreur indique désormais ce type de message. |
| Bogue | Flux | Correction d&#39;un bogue en raison duquel une bannière « L&#39;application n&#39;acceptait pas de nouvelle bannière de contenu » s&#39;affichait faussement sur les pages de règles de diffusion en continu. |
| Amélioration | Flux | Modification de la valeur par défaut des règles de flux nouvellement créées pour appliquer les règles SAFE, le cas échéant. |
| Amélioration | Flux (anciennement, Règles de traitement) | Suppression de l&#39;option Vines uniquement des règles Flux Twitter/Traitement, tandis que Vines s&#39;affichait désormais sous forme de vidéos Twitter. |
| Bogue | Studio Studio | Correction d&#39;un bogue de sorte que Livefyre Studio se chargeait si https:// était explicitement précédé de l&#39;URL. |

