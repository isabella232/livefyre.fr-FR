---
description: Notes de mise à jour de la version du 30 mars 2017.
seo-description: Notes de mise à jour de la version du 30 mars 2017.
seo-title: 30 mars 2017
title: 30 mars 2017
uuid: 2adf04a9-6c52-4fa1-a0c9-b2d3886305e9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 30, 2017{#march}

Notes de mise à jour de la version du 30 mars 2017.

## Version de production

| Type de problème | Composant | Note de mise à jour |
|---|---|---|
| bogue | Recherche sociale | Correction d’un bogue qui empêchait la publication des ressources YouTube enregistrées dans Social Search. |
| Amélioration | Social Sync | Synchronisation sociale Twitter obsolète. |
| Amélioration | Storify 2 | Ajout d’une amélioration afin d’afficher le message "Aucun résultat trouvé" dans la recherche de rubrique Facebook lorsqu’aucun résultat n’est trouvé. |
| Amélioration | Flux | Ajout de règles de résumé pour les règles SAFE au bas d’une page de flux Twitter. |
| bogue | Flux | Ajout d’une amélioration afin de désactiver visiblement la case à cocher "utilisateur vérifié" dans les règles de flux Twitter lorsque des auteurs exclus sont fournis. |
| bogue | Flux | Correction d’un bogue pour autoriser l’utilisation des mots-clés ETing et d’un filtre Emplacement dans une règle Twitter. |
| bogue | Studio | Correction d’un bogue qui empêchait l’enregistrement correct de la balise de fonction lorsqu’elle était appliquée. |

## Version UAT

| Type de problème | Composant | Note de mise à jour |
|---|---|---|
| bogue | Contenu de l’application | Modification du comportement de "Plus d’informations" de sorte que s’il existe plusieurs événements d’indicateur Anonymous sur un élément de contenu donné, l’événement le plus ancien est toujours affiché. |
| bogue | Bibliothèque | Correction d’un bogue en raison duquel les recherches de bibliothèque avec des hashtags échouaient par intermittence. |
| bogue | Mappages | Correction d’un bogue dans les cartes pour la prise en charge d’un grand nombre de contenus dans les grappes de périphériques iOS. |
| Amélioration | Mosaïque | Ajout de la capacité de configurer les applications Mosaic pour qu’elles cliquent n’importe où sur une carte de contenu afin d’ouvrir le module modal par type d’animation `none` dans Designer et `cardAnimation: 'off'`si elles sont instanciées via le SDK. |
| bogue | Mosaïque | Correction d’un bogue pour permettre aux utilisateurs d’apporter des modifications aux applications Mosaic dans Designer. |
| Amélioration | Demande de droits | Ajout d’un nouvel état de demande de droits appelé "Échec de la demande" afin de mettre en évidence lorsque les messages de demande de droits ne parviennent pas à être envoyés. |
| Amélioration | Paramètres | Possibilité pour les clients de créer des règles de modération de messages indésirables dans les paramètres. |
| Amélioration | Recherche sociale | Correction d’un bogue en raison duquel les publications VK.com ne s’affichaient pas par le biais des recherches sur les réseaux sociaux d’URL. |
| Amélioration | Recherche sociale | Lors de la recherche de contenu Instagram à partir de Studio, si la recherche est due à un jeton d’API Instagram expiré, le message d’erreur s’affiche alors. |
| bogue | Flux | Correction d’un bogue en raison duquel une bannière "L’application n’accepte pas le nouveau contenu" s’affichait incorrectement au-dessus des pages des règles de diffusion en continu. |
| Amélioration | Flux | Modification de la valeur par défaut des nouvelles règles de flux pour appliquer des règles SAFE, le cas échéant. |
| Amélioration | Flux (anciennement, Règles de traitement) | Suppression de l’option "Vins" uniquement des règles de flux/traitement Twitter, dans la mesure où les Vins sont désormais affichés sous forme de vidéos Twitter. |
| bogue | Shell Studio | Correction d’un bogue afin que Livefyre Studio se charge si https:// était explicitement ajouté en préfixe à l’URL. |

