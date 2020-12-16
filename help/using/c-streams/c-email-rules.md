---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu du courrier électronique.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu du courrier électronique.
seo-title: règles d'émail
solution: Experience Manager
title: règles d'émail
uuid: 3cd27d28-b7c0-4cbc-bae3-e2ef7beacba9
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# règles d&#39;émail{#email-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu du courrier électronique.

La création de flux basés sur le courrier électronique vous permet de publier du contenu directement dans une application ou un dossier par courrier électronique.

Utilisez cette fonction pour permettre aux contributeurs de publier directement sur vos applications ou votre bibliothèque de fichiers depuis leur ordinateur ou leur périphérique mobile.

Une fois la règle créée, tout courrier électronique contenant une image ou un fichier vidéo envoyé à l’adresse électronique répertoriée sera publié directement sur votre application ou votre bibliothèque de fichiers, comme indiqué. Les courriers électroniques envoyés avec plusieurs pièces jointes publieront tous les fichiers à l’emplacement approprié. Les courriels envoyés à l&#39;adresse répertoriée contenant uniquement du texte ne feront rien.

Une fois envoyé, les champs du courrier électronique seront utilisés pour renseigner les éléments suivants pour l’élément de contenu :

* **[!UICONTROL From:]** Utilisé comme auteur du contenu, si le compte utilisateur existe. S’il n’existe aucun compte pour l’expéditeur, l’auteur est répertorié comme anonyme.
* **[!UICONTROL Subject:]** Utilisé pour le titre du contenu.
* **[!UICONTROL Body:]** Permet de renseigner les détails du contenu dans Studio.
* **[!UICONTROL Attachments:]** Les fichiers multimédias doivent être joints, sinon le courrier électronique sera ignoré. Les types de fichiers pris en charge sont les suivants : 3GP, ASF, AVI, DV, GIF, JPG, MOV, MP4, MPEG, MPG, PNG, QT et WMV. La taille totale de toutes les pièces jointes doit être inférieure à 25 Mo.

Pour obtenir des options de règle de diffusion supplémentaires pour toutes les règles de diffusion en continu, voir [Options de règle de diffusion pour toutes les règles de diffusion en continu](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
