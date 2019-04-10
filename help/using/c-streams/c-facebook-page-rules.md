---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le
  contenu des pages Facebook.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient
  le contenu des pages Facebook.
seo-title: Règles de page Facebook
solution: Experience Manager
title: Règles de page Facebook
uuid: 2 be 63476-1 a 92-409 d-a 22 f-e 1 ec 66 b 6 dcc 8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Règles de page Facebook{#facebook-page-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu des pages Facebook.

Vous pouvez utiliser des règles de page Facebook pour diffuser du contenu publié publiquement depuis des pages Facebook. Le contenu sera extrait dans l'application ou le dossier à la même fréquence que socialsync, qui change en fonction de la page Facebook et des modèles de trafic. Les liens dans les pages Facebook sont également pris en charge et s'afficheront dans le flux.

Pour créer des règles de page Facebook pour extraire du contenu des pages Facebook dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL Facebook Page]**

   * Saisissez la **[!UICONTROL Name]** page. Saisissez uniquement le texte de fin de l'URL. **Par exemple :** Pour ajouter du contenu, `https://facebook.com/KellysSuperFunFanPage`saisissez *kellyssuperfunfanpage* dans **[!UICONTROL Name]** le champ.

   * Passez en revue **[!UICONTROL Include Facebook Comments for each post]** si vous souhaitez inclure des commentaires utilisateur dans les publications de page.
   * Passez à l **[!UICONTROL Only Show Author Posts]** 'écran si vous souhaitez exclure les publications d'autres utilisateurs.

Pour obtenir des options de règle de diffusion en continu pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion en continu pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre est limité au contenu reçu de Facebook ; il n'est donc pas garanti que chaque publication sur une page Facebook sera incluse dans votre flux.

>[!NOTE]
>
>Si Facebook socialsync et une règle de page Facebook sont tous deux activés pour une page Facebook spécifique et que les commentaires utilisateur sont activés pour la règle de page Facebook, la règle de diffusion en continu remplace socialsync. Le contenu sera diffusé en continu dans l'application en fonction de la règle de traitement des pages Facebook uniquement et non de socialsync.

Les types de contenu pris en charge par le curseur de page Facebook incluent :

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

