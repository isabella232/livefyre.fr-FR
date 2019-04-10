---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le
  contenu depuis Twitter.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient
  le contenu depuis Twitter.
seo-title: Règles Twitter
solution: Experience Manager
title: Règles Twitter
uuid: a 7 fd 2398-fd 6 b -4 c 24-92 b 2-7471176 d 7648
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Règles Twitter{#twitter-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu depuis Twitter.

Créez des règles Twitter basées sur des hashtags, mots-clés, @ mentions ou auteur.

Ajouter **[!UICONTROL Words]** et a **[!UICONTROL Username]** pour votre règle renverra le contenu qui inclut les deux entrées.

>[!NOTE]
>
>Livefyre adhère aux directives d'affichage Twitter et les clients sont chargés de respecter ces directives. Pour plus d'informations, consultez la documentation de Twitter sur les exigences [d'affichage](https://dev.twitter.com/terms/display-requirements).

Pour créer des règles Twitter pour extraire du contenu des flux Twitter vers votre application ou votre dossier, vous pouvez filtrer par :

* **[!UICONTROL Keywords]**
   * Saisissez à **[!UICONTROL Keywords]** inclure ou à exclure de votre flux Twitter. La spécification des valeurs pour les **[!UICONTROL Contains any of these words]****[!UICONTROL Does not contain any of these words]** deux champs renvoie les tweets qui contiennent la première et ne contient pas la seconde. Il est possible de saisir plusieurs valeurs pour un champ unique et renvoie des résultats qui contiennent l'une des valeurs. Pour utiliser l'opérateur booléen ET pour rechercher des tweets avec deux mots ou plus, utilisez deux esperluettes (*& &*) pour séparer les deux mots.
   * Par exemple, la saisie **[!UICONTROL Contains any of these words]** de mots-clés Giants, Posey et **[!UICONTROL Does not contain any of these words]** Dodger renvoie tous les tweets qui incluent le mot *Giants* ou *Posey* et n'incluent pas le mot *Dodger*.
Pour rechercher des tweets qui comprennent les termes *Giants* et *Posey*, saisissez « Giants & & Posey ». Cette fonctionnalité est prise en charge uniquement pour **[!UICONTROL Contains any of these words]** les **[!UICONTROL Does not contain any of these words]** champs et les champs des règles Twitter.

* **[!UICONTROL Hashtags]**.
   * Saisissez à **[!UICONTROL Hashtags]** inclure ou à exclure de votre flux Twitter. La spécification des valeurs pour les **[!UICONTROL Contains any of these words]** deux **[!UICONTROL Does not contain any of these words]** champs renvoie les tweets qui contiennent des hashtags dans le premier champ et ne contient pas de hashtags dans le second champ. Vous pouvez saisir plusieurs valeurs pour un champ unique. Le flux renvoie les résultats qui contiennent l'une des valeurs.

* **[!UICONTROL Usernames]**
   * Entrez **[!UICONTROL @mentions]** ou **[!UICONTROL authors]** appuyez sur le flux ou excluez du flux. Utilisez les cases à cocher pour définir si **[!UICONTROL Retweets]****[!UICONTROL replies]** les auteurs sélectionnés doivent également être inclus.
   >[!NOTE]
   >
   >Vous pouvez inclure ou exclure des auteurs ; vous ne pouvez pas combiner ces deux champs dans une seule règle Twitter.

* **[!UICONTROL Minimum number of followers.]** Sélectionnez le nombre minimum d'abonnés dont l'utilisateur doit extraire les informations à partir de ses publications.
* **[!UICONTROL Location]**

   * Saisissez l'emplacement (ville, zipcode, adresse ou geocode) dans le format de latitude/longitude commun (+/- 90, +/- 180)). Commencez à saisir un emplacement pour afficher un menu déroulant avec des suggestions. Sélectionnez un emplacement dans la liste déroulante. La carte affiche un coin de cet emplacement. Ajustez le curseur pour sélectionner un rayon d'un kilomètre à 25 miles pour chaque emplacement. Si vous ne choisissez pas un rayon, Livefyre sélectionne automatiquement une valeur par défaut de huit miles.
   >[!NOTE]
   >
   >Pour les deux champs, la distance est calculée à partir du centre de l'emplacement d'entrée.

   * Vous pouvez ajouter plusieurs emplacements et rayon. Vous pouvez supprimer un emplacement en cliquant sur le X en regard du nom d'un emplacement dans la zone.
   * Combinez les **[!UICONTROL Is near this location]** champs et **[!UICONTROL Is not near this location]** les champs pour extraire du contenu dans des emplacements dans **[!UICONTROL Is near this location]** le champ, mais pas à proximité des emplacements dans **[!UICONTROL Is not near this location]** le champ.


* **[!UICONTROL Additional Filters]**
   * Utilisez des filtres supplémentaires pour affiner davantage votre règle Twitter. Définissez si vous procédez comme suit :
      * Inclure **[!UICONTROL Replies]** les tweets ciblés (si le flux devient une vitesse élevée, cette fonction est automatiquement désactivée).
      * Inclure les tweets à partir de **[!UICONTROL Verified Twitter accounts only.]**
      * Inclure **[!UICONTROL All Content]**, ou **[!UICONTROL Vines Only]**ou **[!UICONTROL Images Only.]**
      * Incluez uniquement les tweets provenant de comptes dont la valeur est sélectionnée **[!UICONTROL Minimum number of followers]** (n'importe lequel, 100, 500, 1000, 10 000 ou 100 000).

Pour obtenir des options de règle de diffusion en continu pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion en continu pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
