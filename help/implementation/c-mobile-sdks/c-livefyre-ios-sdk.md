---
description: Ajoutez Livefyre à votre application ios native.
seo-description: Ajoutez Livefyre à votre application ios native.
seo-title: SDK ios Livefyre
solution: Experience Manager
title: SDK ios Livefyre
uuid: bfdef 31 a -49 fc -4 b 25-b 0 c 5-300 f 27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK ios Livefyre{#livefyre-ios-sdk}

Ajoutez Livefyre à votre application ios native.

Utilisez cette bibliothèque Open Source pour intégrer les services Livefyre à votre application ios native. Le SDK Livefyre streamhub ios offre une fine palette autour de nos mécanismes API courants, en fonction de l&#39;excellente bibliothèque afnetworking.

Livefyre fournit également deux exemples d&#39;applications ios basés sur ce SDK : un flux de commentaires et un exemple de module Survey.

## Intégration du SDK dans votre projet en tant que capsule Cocoa (recommandé) {#section_qc5_h3v_zz}

La méthode la plus pratique pour ajouter du SDK streamhub-ios à votre projet consiste à utiliser des cocoapods. Si vous n&#39;avez pas de COCOAPODS, exécutez gem install cocoapods et la configuration de capsule. Voici un exemple de fichier Podfile :

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Vous devez également ajouter un référentiel Specs à votre installation cocoapod (ceci sera clone dans `~/.cocoapods/repos` le répertoire) :

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Une fois votre fichier podfile créé dans la racine du projet d&#39;application et le référentiel ci-dessus ajouté, exécutez :

```
pod install
```

Vous téléchargez toutes les dépendances et créez un fichier myapp. xcworkspace, que vous pourrez utiliser à partir de maintenant pour ouvrir votre projet d&#39;application dans Xcode.

## Sous forme de sous-projet Xcode {#section_jcm_g3v_zz}

Vous pouvez également cloner le référentiel :

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Ensuite, ajoutez le projet Xcode (lfsclient. xcodeproj) à votre application sous forme de sous-projet (simplement en faisant glisser le fichier lfsclient. xcodeproj dans le volet Project Navigator dans Xcode).

Vous devez également faire de même avec l&#39;une des dépendances ([afnetworking](https://github.com/AFNetworking/AFNetworking), [jsonkit](https://github.com/escherba/JSONKit)).

## Télécharger tous les éléments simultanément (non recommandé) {#section_rpb_f3v_zz}

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
>Pour exécuter des tests dans Xcode 6, vous devez ajouter $ (PLATFORM_ DIR)/Developer/Library/Frameworks à FRAMEWORK_ SEARCH_ PATHS dans Pods-test-xctest + ohhttpstubsuitecleanup podhttps://stackoverflow.com/a/24651704[](https://stackoverflow.com/a/24651704).

Vous avez besoin du fichier lfstestconfig. plist de Livefyre, fourni par Livefyre sur demande.

## Documentation Xcode {#section_arl_b3v_zz}

Vous pouvez parcourir la [documentation](https://livefyre.github.com/StreamHub-iOS-SDK/) ou créer la cible « Documentation » dans votre Xcode (nécessite appledoc pour être installé) sur votre système.

## Conditions requises {#section_m5l_13v_zz}

Les versions du SDK ios streamhub étant la version 0.2.0, la version ios 6.0 ou supérieure est requise.

## Annexe (prise en charge JSON) {#section_pcd_5hv_zz}

Pour les utilisateurs qui consultent le SDK streamhub-ios, notez que nous utilisons une version modifiée [de jsonkit](https://github.com/escherba/JSONKit) comme analyseur JSON par défaut (au lieu de nsjsonserialization fourni par Apple). Nous devions le faire car l&#39;analyseur fourni par Apple ne prend pas en charge le décodage de fichiers JSON qui contiennent des nombres entiers ou des nombres à virgule flottante supérieurs à ceux pouvant être représentés par le système. La version modifiée de jsonkit tronque les nombres très élevés au maximum du système correspondant, au lieu de renvoyer une exception.
