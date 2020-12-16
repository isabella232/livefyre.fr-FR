---
description: Notes de mise à jour de la version du 30 mars 2017.
seo-description: Notes de mise à jour de la version du 30 mars 2017.
seo-title: 30 mars 2017
title: 30 mars 2017
uuid: 2adf04a9-6c52-4fa1-a0c9-b2d3886305e9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 7%

---


# 30 mars 2017{#march}

Notes de mise à jour de la version du 30 mars 2017.

## Version de production

| Type de problème | Composant | Note de mise à jour |
|---|---|---|
| bogue | Recherche sociale | Correction d’un bogue qui empêchait la publication des ressources YouTube enregistrées dans Social Search. |
| Amélioration | Social Sync | Synchronisation sociale Twitter obsolète. |
| Amélioration | Storify 2 | Amélioration Ajoutée afin d’afficher le message &quot;Aucun résultat trouvé&quot; sur la recherche de rubrique Facebook lorsqu’aucun résultat n’est trouvé. |
| Amélioration | Flux | Règles de résumé Ajoutées pour les règles SAFE au bas d’une page de flux Twitter. |
| bogue | Flux | Amélioration Ajoutée afin de désactiver de manière visible la case à cocher &quot;utilisateur vérifié&quot; dans les règles de flux Twitter lorsque des auteurs exclus sont fournis. |
| bogue | Flux | Correction d’un bogue qui autorisait l’utilisation de mots-clés ETing et d’un filtre Emplacement dans une règle Twitter. |
| bogue | Studio | Correction d’un bogue qui empêchait l’enregistrement correct de la &quot;balise de fonction&quot; lorsqu’elle était appliquée. |

## Version UAT

| Type de problème | Composant | Note de mise à jour |
|---|---|---|
| bogue | Contenu de l’application | Modification du comportement de &quot;Plus d’informations&quot; de sorte que si plusieurs événements d’indicateur Anonymous figurent sur un élément de contenu donné, le premier événement est toujours affiché. |
| bogue | Bibliothèque | Correction d’un bogue en raison duquel les recherches de la bibliothèque avec des hashtags échouaient par intermittence. |
| bogue | Mappages | Correction d’un bogue dans Maps pour la prise en charge d’un grand nombre de contenus dans des grappes sur des périphériques iOS. |
| Amélioration | Mosaïque | Ajouté la possibilité de configurer des applications Mosaic pour qu’elles cliquent n’importe où sur une carte de contenu afin d’ouvrir le module modal par type d’animation `none` dans Designer et `cardAnimation: 'off'`si elles sont instanciées via le SDK. |
| bogue | Mosaïque | Correction d’un bogue en raison duquel les utilisateurs pouvaient apporter des modifications aux applications Mosaic dans Designer. |
| Amélioration | Demande de droits | Ajouté un nouvel état de demande de droits appelé &quot;Échec de la demande&quot; afin de le mettre en évidence lorsque les messages de demande de droits ne parviennent pas à être envoyés. |
| Amélioration | Paramètres | Ajoute la possibilité pour les clients de créer des règles de modération indésirable dans les paramètres. |
| Amélioration | Recherche sociale | Correction d’un bogue en raison duquel les publications VK.com ne s’affichaient pas par le biais des recherches d’URL Social. |
| Amélioration | Recherche sociale | Lors de la recherche de contenu Instagram à partir de Studio, si la recherche est due à un jeton d&#39;API Instagram expiré, le message d&#39;erreur s&#39;affiche désormais comme tel. |
| bogue | Flux | Correction d’un bogue en raison duquel une bannière &quot;L’application n’accepte pas de nouveau contenu&quot; s’affichait incorrectement au-dessus des pages des règles de diffusion en continu. |
| Amélioration | Flux | Modification de la valeur par défaut des nouvelles règles de flux pour appliquer des règles SAFE le cas échéant. |
| Amélioration | Flux (anciennement, Traiter les règles) | Suppression de l’option &quot;Vins&quot; uniquement des règles de flux/traitement Twitter, dans la mesure où les vignes s’affichent désormais sous forme de vidéos Twitter. |
| bogue | Shell Studio | Correction d’un bogue afin que Livefyre Studio se charge si https:// était explicitement ajouté en préfixe à l’URL. |

