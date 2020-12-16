---
description: Vous pouvez placer sur la liste autorisée votre domaine vidéo.
seo-description: Vous pouvez placer sur la liste autorisée votre domaine vidéo.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Si vous utilisez vos propres vidéos et lecteurs personnalisés dans le cadre des vidéos qui s’affichent dans une application de visualisation Livefyre, vous pouvez placer sur la liste autorisée votre domaine vidéo. La Liste autorisée de votre domaine vidéo supprime le masque vidéo pour vos vidéos et lecteurs personnalisés.

>[!NOTE]
>
>Utilisez des chemins spécifiques pour vous assurer que seules les vidéos sécurisées sont placées sur la liste autorisée. Si vous placez un chemin d’accès large (par exemple, sampledomain.com), vous pouvez placer sur la liste autorisée des vidéos non sécurisées.

* Ajoutez `userPrivacyVideoWhitelist` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité de Livefyre en même temps dans le cadre d’un seul objet Livefyre.
* `userPrivacyVideoWhitelist` s’applique uniquement au contenu qui n’est pas incorporé dans les médias sociaux.

Dans l’exemple suivant, les vidéos s’affichant dans les applications avec le chemin d’accès `sampledomain.com/cdn/videos` sont placées sur la liste autorisée :

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
