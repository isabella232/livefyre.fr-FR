---
description: Ajoutez Livefyre à votre application iOS native.
title: SDK iOS Livefyre
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# SDK iOS Livefyre{#livefyre-ios-sdk}

Ajoutez Livefyre à votre application iOS native.

Utilisez cette bibliothèque Open Source pour intégrer les services Livefyre à votre application iOS native. Le SDK iOS Livefyre StreamHub fournit une fine couche autour de nos mécanismes d’API communs, basés sur l’excellente bibliothèque AFNetworking.

Livefyre fournit également deux exemples d’applications iOS basés sur ce SDK : un flux de commentaires et un exemple d’application Révisions .

## Intégration du SDK dans votre projet as a Cocoa Pod (recommandé) {#section_qc5_h3v_zz}

La méthode la plus pratique pour ajouter le SDK StreamHub-iOS à votre projet consiste à utiliser CocoaPods. Si vous ne disposez pas de CocoaPods, exécutez gem install cocoapods et pod setup. Voici un exemple de fichier Podfile :

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Vous devez également ajouter un référentiel Specs à votre installation CocoaPod (il sera cloné dans le répertoire `~/.cocoapods/repos`) :

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Une fois votre fichier de capsule créé à la racine du projet de votre application et le référentiel ajouté ci-dessus, exécutez :

```
pod install
```

Cela téléchargera toutes les dépendances et créera un fichier MyApp.xcworkspace, que vous utiliserez désormais pour ouvrir votre projet d’application dans Xcode.

## En tant que sous-projet Xcode {#section_jcm_g3v_zz}

Vous pouvez également cloner le référentiel :

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Ajoutez ensuite le projet Xcode (LFSClient.xcodeproj) à votre application en tant que sous-projet (facilement réalisable en faisant simplement glisser le fichier LFSClient.xcodeproj dans le volet Navigateur du projet dans Xcode).

Vous devez également faire de même avec toutes les dépendances ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Télécharger tout en même temps (non recommandé) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>Pour exécuter des tests dans Xcode 6, vous devez ajouter $(PLATFORM_DIR)/Developer/Library/Frameworks à FRAMEWORK_SEARCH_PATHS dans Pods-test-XCTest+OHHTTPSbathSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

Vous avez besoin du fichier LFSTestConfig.plist de Livefyre, que Livefyre vous fournit sur demande.

## Documentation Xcode {#section_arl_b3v_zz}

Vous pouvez parcourir la [documentation](https://github.com/Livefyre/StreamHub-iOS-SDK) ou créer la cible &quot;Documentation&quot; dans votre Xcode (nécessite l’installation d’appledoc) sur votre système.

## Conditions {#section_m5l_13v_zz}

Les versions du SDK iOS StreamHub depuis la version v0.2.0 requièrent iOS 6.0 ou une version ultérieure.

## Annexe (prise en charge JSON) {#section_pcd_5hv_zz}

Pour ceux qui consultent les versions internes du SDK StreamHub-iOS, notez que nous utilisons une version modifiée de [JSONKit](https://github.com/escherba/JSONKit) comme analyseur JSON par défaut (au lieu de NSJSONSerialization fourni par Apple). Nous avons dû le faire car l’analyseur fourni par Apple ne prend pas en charge le décodage de fichiers JSON contenant des entiers ou des nombres à virgule flottante plus grands que ceux pouvant être représentés par le système. Notre version modifiée de JSONKit tronque de très grands nombres au maximum du système correspondant, au lieu de lancer une exception.
