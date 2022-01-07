---
description: Analysez l’activité des utilisateurs, du contenu et du modérateur de votre site.
title: Analytics
exl-id: dc0545ec-2294-44ab-87c4-67eb30c3f787
source-git-commit: 9cd6617c4204b2c09787ea294227f640018928ce
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 1%

---

# Analytics{#analytics}

Analysez l’activité des utilisateurs, du contenu et du modérateur de votre site.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analysez l’activité des utilisateurs, du contenu et du modérateur de votre site.

Livefyre Analytics permet d’accéder à vos données réseau dans des tableaux de bord faciles à lire pour les données de conversation, de modération et d’utilisateur. Utilisez ces tableaux de bord pour surveiller l’activité et exécuter des analyses rapides sur votre ou vos sites.

Les tableaux de bord peuvent être filtrés par site, date et activité. Utilisez la liste déroulante Réseau en haut à gauche de la fenêtre pour sélectionner un site à afficher. Une fois généré, cliquez sur l’en-tête d’une colonne à trier ou placez le pointeur de la souris sur le graphique pour obtenir des informations plus spécifiques sur n’importe quel point de données.

Cette page décrit :

* Sélection d’une plage de dates pour votre tableau de bord
* Affichage/masquage des activités disponibles
* Exportation des données d’un tableau de bord
* Tableau de bord des collections
* Tableau de bord de modération
* Tableau de bord Utilisateurs

>[!NOTE]
>
>Analytics prend actuellement en charge les activités provenant des applications principales et de la modération Livefyre. La plupart des activités incluses dans ces tableaux de bord sont également disponibles par le biais des événements JavaScript Livefyre, qui peuvent être utilisés pour alimenter votre propre outil d’analyse personnalisé ou tiers.

## Période {#concept_798C438120E643B6BE262C9997DC87C4}

Cliquez sur le menu déroulant des dates pour sélectionner une plage à afficher. Utilisez les dates rapides ou sélectionnez une date de début et de fin dans les calendriers proposés.

![](assets/analytics-date-range.png)

Dates rapides :

* **Aujourd&#39;hui :** Affiche les données à partir de minuit le matin du jour en cours, jusqu’à la dernière heure complète avant ce moment.
* **Hier :** Affiche les données des 24 heures précédentes.
* **7 jours :** Affiche les données des 7 jours précédents, à l’exception d’aujourd’hui.
* **30 jours :** Affiche les données des 30 jours précédents, à l’exception d’aujourd’hui.
* **Cette semaine :** Affiche les données à partir de minuit le matin du dimanche dernier, jusqu’à la dernière heure complète avant ce moment.
* **Ce mois-ci :** Affiche les données à partir de minuit le matin du premier jour du mois en cours, jusqu’à la dernière heure de fin avant ce moment.
* **Semaine dernière :** Affiche les données de la semaine dernière.
* **Mois dernier :** Affiche les données du mois dernier.

## Affichage/masquage des activités {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Les activités sont des actions que les utilisateurs effectuent sur votre site, notamment pour commenter, marquer, partager et modérer. Utilisez la variable **Afficher/masquer les activités** Menu déroulant pour sélectionner les activités que vous souhaitez inclure dans votre tableau de bord.

>[!NOTE]
>
>La sélection de nouveaux événements pour le filtre entraîne le rendu de la page sans modifier l’URL.

![](assets/analytics-show-hide-activities.png)

Les activités disponibles varient en fonction du type et de l’exportation d’un tableau de bord et peuvent inclure :

* **Publications :** Affiche les données à partir de minuit le matin du jour en cours, jusqu’à la dernière heure complète avant ce moment.
* **Réponses :** Affiche les données des 24 heures précédentes.
* **Mentions J’aime :** Affiche les données des 7 jours précédents, à l’exception d’aujourd’hui.
* **N’aime pas :** Affiche les données des 30 jours précédents, à l’exception d’aujourd’hui.
* **Contient le média :** Affiche les données à partir de minuit le matin du dimanche dernier, jusqu’à la dernière heure complète avant ce moment.
* **Le billet a été téléchargé avec photo :** Affiche les données à partir de minuit le matin du premier jour du mois en cours, jusqu’à la dernière heure de fin avant ce moment.
* **La publication comporte un lien :** Affiche les données de la semaine dernière.
* **Le billet a @mentions :** Affiche les données du mois dernier.
* **Approuvé :** Affiche les données du mois dernier.
* **Bozo&#39;d :** Affiche les données du mois dernier.
* **Blocage :** Affiche les données du mois dernier.
* **Total de la modération :** Affiche les données du mois dernier.

## Exportation des données d’un tableau de bord {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Utilisez la variable **Exporter** menu déroulant pour exporter les données de votre tableau de bord au format CSV.

* Résumé quotidien (collections uniquement) : exporte les bilans quotidiens de la dernière semaine complète pour chaque collection.
* Données du tableau : exporte toutes les données de collections cumulées (toutes les colonnes et toutes les lignes du rapport actif).
* Données brutes : exporte tous les événements individuels utilisés pour créer le rapport cumulé actuel.

>[!NOTE]
>
>L’exportation de ces rapports peut prendre quelques minutes. Tous les horodatages sont des heures Unix.

## Collections {#concept_228D8E5553784DB8BABF3819A5FF0345}

Le tableau de bord Collections répertorie l’activité des utilisateurs par collection, ce qui vous permet de déterminer votre contenu le plus (et le moins) engageant. Chaque collection répertoriée comprend un lien vers la page sur laquelle elle se trouve.

![](assets/analytics-collections.png)

## Modération {#concept_98689B1E804B43CEA21E3F456107CCD9}

Le tableau de bord Modération répertorie les événements par modérateur, ce qui vous permet d’évaluer leur activité. Utilisez ce rapport pour trouver les modérateurs les plus principaux et leurs actions de modération les plus courantes.

>[!NOTE]
>
>Les activités de modération automatisée Livefyre sont répertoriées pour le nom du modérateur Livefyre System.

![](assets/analytics-moderation.png)

## Utilisateurs {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

Le tableau de bord Utilisateurs présente l’activité du site par utilisateur, ce qui vous permet d’analyser la manière dont les utilisateurs individuels interagissent avec votre site. Utilisez ce tableau de bord pour trouver vos utilisateurs les plus principaux sur votre site et pour évaluer les activités de site les plus populaires.

![](assets/analytics-users.png)
