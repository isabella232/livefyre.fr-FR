---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Twitter.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Twitter.
seo-title: Règles Twitter
solution: Experience Manager
title: Règles Twitter
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Règles Twitter{#twitter-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Twitter.

Créez des règles Twitter basées sur des hashtags, mots-clés, @mentions ou auteur.

L’ajout **[!UICONTROL Words]** et un **[!UICONTROL Username]** pour votre règle renverront le contenu qui inclut les deux entrées.

>[!NOTE]
>
>Livefyre adhère aux directives d'affichage de Twitter, et les clients sont également responsables de respecter ces directives. Pour plus d’informations, reportez-vous à la documentation de Twitter sur leurs conditions d’ [affichage](https://dev.twitter.com/terms/display-requirements).

Pour créer des règles Twitter afin d’extraire du contenu des flux Twitter dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL Keywords]**
   * Entrez **[!UICONTROL Keywords]** pour être inclus ou exclu de votre flux Twitter. Si vous spécifiez des valeurs pour les champs **[!UICONTROL Contains any of these words]** et **[!UICONTROL Does not contain any of these words]** les champs, les tweets qui contiennent le premier tweet seront renvoyés et ne contiennent pas le second. Vous pouvez entrer plusieurs valeurs pour un seul champ et renvoyer les résultats qui contiennent l’une des valeurs. Pour utiliser l’opérateur booléen ET pour rechercher des tweets contenant deux mots ou plus, utilisez deux esperluettes (*&amp;&amp;*) pour séparer les deux mots.
   * Par exemple, la saisie de **[!UICONTROL Contains any of these words]** mots-clés Giants, Posey et **[!UICONTROL Does not contain any of these words]** Dodger renvoie tous les tweets qui contiennent le mot *Giants* ou *Posey* et ne contiennent pas le mot *Dodger.*
Pour rechercher des tweets qui contiennent à la fois les mots *Giants* et *Posey*, saisissez "Giants &amp;&amp; Posey". Cette fonctionnalité est prise en charge uniquement pour les champs **[!UICONTROL Contains any of these words]** et **[!UICONTROL Does not contain any of these words]** les champs des règles Twitter.

* **[!UICONTROL Hashtags]**.
   * Entrez **[!UICONTROL Hashtags]** pour être inclus ou exclu de votre flux Twitter. Si vous spécifiez des valeurs pour les champs **[!UICONTROL Contains any of these words]** et **[!UICONTROL Does not contain any of these words]** les champs, les tweets qui contiennent des hashtags dans le premier champ seront renvoyés et ne contiennent pas de hashtags dans le deuxième champ. Vous pouvez saisir plusieurs valeurs pour un seul champ. Le flux renvoie des résultats qui contiennent l’une des valeurs.

* **[!UICONTROL Usernames]**
   * Entrez **[!UICONTROL @mentions]** ou **[!UICONTROL authors]** extrayez dans le flux, ou excluez-le du flux. Utilisez les cases à cocher pour définir si les auteurs sélectionnés **[!UICONTROL Retweets]** ou **[!UICONTROL replies]** doivent également être inclus.
   >[!NOTE]
   >
   >Vous pouvez inclure ou exclure des auteurs ; vous ne pouvez pas combiner ces deux champs en une seule règle Twitter.

* **[!UICONTROL Minimum number of followers.]** Sélectionnez le nombre minimum d’abonnés que l’utilisateur doit obligatoirement extraire des informations de ses publications.
* **[!UICONTROL Location]**

   * Entrez l’emplacement (ville, code postal, adresse ou code géographique au format de latitude/longitude commun (+/- 90, +/- 180) ). Commencez à saisir un emplacement pour afficher un menu déroulant contenant des suggestions. Sélectionnez un emplacement dans la liste déroulante. La carte affiche une épingle de cet emplacement. Réglez le curseur pour sélectionner un rayon d'un mille à 25 milles pour chaque emplacement. Si vous ne choisissez pas de rayon, Livefyre choisit automatiquement une valeur par défaut de 12 km.
   >[!NOTE]
   >
   >Pour les deux champs, la distance est calculée à partir du centre de l’emplacement d’entrée.

   * Vous pouvez ajouter plusieurs emplacements et un rayon. Vous pouvez supprimer un emplacement en cliquant sur le X en regard du nom d’un emplacement dans la zone.
   * Combinez les champs **[!UICONTROL Is near this location]** et **[!UICONTROL Is not near this location]** pour extraire le contenu dans les emplacements du **[!UICONTROL Is near this location]** champ, mais pas près des emplacements du **[!UICONTROL Is not near this location]** champ.


* **[!UICONTROL Additional Filters]**
   * Utilisez d’autres filtres pour affiner davantage votre règle Twitter. Indiquez si vous souhaitez :
      * Inclure **[!UICONTROL Replies]** les tweets ciblés (si le flux devient à grande vitesse, cette fonction est automatiquement désactivée.)
      * Inclure les tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Inclure **[!UICONTROL All Content]**, ou **[!UICONTROL Vines Only]**, ou **[!UICONTROL Images Only.]**
      * N’incluez que les tweets qui proviennent de comptes avec les utilisateurs sélectionnés **[!UICONTROL Minimum number of followers]** (n’importe quel, 100, 500, 1 000, 10 000 ou 100 000).

Pour obtenir des options de règle de diffusion en continu supplémentaires pour toutes les règles de diffusion en continu, voir Options de règle de [diffusion en continu pour toutes les règles](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de diffusion en continu.
