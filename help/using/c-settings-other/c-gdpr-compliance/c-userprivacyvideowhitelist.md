---
description: Vous pouvez mettre en liste blanche votre domaine vidéo à l’aide de .
seo-description: Vous pouvez mettre en liste blanche votre domaine vidéo à l’aide de .
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Si vous utilisez vos propres vidéos et lecteurs personnalisés dans le cadre des vidéos qui s’affichent dans une application de visualisation Livefyre, vous pouvez mettre en liste blanche votre domaine vidéo. La liste blanche de votre domaine vidéo supprime le masque vidéo pour vos vidéos et lecteurs personnalisés.

>[!NOTE]
>
>Utilisez des chemins spécifiques pour vous assurer que seules les vidéos sécurisées sont mises en liste blanche. Si vous placez un chemin d’accès large (par exemple, sampledomain.com), vous pouvez mettre en liste blanche les vidéos non sécurisées.

* Ajouter `userPrivacyVideoWhitelist` après `userPrivacyOptOut`. Vous pouvez ajouter tous les indicateurs de confidentialité de Livefyre simultanément dans le cadre d’un seul objet Livefyre.
* `userPrivacyVideoWhitelist` s’applique uniquement au contenu qui n’est pas incorporé dans les médias sociaux.

Dans l’exemple suivant, les vidéos qui s’affichent dans les applications avec le `sampledomain.com/cdn/videos` chemin d’accès sont mises en liste blanche :

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
