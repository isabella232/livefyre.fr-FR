---
description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu du courrier électronique.
seo-description: Vous pouvez créer des règles de diffusion en continu qui extraient le contenu du courrier électronique.
seo-title: Règles de messagerie
solution: Experience Manager
title: Règles de messagerie
uuid: 3cd27d28-b7c0-4cbc-bae3-e2ef7beacba9
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Règles de messagerie{#email-rules}

Vous pouvez créer des règles de diffusion en continu qui extraient le contenu du courrier électronique.

La création de flux basés sur le courrier électronique vous permet de publier du contenu directement dans une application ou un dossier par courrier électronique.

Utilisez cette fonctionnalité pour permettre aux contributeurs de publier directement sur vos applications ou bibliothèques de fichiers depuis leur ordinateur ou leur périphérique mobile.

Une fois la règle créée, tout courrier électronique contenant une image ou un fichier vidéo envoyé à l’adresse électronique répertoriée sera publié directement dans votre application ou votre bibliothèque de fichiers, comme indiqué. Les courriers électroniques envoyés avec plusieurs pièces jointes publieront tous les fichiers à l’emplacement approprié. Les courriels envoyés à l'adresse répertoriée contenant uniquement du texte ne feront rien.

Une fois envoyé, les champs du courrier électronique sont utilisés pour renseigner les éléments suivants pour le contenu :

* **[!UICONTROL From:]** Utilisé comme auteur du contenu, si le compte utilisateur existe. S’il n’existe aucun compte pour l’expéditeur, l’auteur est répertorié comme anonyme.
* **[!UICONTROL Subject:]** Utilisé pour le titre du contenu.
* **[!UICONTROL Body:]** Permet de renseigner les détails du contenu dans Studio.
* **[!UICONTROL Attachments:]** Les fichiers multimédia doivent être joints, sinon le courrier électronique sera ignoré. Les types de fichiers pris en charge sont les suivants : 3GP, ASF, AVI, DV, GIF, JPG, MOV, MP4, MPEG, MPG, PNG, QT et WMV. Le total de toutes les pièces jointes doit être inférieur à 25 Mo de taille de fichier.

Pour obtenir des options de règle de diffusion en continu supplémentaires pour toutes les règles de diffusion en continu, voir Options de règle de [diffusion en continu pour toutes les règles](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de diffusion en continu.
