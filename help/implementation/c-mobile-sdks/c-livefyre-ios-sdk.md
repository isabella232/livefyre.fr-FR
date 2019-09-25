---
description: Ajoutez Livefyre à votre application iOS native.
seo-description: Ajoutez Livefyre à votre application iOS native.
seo-title: Kit SDK Livefyre iOS
solution: Experience Manager
title: Kit SDK Livefyre iOS
uuid: bfdef31a-49fc-4b25-b0c5-300f27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Kit SDK Livefyre iOS{#livefyre-ios-sdk}

Ajoutez Livefyre à votre application iOS native.

Utilisez cette bibliothèque Open Source pour intégrer les services Livefyre dans votre application iOS native. Le SDK iOS Livefyre StreamHub fournit une couche mince autour de nos mécanismes d’API communs, basée sur l’excellente bibliothèque AFNetworking.

Livefyre fournit également deux exemples d’applications iOS basés sur ce SDK : un flux de commentaires et un exemple d’application Reviews.

## Intégration du SDK dans votre projet en tant que capsule de cacao (recommandé) {#section_qc5_h3v_zz}

Le moyen le plus pratique d’ajouter le SDK StreamHub-iOS à votre projet consiste à utiliser les CocoaPods. Si vous n’avez pas CocoaPods, exécutez gem install cocoapods et pod setup. Voici un exemple de fichier Podfile :

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Vous devez également ajouter un référentiel Specs à votre installation CocoaPod (qui le clone dans `~/.cocoapods/repos` le répertoire) :

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Une fois que votre fichier Podfile a été créé à la racine du projet d’application et que le référentiel ci-dessus a été ajouté, exécutez :

```
pod install
```

Vous téléchargerez toutes les dépendances et créerez un fichier MyApp.xcworkspace, que vous utiliserez désormais pour ouvrir votre projet d’application dans Xcode.

## En tant que sous-projet Xcode {#section_jcm_g3v_zz}

Vous pouvez également cloner le référentiel :

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Ensuite, ajoutez le projet Xcode (LFSClient.xcodeproj) à votre application en tant que sous-projet (il vous suffit de faire glisser le fichier LFSClient.xcodeproj dans le volet Navigateur de projets dans Xcode).

Vous devrez également faire de même avec n’importe quelle dépendance ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

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
>Pour exécuter des tests dans Xcode 6, vous devez ajouter $(PLATFORM_DIR)/Developer/Library/Frameworks à FRAMEWORK_SEARCH_PATHS dans Pods-test-XCTest+OHHTTPSbathSuiteCleanUp[podhttps://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

Vous avez besoin du fichier LFSTestConfig.plist de Livefyre, que Livefyre fournit sur demande.

## Documentation Xcode {#section_arl_b3v_zz}

Vous pouvez parcourir la [documentation](https://livefyre.github.com/StreamHub-iOS-SDK/) ou créer la cible "Documentation" dans votre Xcode (nécessite l’installation d’appledoc) sur votre système.

## Conditions requises {#section_m5l_13v_zz}

Les versions du SDK iOS de StreamHub depuis la version v0.2.0 nécessitent iOS 6.0 ou une version ultérieure.

## Annexe (prise en charge JSON) {#section_pcd_5hv_zz}

Pour ceux qui consultent les versions internes du SDK StreamHub-iOS, notez que nous utilisons une version modifiée de [JSONKit](https://github.com/escherba/JSONKit) comme analyseur JSON par défaut (au lieu de NSJSONSerialization fourni par Apple). Nous avons dû le faire parce que l’analyseur fourni par Apple ne prend pas en charge le décodage des fichiers JSON qui contiennent des entiers ou des nombres à virgule flottante plus grands que ceux qui peuvent être représentés par le système. Notre version modifiée de JSONKit tronque de très grands nombres au maximum du système correspondant, au lieu de lancer une exception.
