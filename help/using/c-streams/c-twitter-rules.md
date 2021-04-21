---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Twitter.
title: Règles de twitter
exl-id: 3a5081eb-048d-4dcf-80a2-366af2cb2c86
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Règles twitter{#twitter-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu de Twitter.

Créez des règles Twitter basées sur des hashtags, mots-clés, @mentions ou auteur.

Si vous Ajoutez **[!UICONTROL Words]** et **[!UICONTROL Username]** pour votre règle, le contenu qui inclut les deux entrées sera renvoyé.

>[!NOTE]
>
>Livefyre respecte les directives d&#39;affichage de Twitter et les clients sont également tenus de les respecter. Pour plus d’informations, consultez la documentation de Twitter sur leurs [exigences d’affichage](https://dev.twitter.com/terms/display-requirements).

Pour créer des règles Twitter afin d’extraire du contenu des flux Twitter dans votre application ou dossier, vous pouvez filtrer par :

* **[!UICONTROL Keywords]**
   * Saisissez **[!UICONTROL Keywords]** à inclure ou à exclure de votre flux Twitter. Si vous spécifiez des valeurs à la fois pour les champs **[!UICONTROL Contains any of these words]** et **[!UICONTROL Does not contain any of these words]**, les tweets qui contiennent le premier et ne contiennent pas le second seront renvoyés. Vous pouvez entrer plusieurs valeurs pour un seul champ et renvoyer les résultats qui contiennent toutes les valeurs. Pour utiliser l’opérateur booléen ET pour rechercher des tweets contenant au moins deux mots, utilisez deux esperluettes (*&amp;*) pour séparer les deux mots.
   * Par exemple, la saisie de **[!UICONTROL Contains any of these words]** mots-clés Giants, Posey et **[!UICONTROL Does not contain any of these words]** mot-clé Dodger renvoie tous les tweets qui contiennent le mot *Giants* ou *Posey* et n’incluent pas le mot *Dodger*.
Pour rechercher des tweets qui contiennent à la fois les mots *Giants* et *Posey*, saisissez &quot;Giants &amp;&amp; Posey&quot;. Cette fonction est prise en charge uniquement pour les champs **[!UICONTROL Contains any of these words]** et **[!UICONTROL Does not contain any of these words]** des règles Twitter.

* **[!UICONTROL Hashtags]**.
   * Saisissez **[!UICONTROL Hashtags]** à inclure ou à exclure de votre flux Twitter. Si vous spécifiez des valeurs pour les champs **[!UICONTROL Contains any of these words]** et **[!UICONTROL Does not contain any of these words]**, les tweets qui contiennent des hashtags dans le premier champ seront renvoyés et ne contiennent pas de hashtags dans le second champ. Vous pouvez saisir plusieurs valeurs pour un seul champ. Le flux renvoie des résultats qui contiennent toutes les valeurs.

* **[!UICONTROL Usernames]**
   * Saisissez **[!UICONTROL @mentions]** ou **[!UICONTROL authors]** pour extraire dans le flux ou exclure du flux. Utilisez les cases à cocher pour définir si **[!UICONTROL Retweets]** ou **[!UICONTROL replies]** des auteurs sélectionnés doivent également être inclus.

   >[!NOTE]
   >
   >Vous pouvez inclure ou exclure des auteurs ; vous ne pouvez pas combiner ces deux champs en une seule règle Twitter.

* **[!UICONTROL Minimum number of followers.]** Sélectionnez le nombre d&#39;abonnés minimum dont l’utilisateur doit disposer pour extraire les informations de ses publications.
* **[!UICONTROL Location]**

   * Entrez l’emplacement (ville, code postal, adresse ou code géographique au format de latitude/longitude commun (+/- 90, +/- 180) ). Commencez à saisir un emplacement pour afficher un menu déroulant contenant des suggestions. Sélectionnez un emplacement dans la liste déroulante. La carte affiche une épingle de cet emplacement. Réglez le curseur pour sélectionner un rayon d&#39;un mille à 25 miles pour chaque emplacement. Si vous ne choisissez pas de rayon, Livefyre choisit automatiquement un rayon de 12 km par défaut.
   >[!NOTE]
   >
   >Pour les deux champs, la distance est calculée à partir du centre de l’emplacement d’entrée.

   * Vous pouvez ajouter plusieurs emplacements et rayon. Vous pouvez supprimer un emplacement en cliquant sur le X en regard du nom d’un emplacement dans la zone.
   * Combinez les champs **[!UICONTROL Is near this location]** et **[!UICONTROL Is not near this location]** pour extraire le contenu dans les emplacements du champ **[!UICONTROL Is near this location]**, mais pas près des emplacements du champ **[!UICONTROL Is not near this location]**.


* **[!UICONTROL Additional Filters]**
   * Utilisez des Filtres supplémentaires pour affiner davantage votre règle Twitter. Indiquez si vous souhaitez :
      * Insérez **[!UICONTROL Replies]** dans les tweets ciblés (si le flux devient à grande vitesse, cette fonction est automatiquement désactivée.)
      * Inclure les tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Inclure **[!UICONTROL All Content]**, ou **[!UICONTROL Vines Only]** ou **[!UICONTROL Images Only.]**
      * Inclure uniquement les tweets qui proviennent de comptes avec le **[!UICONTROL Minimum number of followers]** sélectionné (n°, 100, 500, 1000, 10 000 ou 100 000).

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
