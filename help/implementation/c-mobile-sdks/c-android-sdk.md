---
description: Création d'applications Android optimisées par Livefyre.
seo-description: Création d'applications Android optimisées par Livefyre.
seo-title: SDK Android
solution: Experience Manager
title: SDK Android
uuid: 68793 fa 9-3 ea 1-4890-b 36 d-b 631 f 1 c 6 f 7 de
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# SDK Android{#android-sdk}

Création d'applications Android optimisées par Livefyre.

Utilisez cette bibliothèque pour intégrer les services Livefyre à votre application Android native. Le SDK [Livefyre streamhub Android](https://github.com/Livefyre/StreamHub-Android-SDK) offre une fine palette autour de nos mécanismes API courants, reposant sur l'environnement de développement Gradle/Android Studio.

Livefyre fournit également un [exemple de module Survey](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) , basé sur ce SDK.

Ce SDK Andefyre Android peut être utilisé dans Eclipse et Android Studio.

>[!NOTE]
>
>Avant d'installer le SDK Andefyre Android, [vous devez installer le SDK](https://developer.android.com/sdk/index.html) Android sur votre environnement. Vous devez également inclure quelques packages SDK Android supplémentaires, comme décrit dans la documentation des développeurs Android >.
>[Ajout de packages SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilisez le Gestionnaire SDK Android (disponible sur la barre d'outils Android Studio ou Eclipse) pour installer tous les packages recommandés. Veillez à inclure également le référentiel d'assistance Android.

## Eclipse {#section_dtm_slv_zz}

Pour ajouter le SDK Andefyre à votre projet dans Eclipse :

1. Bénéficiez de la dernière [version streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) de github.
1. Commencez par un projet existant ou créez-en un nouveau.
1. Pour importer le SDK streamhub-Android-SDK dans votre espace de travail, accédez **[!UICONTROL File > Import > General > Existing Project into Workspace]**à.
1. Recherchez et sélectionnez streamhub-Android-SDK ; il doit maintenant apparaître dans l'explorateur de packages.
1. Droite : cliquez sur votre projet et sélectionnez **[!UICONTROL Properties,]** l'onglet Android.
1. Dans la section Bibliothèque, sélectionnez **[!UICONTROL Add button,]** ensuite streamhub-Android-SDK dans la liste des bibliothèques.
1. Cliquez **[!UICONTROL Apply]** sur et **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Pour ajouter le SDK Andefyre Android à votre projet dans Android Studio :

1. Bénéficiez de la dernière [version streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) de github.
1. Commencez par un projet existant ou créez-en un nouveau.
1. Droite : cliquez sur votre projet et sélectionnez **[!UICONTROL Open Module Settings]**.
1. Sélectionnez **[!UICONTROL +]** le bouton dans le coin supérieur gauche de la fenêtre.
1. Sélectionner **[!UICONTROL Import Existing Project.]** (dans la nouvelle version du studio Android, vous pouvez trouver **[!UICONTROL Import Existing Project]** sous **[!UICONTROL More Modules]**.)

1. Recherchez et sélectionnez streamhub-Android-SDK.

Android Studio peut demander que vous convertissiez le SDK en version de dégradé ; Si cela se produit, sélectionnez **[!UICONTROL next]** ensuite **[!UICONTROL finish]**.

Accédez au **dossier du projet > dossier de l'application > build. gradle** sous dépendances pour ajouter la dépendance suivante :

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Assurez-vous que la ligne suivante se trouve dans le dossier **du projet > settings. gradle** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Vous pouvez personnaliser les configurations à partir de Config. java.

## Clients {#section_yfq_blv_zz}

Le SDK streamhub Android expose plusieurs classes de clients qui peuvent être utilisées pour demander des endpoints de fin API Livefyre :

* **Adminclient** Échangez un jeton d'authentification utilisateur pour les informations de l'utilisateur, les clés et d'autres métadonnées.

* **Bootstrapclient** Obtenir le contenu récent et les métadonnées concernant une collection particulière.

* **Streamclient** Sondage d'un flux pour une collection pour récupérer du contenu nouveau, mis à jour et supprimé.

* **Writeclient** Publication, indicateur et contenu J'aime dans une collection.

