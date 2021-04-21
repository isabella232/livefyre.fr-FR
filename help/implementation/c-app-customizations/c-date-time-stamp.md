---
description: Personnalisez les horodatages et les dates à l’aide de Livefyre.js.
title: Personnalisation de l’horodatage et de la date
exl-id: 77130793-00ba-4a5c-8318-4221d971da6c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# Personnaliser l’horodatage et la date{#customize-the-date-and-time-stamp}

Personnalisez les horodatages et les dates à l’aide de Livefyre.js.

Les applications Livefyre fournissent le paramètre d’option datetimeFormat, pour spécifier le format de date, comme décrit ci-dessous.

* [Terminologie](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formatage](#c_date_time_stamp/section_ynx_gn4_xz)
* [Désignation de symbole](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologie {#section_xsk_jn4_xz}

* **Les** horodatages absolus sont définis comme des heures exactes et spécifiques (1er janvier 2012, 12h00, par exemple)
* **Les** horodatages relatifs sont définis comme des heures générales et moins précises (par exemple, il y a 25 secondes, il y a 14 minutes, il y a 1 jour, il y a 1 an, etc.)

## Formatage {#section_ynx_gn4_xz}

Le paramètre datetimeFormat a le comportement par défaut suivant lorsqu’aucun argument n’est donné :

* Format de date et heure de : JMMM aaaa (pour le 8 janvier 2012)
* 20160 Minutes (14 jours) jusqu’à l’heure absolue (14 jours jusqu’à ce que les horodatages relatifs deviennent des horodatages absolus)

Le paramètre datetimeFormat accepte trois types d&#39;argument possibles : datetime, format et chaîne.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Un objet spécifiant les paramètres absolueFormat et/ou minutesJusqu&#39;àAbsoluteTime. Une valeur de -1 pour minutesJusquAbsoluteTime rend l&#39;heure absolue immédiate.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Fonction qui prend comme argument un objet Date et renvoie une chaîne datetime à afficher

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## Désignation de symbole {#section_inq_2n4_xz}

Les fonctions de mise en forme des dates suivent les spécifications de modèle définies dans le JDK, l&#39;ICU et le CLDR, avec des modifications mineures pour une utilisation typique dans JS. Pour plus d’informations, voir la [documentation de la bibliothèque de fermeture de Google](https://developers.google.com/closure/library/docs/overview).

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

Les éléments signalés par &quot;*&quot; ne sont pas encore pris en charge.

Les éléments signalés par &quot;#&quot; fonctionnent différemment que Java.

Le nombre de lettres de modèle détermine le format.

* **Texte :** 4 ou plus, utilisez le formulaire complet. Moins de 4, utilisez un formulaire court ou abrégé s’il existe. (Par exemple : &quot;EEEE&quot; produit &quot;Lundi&quot;, &quot;EEE&quot; produit &quot;Lun&quot;.)
* **Nombre : nombre minimum** de chiffres. Les nombres plus courts sont à zéro pour ce montant (par exemple : Si &quot;m&quot; produit &quot;6&quot;, &quot;mm&quot; produit &quot;06&quot;.) L&#39;année est gérée spécialement ; en d’autres termes, si le nombre de &quot;y&quot; est de 2, l’année sera tronquée à 2 chiffres. (Par exemple : si &quot;yyy&quot; produit &quot;1997&quot;, &quot;yy&quot; produit &quot;97&quot;.) Contrairement aux autres champs, les secondes fractionnaires sont ajoutées à droite avec zéro.
* **Texte et nombre :** 3 ou plus, utilisez du texte. Moins de 3, utilisez le numéro. (Par exemple : &quot;M&quot; produit &quot;1&quot;, &quot;MM&quot; produit &quot;01&quot;, &quot;MMM&quot; produit &quot;Jan&quot; et &quot;MMMM&quot; produit &quot;Janvier&quot;.)

Tout caractère du modèle qui ne se trouve pas dans les plages de [‘a’..&quot;z’] et [‘A’.&quot;Z’] sera traité comme du texte entre guillemets. Par exemple, les caractères tels que &quot;:&quot;, &quot;.&quot;, &quot;, &quot;#&quot; et &quot;@&quot; apparaîtront dans le texte temporel obtenu, même s’ils ne sont pas pris en compte entre guillemets simples.
