---
description: L’objet de configuration Sidenotes est un objet JSON utilisé pour spécifier le contenu rendu par l’application Livefyre sur la page.
seo-description: L’objet de configuration Sidenotes est un objet JSON utilisé pour spécifier le contenu rendu par l’application Livefyre sur la page.
seo-title: Options de configuration Sidenotes
solution: Experience Manager
title: Options de configuration Sidenotes
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Options de configuration Sidenotes{#sidenotes-configuration-options}

L’objet de configuration Sidenotes est un objet JSON utilisé pour spécifier le contenu rendu par l’application Livefyre sur la page.

L’objet contient les paramètres suivants :

| Paramètre | Type | Description |
|--- |--- |--- |
| authDelegate | *objet obligatoire* | délégué d’authentification initialisée de style nouveau ou ancien. |
| collectionMeta | *objet obligatoire* | Voir collectionMeta token pour plus d’informations. |
| customIcon | *chaîne facultative* | Définit l’URL d’une icône de lancement personnalisée. La bulle Livefyre est utilisée par défaut. |
| customStyles | *objet facultatif* | Ajoute des styles personnalisés pour modifier l’aspect des Sidenotes. Pour plus d’informations, voir Styles personnalisés. |
| disableStream | *booléen facultatif* | Si la valeur est true, la diffusion en continu en temps réel est désactivée dans cette instance Sidenotes (et non dans d’autres flux de commentaires). La valeur par défaut est false. |
| environnement | *chaîne facultative* | Spécifie l’environnement UAT de Livefyre. La seule valeur possible est `t402.livefyre.com`. Pour la production, ce paramètre doit être supprimé. |
| iconVisibility | *objet ou chaîne facultatif* | Définit si l’icône Sidenotes est visible au survol ou statique. S’il s’agit d’une chaîne, elle sera utilisée pour les deux versions de l’icône de bloc (vide et avec Sidenotes). Si un objet est défini, vous devez spécifier chaque type : {empty: "hover", num: ‘static’}. La valeur par défaut est statique. |
| inlineThreads | *booléen facultatif* | Si la valeur est true, les threads Sidenote sont insérés directement après le bloc auquel ils sont associés. La valeur par défaut est false. |
| numSidenotesEl | *objet, chaîne ou tableau facultatif* | Indique l’élément que le widget Nombre de signets va décorer. (Ce widget montre le nombre de notes de côté sur la page et des informations sur les Sidenotes.) Si le sélecteur de chaînes correspond à plusieurs éléments, le premier est choisi. (Utilise les spécifications du sélecteur DOM CSS3.) |
| position | *chaîne facultative* | Détermine la position de la fenêtre contextuelle lorsqu’un utilisateur clique sur un élément pour lequel les identifications sont activées. Les valeurs possibles sont ‘smart’, ‘left’, ‘right’, ‘bottom’. La valeur par défaut est "intelligent", ce qui aligne la fenêtre contextuelle sur la droite de la page, sauf s’il n’y a pas assez d’espace (auquel cas elle passe sous le contenu). |
| sélecteurs | *objet, chaîne ou tableau requis* | Spécifie les éléments sur lesquels les icônes de lancement doivent apparaître. (Utilise les spécifications du sélecteur DOM CSS3.) Si objet, inclut une section "inclut" et une section "exclut" qui applique le sélecteur CSS pour toute correspondance inclut, et supprime tous les éléments correspondant aux exclusions. Si la chaîne est définie, inclut tous les éléments correspondants sur la page. Si array, répertorie les éléments à inclure. |
| chaînes | *objet facultatif* | Ajoute des chaînes de texte personnalisées pour modifier n’importe quelle langue ou texte dans toute l’application. Pour plus d’informations, voir Chaînes personnalisées. |
| threadContainerEl | *objet, chaîne ou tableau facultatif* | Spécifie un élément dans lequel le thread des notes de côté apparaîtra. Ce paramètre vous permet de repositionner le thread. Si le sélecteur de chaînes correspond à plusieurs éléments, le premier est choisi. (Utilise les spécifications du sélecteur DOM CSS3.) |

