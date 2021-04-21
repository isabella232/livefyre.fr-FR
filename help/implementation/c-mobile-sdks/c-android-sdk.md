---
description: Créez des applications Android pilotées par Livefyre.
title: SDK Android
exl-id: 54ea6537-5f27-4174-af25-d17257f23e48
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# SDK Android{#android-sdk}

Créez des applications Android pilotées par Livefyre.

Utilisez cette bibliothèque pour intégrer les services Livefyre à votre application Android native. Le [SDK Android Livefyre StreamHub](https://github.com/Livefyre/StreamHub-Android-SDK) fournit une couche mince autour de nos mécanismes d’API communs, basée sur l’environnement de développement Gradle/Android Studio.

Livefyre fournit également un exemple d’application [Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App), basé sur ce SDK.

Ce SDK Android Livefyre peut être utilisé dans Eclipse et Android Studio.

>[!NOTE]
>
>Avant d’installer le SDK Android Livefyre, vous devez avoir installé le [SDK Android](https://developer.android.com/sdk/index.html) sur votre environnement. Vous devez également inclure quelques packages SDK Android supplémentaires, comme décrit dans la documentation destinée aux développeurs Android > .
>[Ajouter des packages SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilisez Android SDK Manager (disponible depuis Android Studio ou la barre d’outils Eclipse) pour installer tous les packages recommandés. Veillez également à inclure le référentiel de support Android.

## Eclipse {#section_dtm_slv_zz}

Pour ajouter le SDK Android Livefyre à votre projet dans Eclipse :

1. Bénéficiez de la toute dernière version de [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) à partir de GitHub.
1. Début avec un projet existant ou en créer un nouveau.
1. Pour importer le SDK StreamHub-Android dans votre espace de travail, accédez à **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Recherchez et sélectionnez StreamHub-Android-SDK ; il devrait maintenant s&#39;afficher dans l&#39;explorateur de paquets.
1. Cliquez avec le bouton droit sur votre projet et sélectionnez **[!UICONTROL Properties,]** puis l&#39;onglet Android.
1. Dans la section Bibliothèque, sélectionnez **[!UICONTROL Add button,]**, puis StreamHub-Android-SDK dans la liste des bibliothèques.
1. Cliquez sur **[!UICONTROL Apply]** et **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Pour ajouter le SDK Android Livefyre à votre projet dans Android Studio :

1. Bénéficiez de la toute dernière version de [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) à partir de GitHub.
1. Début avec un projet existant ou en créer un nouveau.
1. Cliquez avec le bouton droit sur votre projet et sélectionnez **[!UICONTROL Open Module Settings]**.
1. Sélectionnez le bouton **[!UICONTROL +]** dans le coin supérieur gauche de la fenêtre.
1. Sélectionnez **[!UICONTROL Import Existing Project.]** (dans la nouvelle version d&#39;Android studio, vous trouverez **[!UICONTROL Import Existing Project]** sous **[!UICONTROL More Modules]**.)

1. Recherchez et sélectionnez StreamHub-Android-SDK.

Android Studio peut demander que vous convertissiez le SDK en version progressive ; si cela se produit, sélectionnez **[!UICONTROL next]** puis **[!UICONTROL finish]**.

Accédez au **dossier du projet > dossier de l’application > fichier build.gradle** sous dépendances pour ajouter la dépendance suivante :

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Assurez-vous que la ligne suivante se trouve dans votre dossier de projet **settings.gradle** fichier :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Vous pouvez personnaliser des configurations à partir de Config.java.

## Clients {#section_yfq_blv_zz}

Le SDK Android StreamHub expose plusieurs classes de clients qui peuvent être utilisées pour demander des points de terminaison de l’API Livefyre :

* **** AdminClientExchange un jeton d’authentification utilisateur pour les informations utilisateur, les clés et d’autres métadonnées.

* **** BootstrapClientObtenez du contenu et des métadonnées récents sur une collection particulière.

* **** StreamClientSondage un flux pour une collection afin de récupérer du contenu nouveau, mis à jour et supprimé.

* **** WriteClientPost, marquer et aimer le contenu d’une collection.
