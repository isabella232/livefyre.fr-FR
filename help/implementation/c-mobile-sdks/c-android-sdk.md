---
description: Création d'applications Android optimisées par Livefyre.
seo-description: Création d'applications Android optimisées par Livefyre.
seo-title: SDK Android
solution: Experience Manager
title: SDK Android
uuid: 68793 fa 9-3 ea 1-4890-b 36 d-b 631 f 1 c 6 f 7 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK Android{#android-sdk}

Création d&#39;applications Android optimisées par Livefyre.

Utilisez cette bibliothèque pour intégrer les services Livefyre à votre application Android native. Le SDK [Livefyre streamhub Android](https://github.com/Livefyre/StreamHub-Android-SDK) offre une fine palette autour de nos mécanismes API courants, reposant sur l&#39;environnement de développement Gradle/Android Studio.

Livefyre fournit également un [exemple de module Survey](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) , basé sur ce SDK.

Ce SDK Andefyre Android peut être utilisé dans Eclipse et Android Studio.

>[!NOTE]
>
>Avant d&#39;installer le SDK Andefyre Android, [vous devez installer le SDK](https://developer.android.com/sdk/index.html) Android sur votre environnement. Vous devez également inclure quelques packages SDK Android supplémentaires, comme décrit dans la documentation des développeurs Android &gt;.
>[Ajout de packages SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilisez le Gestionnaire SDK Android (disponible sur la barre d&#39;outils Android Studio ou Eclipse) pour installer tous les packages recommandés. Veillez à inclure également le référentiel d&#39;assistance Android.

## Eclipse {#section_dtm_slv_zz}

Pour ajouter le SDK Andefyre à votre projet dans Eclipse :

1. Bénéficiez de la dernière [version streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) de github.
1. Commencez par un projet existant ou créez-en un nouveau.
1. Pour importer le SDK streamhub-Android-SDK dans votre espace de travail, accédez **[!UICONTROL File > Import > General > Existing Project into Workspace]**à.
1. Recherchez et sélectionnez streamhub-Android-SDK ; il doit maintenant apparaître dans l&#39;explorateur de packages.
1. Droite : cliquez sur votre projet et sélectionnez **[!UICONTROL Properties,]** l&#39;onglet Android.
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

Accédez au **dossier du projet &gt; dossier de l&#39;application &gt; build. gradle** sous dépendances pour ajouter la dépendance suivante :

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Assurez-vous que la ligne suivante se trouve dans le dossier **du projet &gt; settings. gradle** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Vous pouvez personnaliser les configurations à partir de Config. java.

## Clients {#section_yfq_blv_zz}

Le SDK streamhub Android expose plusieurs classes de clients qui peuvent être utilisées pour demander des endpoints de fin API Livefyre :

* **Adminclient** Échangez un jeton d&#39;authentification utilisateur pour les informations de l&#39;utilisateur, les clés et d&#39;autres métadonnées.

* **Bootstrapclient** Obtenir le contenu récent et les métadonnées concernant une collection particulière.

* **Streamclient** Sondage d&#39;un flux pour une collection pour récupérer du contenu nouveau, mis à jour et supprimé.

* **Writeclient** Publication, indicateur et contenu J&#39;aime dans une collection.

