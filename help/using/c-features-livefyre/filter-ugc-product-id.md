---
description: Filtrage d'UGC par - l'ID du produit permet d'incorporer exactement la
  même application sur plusieurs pages tout en affichant différents UGC spécifiques
  au produit pour chaque page.
seo-description: Filtrage d'UGC par - l'ID du produit permet d'incorporer exactement
  la même application sur plusieurs pages tout en affichant différents UGC spécifiques
  au produit pour chaque page.
seo-title: Filtrage UGC par - ID du produit
title: Filtrage UGC par - ID du produit
uuid: 98108 ddb -5710-4331-891 b -7 e 1 bbb 106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816

---


# Filtrage UGC par - ID du produit {#filter-ugc-product-id}

Filtrage d'UGC par - l'ID du produit permet d'incorporer exactement la même application sur plusieurs pages tout en affichant différents UGC spécifiques au produit pour chaque page.

Pour filtrer UGC par ID de produit, procédez comme suit :

1. Dans Livefyre Studio, accédez à **[!UICONTROL Apps]** l'onglet.

1. Sélectionnez l'application que vous souhaitez modifier.

1. Sélectionnez l'onglet Designer dans le rail de gauche.

1. Activez **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Sélectionnez les dossiers de produit de niveau supérieur qui contiennent le ou les produits dont vous souhaitez filtrer le contenu UGC.
Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers.

1. Désactiver **[!UICONTROL Show related content]**.
Lorsqu'elle est activée, le contenu filtré à l'aide de `data-lf-attr-product` l'attribut s'affiche d'abord, suivi de tout autre contenu de l'application.

1. Cliquez **[!UICONTROL Publish]**sur.

1. Insérez les ID du produit que vous souhaitez filtrer dans le code cible.

>[!NOTE]
>
>Pour localiser des ID de produit, accédez **[!UICONTROL Settings > Products]**à. Localisez le produit souhaité et sélectionnez-le et l'ID s'affiche.

Par exemple, le code suivant est généré pour une application Media Wall :

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

Pour baliser un produit, remplacez `<product 1>` -le `data-lf-attr-product` par l'identifiant de produit souhaité. Vous pouvez baliser un ou plusieurs produits en ajoutant des ID de produit séparés par des virgules. Les produits doivent être contenus dans le dossier ou les dossiers de produit de niveau supérieur sélectionnés à l'étape 5.

Le segment de code modifié apparaîtra comme suit :

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

L'application affiche désormais uniquement les ID de produit balisés.