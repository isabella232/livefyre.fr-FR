---
description: Le filtrage UGC par ID de produit vous permet d’incorporer exactement la même application sur plusieurs pages tout en affichant un UGC spécifique à chaque page.
seo-description: Le filtrage UGC par ID de produit vous permet d’incorporer exactement la même application sur plusieurs pages tout en affichant un UGC spécifique à chaque page.
seo-title: Filtrage de l’UGC par ID de produit
title: Filtrage de l’UGC par ID de produit
uuid: 98108ddb-5710-4331-891b-7e1bb106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816

---


# Filtrage de l’UGC par ID de produit {#filter-ugc-product-id}

Le filtrage UGC par ID de produit vous permet d’incorporer exactement la même application sur plusieurs pages tout en affichant un UGC spécifique à chaque page.

Pour filtrer l’UGC par ID de produit, procédez comme suit :

1. Dans Livefyre Studio, accédez à l’ **[!UICONTROL Apps]** onglet.

1. Sélectionnez l’application à modifier.

1. Sélectionnez l’onglet Designer dans le rail de gauche.

1. Enable **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Sélectionnez les dossiers de produit de niveau supérieur qui contiennent le ou les produits dont vous souhaitez filtrer le contenu généré par l’utilisateur.
Utilisez Ctrl/Commande + clic pour sélectionner plusieurs dossiers.

1. Disable **[!UICONTROL Show related content]**.
Lorsqu’il est activé, le contenu filtré à l’aide de l’ `data-lf-attr-product` attribut s’affiche en premier, suivi de tous les autres contenus de l’application.

1. Cliquez sur **[!UICONTROL Publish]**.

1. Insérez les ID de produit par lesquels vous souhaitez filtrer dans le code cible.

>[!NOTE]
>
>Pour localiser les ID de produit, accédez à **[!UICONTROL Settings > Products]**. Localisez le produit souhaité, sélectionnez-le et l’ID s’affiche.

Par exemple, le code suivant est généré pour une application Media Wall App :

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

Pour baliser un produit, remplacez `<product 1>` dans l’ `data-lf-attr-product` attribut par l’ID de produit souhaité. Vous pouvez baliser un ou plusieurs produits en ajoutant des identifiants de produit séparés par des virgules supplémentaires. Les produits doivent être contenus dans le dossier de produit de niveau supérieur ou dans les dossiers sélectionnés à l’étape 5.

Le segment de code modifié s’affiche comme suit :

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

L’application affiche désormais uniquement les ID de produit balisés.