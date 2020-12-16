---
description: Analyser l’activité des utilisateurs, du contenu et du modérateur de votre site.
seo-description: Analyser l’activité des utilisateurs, du contenu et du modérateur de votre site.
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# Analytics{#analytics}

Analyser l’activité des utilisateurs, du contenu et du modérateur de votre site.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analyser l’activité des utilisateurs, du contenu et du modérateur de votre site.

Livefyre Analytics permet d’accéder à vos données réseau dans des tableaux de bord faciles à lire pour les conversations, la modération et les données utilisateur. Utilisez ces tableaux de bord pour surveiller les activités et exécuter des analyses rapides sur votre ou vos sites.

Les tableaux de bord peuvent être filtrés par site, date et activité. Utilisez la liste déroulante Réseau en haut à gauche de la fenêtre pour sélectionner un site à afficher. Une fois le graphique généré, cliquez sur un en-tête de colonne à trier ou placez le pointeur de la souris sur le graphique pour obtenir des informations plus précises sur un point de données.

Cette page décrit :

* Sélection d&#39;une [plage de dates](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) pour votre tableau de bord
* [Affichage/masquage des Activités disponibles](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [Exportation de données de Tableau de bord](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [Le Tableau de bord Collections](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [Le Tableau de bord de modération](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [Le Tableau de bord Utilisateurs](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics prend actuellement en charge les activités provenant des applications principales Livefyre et de la modération. La plupart des activités incluses dans ces tableaux de bord sont également disponibles par le biais de [Événements JavaScript Livefyre](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/), qui peuvent être utilisés pour alimenter votre propre outil d&#39;analyse personnalisé ou tiers.

## Période {#concept_798C438120E643B6BE262C9997DC87C4}

Cliquez sur la liste déroulante des dates pour sélectionner une plage à afficher. Utilisez les dates rapides ou sélectionnez un début et une date de fin dans les calendriers fournis.

![](assets/analytics-date-range.png)

Dates rapides :

* **Aujourd’hui :** affiche les données à partir de minuit le matin du jour en cours, jusqu’à la dernière heure complète avant ce moment.
* **Hier :** affiche les données des 24 heures précédentes.
* **7 jours :** affiche les données des 7 jours précédents, sauf aujourd’hui.
* **30 jours :** affiche les données des 30 jours précédents, sauf aujourd’hui.
* **Cette semaine :** affiche les données à partir de minuit le matin du dimanche dernier, jusqu’à la dernière heure complète avant ce moment.
* **Ce mois :** affiche les données à partir de minuit le matin du premier jour du mois en cours, jusqu’à la dernière heure complète avant ce moment.
* **Semaine dernière :** affiche les données de la semaine dernière.
* **Mois dernier :** affiche les données du mois dernier.

## Affichage/masquage des Activités {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Les Activités sont des actions que les utilisateurs effectuent sur votre site, y compris la création de commentaires, le marquage, le partage et la modération. Utilisez la liste déroulante **Afficher/Masquer les Activités** pour sélectionner les activités à inclure dans votre tableau de bord.

>[!NOTE]
>
>Si vous sélectionnez de nouveaux événements pour le filtre, la page sera rendue à nouveau sans modifier l’URL.

![](assets/analytics-show-hide-activities.png)

Les activités disponibles varient en fonction du type de tableau de bord et de l&#39;exportation, et peuvent inclure :

* **Publications :** affiche les données à partir de minuit le matin du jour en cours, jusqu’à la dernière heure complète avant ce moment.
* **Réponses :** affiche les données des 24 heures précédentes.
* **Mentions &quot;J’aime&quot; :** affiche les données des 7 jours précédents, sans inclure aujourd’hui.
* **Mentions &quot;Je n’aime pas&quot; :** affiche les données des 30 jours précédents, sauf aujourd’hui.
* **Contient le média :** affiche les données à partir de minuit le matin du dimanche dernier, jusqu’à la dernière heure complète avant ce moment.
* **La publication comporte un téléchargement de photos :** affiche les données à partir de minuit le matin du premier jour du mois en cours, jusqu’à la dernière heure complète avant ce moment.
* **La publication comporte un lien :** affiche les données de la semaine dernière.
* **La publication comporte @mentions :** affiche les données du mois dernier.
* **Approuvé :** affiche les données du mois dernier.
* **Bozo&#39;d :** affiche les données du mois dernier.
* **Blocage :** affiche les données du mois dernier.
* **Total de modération :** affiche les données du mois dernier.

## Exportation de données de Tableau de bord {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Utilisez le menu déroulant **Exporter** pour exporter vos données de tableau de bord au format CSV.

* Résumé quotidien (collections uniquement) : exporte les totaux quotidiens de la dernière semaine complète pour chaque collection.
* Données tabulaires : exporte toutes les données des collections cumulées (toutes les colonnes et toutes les lignes du rapport actuel).
* Données brutes : exporte tous les événements individuels utilisés pour créer le rapport cumulé actuel.

>[!NOTE]
>
>L’exportation de ces rapports peut prendre quelques minutes. Tous les horodatages sont des heures Unix.

## Collections {#concept_228D8E5553784DB8BABF3819A5FF0345}

Le tableau de bord Collections liste l’activité des utilisateurs par collection, ce qui vous permet de déterminer votre contenu le plus (et le moins) attrayant. Chaque collection répertoriée comprend un lien vers la page sur laquelle elle se trouve.

![](assets/analytics-collections.png)

## Modération {#concept_98689B1E804B43CEA21E3F456107CCD9}

Le tableau de bord de modération liste des événements par modérateur, ce qui vous permet d’évaluer leur activité. Utilisez ce rapport pour rechercher les modérateurs les plus principaux et leurs actions de modération les plus courantes.

>[!NOTE]
>
>Les activités de modération automatisées de Livefyre seront répertoriées pour le nom du modérateur Livefyre System.

![](assets/analytics-moderation.png)

## Utilisateurs {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

Le tableau de bord Utilisateurs présente l’activité du site par utilisateur, ce qui vous permet d’analyser comment les utilisateurs interagissent avec votre site. Utilisez ce tableau de bord pour identifier vos utilisateurs les plus principaux sur votre site et pour évaluer les activités les plus populaires du site.

![](assets/analytics-users.png)

