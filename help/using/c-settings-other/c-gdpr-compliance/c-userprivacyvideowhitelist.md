---
description: Vous pouvez placer votre domaine vidéo en liste blanche à l'aide de.
seo-description: Vous pouvez placer votre domaine vidéo en liste blanche à l'aide
  de.
seo-title: Userprivacyvideowhitelist
solution: Experience Manager
title: Userprivacyvideowhitelist
uuid: adfead 18-b 73 b -4 ac 4-97 a 0-d 39 f 528 b 7606
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyvideowhitelist{#userprivacyvideowhitelist}

Si vous utilisez vos propres vidéos et lecteurs personnalisés dans le cadre des vidéos qui s'affichent dans une application de visualisation Livefyre, vous pouvez placer votre domaine vidéo en liste blanche. La liste blanche de votre domaine vidéo supprime le masque vidéo de vos vidéos et lecteurs personnalisés.

>[!NOTE]
>
>Utilisez des chemins spécifiques pour garantir que seules les vidéos qui sont sécurisées sont autorisées. Si vous placez un chemin large (par exemple, sampledomain.com), vous pouvez placer des vidéos en liste blanche.

* Ajoutez `userPrivacyVideoWhitelist` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité Livefyre à la fois dans le cadre d'un objet Livefyre.
* `userPrivacyVideoWhitelist` s'applique uniquement au contenu qui n'est pas incorporé à des médias sociaux.

Dans l'exemple suivant, les vidéos qui s'affichent dans les applications avec `sampledomain.com/cdn/videos` le chemin d'accès sont mises en liste blanche :

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
