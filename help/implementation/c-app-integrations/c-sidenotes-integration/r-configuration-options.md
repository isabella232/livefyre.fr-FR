---
description: L’objet de configuration Sidenotes est un objet JSON utilisé pour spécifier le contenu rendu par l’application Livefyre sur la page.
title: Identifie les options de configuration
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# Identifie les options de configuration{#sidenotes-configuration-options}

L’objet de configuration Sidenotes est un objet JSON utilisé pour spécifier le contenu rendu par l’application Livefyre sur la page.

L’objet contient les paramètres suivants :

| Paramètre | Type | Description |
|--- |--- |--- |
| authDelegate | ** requiredobject | Délégué d&#39;authentification initialisé de style nouveau ou ancien. |
| collectionMeta | ** requiredobject | Voir collectionMeta token pour plus d’informations. |
| customIcon | ** optionalstring | Définit l’URL d’une icône de lancement personnalisée. Par défaut, la bulle Livefyre est utilisée. |
| customStyles | ** optionalobject | Ajoute des styles personnalisés pour modifier l’aspect des Sidenotes. Pour plus d’informations, voir Styles personnalisés. |
| disableStream | ** optionalBoolean | Si la valeur est true, désactive la diffusion en temps réel dans cette instance Sidenotes (et non dans d’autres flux de commentaires). La valeur par défaut est false. |
| environnement | ** optionalstring | Indique l’environnement UAT Livefyre. La seule valeur possible est `t402.livefyre.com`. Pour la production, ce paramètre doit être supprimé. |
| iconVisibility | ** facultatif, objet ou chaîne | Indique si l’icône Sidenotes est visible au survol ou statique. S&#39;il s&#39;agit d&#39;une chaîne, elle sera utilisée pour les deux versions de l&#39;icône de bloc (vide et avec des Sidenotes). Si un objet est défini, vous devez spécifier chaque type : {empty: &quot;hover&quot;, num : ‘static’}. La valeur par défaut est statique. |
| inlineThreads | ** optionalboolean | Si la valeur est true, les threads Sidenote sont insérés directement après le bloc auquel ils sont associés. La valeur par défaut est false. |
| numSidenotesEl | ** facultatif, objet, chaîne ou tableau | Indique l’élément que le widget Nombre de Sidenotes décorera. (Ce widget affiche le nombre de notes de côté sur la page et des informations sur les Sidenotes.) Si le sélecteur de chaînes correspond à plusieurs éléments, le premier est choisi. (Utilise les spécifications du sélecteur DOM CSS3.) |
| position | ** optionalstring | Détermine la position de la fenêtre contextuelle lorsque l’utilisateur clique sur un élément pour lequel les identifications sont activées. Les valeurs possibles sont &quot;smart&quot;, &quot;left&quot;, &quot;right&quot;, &quot;bottom&quot;. La valeur par défaut est &quot;intelligent&quot;, ce qui aligne la fenêtre contextuelle sur la droite de la page, sauf s’il n’y a pas suffisamment d’espace (auquel cas elle passe en dessous du contenu). |
| sélecteurs | ** requiredobject, string ou array | Spécifie les éléments sur lesquels les icônes de lancement doivent apparaître. (Utilise les spécifications du sélecteur DOM CSS3.) Si objet, inclut une section &quot;inclut&quot; et une section &quot;exclut&quot; qui applique le sélecteur CSS pour toute correspondance inclut et supprime tous les éléments correspondant aux exclusions. Si la chaîne est définie, inclura tous les éléments correspondants sur la page. Si tableau, liste les éléments à inclure. |
| chaînes | ** optionalobject | Ajoute des chaînes de texte personnalisées pour modifier n’importe quelle langue ou texte dans toute l’application. Pour plus d’informations, voir Chaînes personnalisées. |
| threadContainerEl | ** facultatif, objet, chaîne ou tableau | Spécifie un élément dans lequel le thread des notes de côté apparaîtra. Ce paramètre vous permet de repositionner le thread. Si le sélecteur de chaînes correspond à plusieurs éléments, le premier est choisi. (Utilise les spécifications du sélecteur DOM CSS3.) |
