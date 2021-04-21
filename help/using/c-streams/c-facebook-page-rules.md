---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des pages Facebook.
title: Règles de page facebook
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Règles de page facebook{#facebook-page-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des pages Facebook.

Vous pouvez utiliser les règles de page Facebook pour diffuser en continu du contenu publié publiquement à partir des pages Facebook. Le contenu est extrait dans l’application ou le dossier à la même fréquence que SocialSync, ce qui change en fonction des modèles de trafic Facebook Page et Post. Les liens dans les pages Facebook sont également pris en charge et s’afficheront dans le flux.

Pour créer des règles de page Facebook afin d’extraire du contenu des pages Facebook dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL Facebook Page]**

   * Saisissez **[!UICONTROL Name]** pour la page. Entrez uniquement le texte de fin de l’URL. **Par exemple :** Pour ajouter du contenu à partir de  `https://facebook.com/KellysSuperFunFanPage`, saisissez  ** KellysSuperFunFanPagedans le  **[!UICONTROL Name]** champ.

   * Activez **[!UICONTROL Include Facebook Comments for each post]** si vous souhaitez inclure des commentaires d’utilisateur dans les publications de page.
   * Activez **[!UICONTROL Only Show Author Posts]** si vous souhaitez exclure des publications d’autres utilisateurs.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre est limité au contenu reçu de Facebook, et n’est donc pas en mesure de garantir que chaque publication d’une page Facebook sera incluse dans votre flux.

>[!NOTE]
>
>Si Facebook SocialSync et une règle de page Facebook sont tous deux activés pour une page Facebook spécifique et que les commentaires d’utilisateur sont activés pour la règle de page Facebook, la règle de flux remplace SocialSync. Le contenu sera diffusé en continu dans l’application en fonction de la règle de traitement des pages de Facebook uniquement, sans utiliser SocialSync.

Les types de contenu pris en charge par Facebook Page Curate sont les suivants :

* Propriétaire ou administrateur de la page

   * État
   * Photos
   * Vidéos sous forme de liens

* Utilisateur Facebook standard

   * État
   * Photos
   * Vidéos sous forme de liens

* Tiers

   * État
