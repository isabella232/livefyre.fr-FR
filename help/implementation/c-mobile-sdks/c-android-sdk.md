---
description: Créez des applications Android optimisées par Livefyre.
seo-description: Créez des applications Android optimisées par Livefyre.
seo-title: SDK Android
solution: Experience Manager
title: SDK Android
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK Android{#android-sdk}

Créez des applications Android optimisées par Livefyre.

Utilisez cette bibliothèque pour intégrer les services Livefyre dans votre application Android native. Le SDK [Android](https://github.com/Livefyre/StreamHub-Android-SDK) Livefyre StreamHub fournit une couche mince autour de nos mécanismes d’API communs, en fonction de l’environnement de développement Gradle/Android Studio.

Livefyre fournit également un exemple d’application [Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) , basé sur ce SDK.

Ce SDK Android Livefyre peut être utilisé dans Eclipse et Android Studio.

>[!NOTE]
>
>Avant d’installer le SDK Android Livefyre, vous devez avoir installé le SDK [](https://developer.android.com/sdk/index.html) Android sur votre environnement. Vous devez également inclure quelques packages Android SDK supplémentaires, comme décrit dans la documentation destinée aux développeurs Android &gt; .
>[Ajout de packages SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilisez Android SDK Manager (disponible depuis Android Studio ou la barre d’outils Eclipse) pour installer tous les packages recommandés. Veillez également à inclure le référentiel de support Android.

## Eclipse {#section_dtm_slv_zz}

Pour ajouter le SDK Android Livefyre à votre projet dans Eclipse :

1. Profitez de la dernière version du [SDK](https://github.com/Livefyre/StreamHub-Android-SDK) StreamHub-Android à partir de GitHub.
1. Commencez par un projet existant ou créez-en un nouveau.
1. Pour importer le SDK StreamHub-Android dans votre espace de travail, accédez à **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Recherchez et sélectionnez le SDK StreamHub-Android ; il devrait maintenant apparaître dans l'explorateur de packages.
1. Cliquez avec le bouton droit sur votre projet et sélectionnez **[!UICONTROL Properties,]** ensuite l'onglet Android.
1. Dans la section Bibliothèque, sélectionnez **[!UICONTROL Add button,]** puis StreamHub-Android-SDK dans la liste des bibliothèques.
1. Cliquez sur **[!UICONTROL Apply]** et **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Pour ajouter le SDK Android Livefyre à votre projet dans Android Studio :

1. Profitez de la dernière version du [SDK](https://github.com/Livefyre/StreamHub-Android-SDK) StreamHub-Android à partir de GitHub.
1. Commencez par un projet existant ou créez-en un nouveau.
1. Cliquez avec le bouton droit sur votre projet et sélectionnez **[!UICONTROL Open Module Settings]**.
1. Sélectionnez le **[!UICONTROL +]** bouton dans le coin supérieur gauche de la fenêtre.
1. Sélectionnez **[!UICONTROL Import Existing Project.]** (dans la nouvelle version d'Android studio, vous trouverez **[!UICONTROL Import Existing Project]** sous **[!UICONTROL More Modules]**).

1. Recherchez et sélectionnez le SDK StreamHub-Android.

Android Studio peut vous demander de convertir le SDK en version progressive ; si cela se produit, sélectionnez **[!UICONTROL next]** alors **[!UICONTROL finish]**.

Accédez au dossier **du projet &gt; dossier de l’application &gt; fichier build.gradle** sous dépendances pour ajouter la dépendance suivante :

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Assurez-vous que la ligne suivante se trouve dans le dossier de votre **projet &gt; fichier settings.gradle** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Vous pouvez personnaliser des configurations à partir de Config.java.

## Clients {#section_yfq_blv_zz}

Le SDK Android StreamHub expose plusieurs classes de clients qui peuvent être utilisées pour demander des points de fin d’API Livefyre :

* **AdminClient** Echange un jeton d’authentification utilisateur pour les informations utilisateur, les clés et d’autres métadonnées.

* **BootstrapClient** Obtenez du contenu et des métadonnées récents sur une collection particulière.

* **StreamClient** Sondage d’un flux pour une collection afin de récupérer du contenu nouveau, mis à jour et supprimé.

* **WriteClient** Post, indicateur et contenu similaire dans une collection.

