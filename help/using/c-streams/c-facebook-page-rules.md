---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des pages Facebook.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des pages Facebook.
seo-title: Règles de page Facebook
solution: Experience Manager
title: Règles de page Facebook
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Règles de page Facebook{#facebook-page-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des pages Facebook.

Vous pouvez utiliser les règles de page Facebook pour diffuser en continu du contenu publié publiquement à partir des pages Facebook. Le contenu est extrait dans l’application ou le dossier à la même fréquence que SocialSync, ce qui change en fonction des modèles de trafic des publications et des pages Facebook. Les liens des pages Facebook sont également pris en charge et s’afficheront dans le flux.

Pour créer des règles de page Facebook afin d’extraire du contenu des pages Facebook dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL Facebook Page]**

   * Saisissez **[!UICONTROL Name]** pour la page. Entrez uniquement le texte de fin de l’URL. **Par exemple :** Pour ajouter du contenu à partir de  `https://facebook.com/KellysSuperFunFanPage`, saisissez  ** KellysSuperFunFanPagedans le  **[!UICONTROL Name]** champ.

   * Activez **[!UICONTROL Include Facebook Comments for each post]** si vous souhaitez inclure des commentaires d’utilisateur dans les publications de page.
   * Activez **[!UICONTROL Only Show Author Posts]** si vous souhaitez exclure des publications d’autres utilisateurs.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre est limité au contenu reçu de Facebook, et n&#39;est donc pas en mesure de garantir que chaque publication d&#39;une page Facebook sera incluse dans votre flux.

>[!NOTE]
>
>Si Facebook SocialSync et une règle de page Facebook sont tous deux activés pour une page Facebook spécifique et que les commentaires des utilisateurs sont activés pour la règle de page Facebook, la règle de diffusion en continu remplace SocialSync. Le contenu sera diffusé en continu dans l’application en fonction de la règle de traitement des pages Facebook uniquement, sans utiliser SocialSync.

Les types de contenu pris en charge par le traitement des pages Facebook sont les suivants :

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

