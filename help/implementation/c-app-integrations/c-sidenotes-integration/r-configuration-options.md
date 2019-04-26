---
description: L'objet de configuration Sidenotes est un objet JSON utilisé pour spécifier
  le contenu généré par l'application Livefyre sur la page.
seo-description: L'objet de configuration Sidenotes est un objet JSON utilisé pour
  spécifier le contenu généré par l'application Livefyre sur la page.
seo-title: Options de configuration des tableaux annexes
solution: Experience Manager
title: Options de configuration des tableaux annexes
uuid: 067 e 51 e 6-9720-4226-a 805-c 7 a 07 c 8 cdaa 0 cdaa 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Options de configuration des tableaux annexes{#sidenotes-configuration-options}

L'objet de configuration Sidenotes est un objet JSON utilisé pour spécifier le contenu généré par l'application Livefyre sur la page.

L'objet contient les paramètres suivants :

| Paramètre | Type | Description |
|--- |--- |--- |
| Authdelegate | *required* object | Délégué d'authentification initialisé nouveau ou ancien. |
| Collectionmeta | *required* object | Voir Jeton collectionmeta pour plus d'informations. |
| Customicon | *optional* string | Définit l'URL d'une icône de lanceur personnalisée. Par défaut, la bulle Livefyre. |
| Customstyles | *optional* object | Ajoute des styles personnalisés pour modifier l'apparence des commentaires Sidenotes. Pour plus d'informations, voir Styles personnalisés. |
| Disablestream | *optional* Boolean | Si la valeur est true, désactive la diffusion en temps réel dans cette instance de consigne (et non dans d'autres flux de commentaires). La valeur par défaut est false. |
| environnement | *optional* string | Spécifie l'environnement UAT Livefyre. La seule valeur possible `t402.livefyre.com`est la suivante : Pour la production, ce paramètre doit être supprimé. |
| Iconvisibility | *objet ou* chaîne facultatif | Indique si l'icône de sidenotes est visible au survol ou à la statique. S'il s'agit d'une chaîne, elle est utilisée pour les deux versions de l'icône de bloc (vide et comporte des commentaires Sidenotes). Si un objet, vous devez spécifier chaque type : {empty : ' hover ', num : « static »}. La valeur par défaut est statique. |
| Inlinethreads | *optional* boolean | Si la valeur est true, les threads Sidenote sont insérés directement après le bloc avec lequel ils sont associés. La valeur par défaut est false. |
| Numsidenotesel | *objet,* chaîne ou tableau facultatif | Indique l'élément qui décorera le widget Nombre de commentaires Sidenotes. (Ce widget indique le nombre de mentions annexe sur la page et les informations sur les notes de sidenom.) Si le sélecteur de chaînes correspond à plusieurs éléments, la première est choisie. (Utilise la spécification du sélecteur DOM CSS 3.) |
| position | *optional* string | Détermine la position de la fenêtre contextuelle lorsqu'un élément dont les commentaires sont activés est activé. Les valeurs possibles sont'smart ','left ','right ','bottom '. La valeur par défaut est « intelligent » qui aligne la fenêtre contextuelle à droite de la page, à moins qu'il n'y ait suffisamment d'espace (auquel cas il se passe sous le contenu). |
| sélecteurs | *objet,* chaîne ou tableau requis | Indique les éléments sur lesquels les icônes de lanceur doivent apparaître. (Utilise la spécification du sélecteur DOM CSS 3.) If object, contains a « includes » section and an « exclude » section that apply the CSS selector for any match includes, and remove any elements match the exclude. Si chaîne, inclura les éléments correspondants de la page. If array, list the elements to include. |
| chaînes | *optional* object | Ajoute des chaînes de texte personnalisées pour modifier n'importe quelle langue ou texte dans l'ensemble de l'application. Pour plus d'informations, voir Chaînes personnalisées. |
| Threadcontainerel | *objet,* chaîne ou tableau facultatif | Indique un élément dans lequel le thread des caractères annexes s'affiche. Ce paramètre vous permet de repositionner le thread. Si le sélecteur de chaînes correspond à plusieurs éléments, la première est choisie. (Utilise la spécification du sélecteur DOM CSS 3.) |

