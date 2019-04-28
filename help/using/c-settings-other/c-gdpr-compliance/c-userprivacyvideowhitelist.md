---
description: Vous pouvez placer votre domaine vidéo en liste blanche à l'aide de.
seo-description: Vous pouvez placer votre domaine vidéo en liste blanche à l'aide de.
seo-title: Userprivacyvideowhitelist
solution: Experience Manager
title: Userprivacyvideowhitelist
uuid: adfead 18-b 73 b -4 ac 4-97 a 0-d 39 f 528 b 7606
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacyvideowhitelist{#userprivacyvideowhitelist}

Si vous utilisez vos propres vidéos et lecteurs personnalisés dans le cadre des vidéos qui s&#39;affichent dans une application de visualisation Livefyre, vous pouvez placer votre domaine vidéo en liste blanche. La liste blanche de votre domaine vidéo supprime le masque vidéo de vos vidéos et lecteurs personnalisés.

>[!NOTE]
>
>Utilisez des chemins spécifiques pour garantir que seules les vidéos qui sont sécurisées sont autorisées. Si vous placez un chemin large (par exemple, sampledomain.com), vous pouvez placer des vidéos en liste blanche.

* Ajoutez `userPrivacyVideoWhitelist` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité Livefyre à la fois dans le cadre d&#39;un objet Livefyre.
* `userPrivacyVideoWhitelist` s&#39;applique uniquement au contenu qui n&#39;est pas incorporé à des médias sociaux.

Dans l&#39;exemple suivant, les vidéos qui s&#39;affichent dans les applications avec `sampledomain.com/cdn/videos` le chemin d&#39;accès sont mises en liste blanche :

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
