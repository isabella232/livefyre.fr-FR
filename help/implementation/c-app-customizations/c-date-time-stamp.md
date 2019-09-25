---
description: Personnalisez les tampons de date et d’heure à l’aide de Livefyre.js.
seo-description: Personnalisez les tampons de date et d’heure à l’aide de Livefyre.js.
seo-title: Personnalisation de l’horodatage et de la date
solution: Experience Manager
title: Personnalisation de l’horodatage et de la date
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisation de l’horodatage et de la date{#customize-the-date-and-time-stamp}

Personnalisez les tampons de date et d’heure à l’aide de Livefyre.js.

Les applications Livefyre fournissent le paramètre d’option, datetimeFormat, pour spécifier le format de date, comme décrit ci-dessous.

* [Terminologie](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formatage](#c_date_time_stamp/section_ynx_gn4_xz)
* [Désignation de symbole](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologie {#section_xsk_jn4_xz}

* **Les horodatages** absolus sont définis comme des heures exactes et spécifiques (par exemple, 1er janvier 2012 à 12h00)
* **Les horodatages** relatifs sont définis comme des périodes générales et moins précises (p. ex., il y a 25 secondes, 14 minutes, 1 jour auparavant, 1 an auparavant, etc.)

## Formatage {#section_ynx_gn4_xz}

Le paramètre datetimeFormat a le comportement par défaut suivant lorsqu’aucun argument n’est donné :

* Format de date et heure de : JJ MMM aaaa (pour le 8 janvier 2012)
* 20160 Minutes (14 jours) jusqu’à l’heure absolue (14 jours jusqu’à ce que les horodatages relatifs deviennent des horodatages absolus)

Le paramètre datetimeFormat accepte trois types d’arguments possibles : datetime, format et chaîne.

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

Un objet spécifiant la valeur absolueFormat et/ou la valeur minutesJusqu’à la valeur absolueTime. Une valeur de minutesBeforeAbsoluteTime de -1 rendra l’heure absolue immédiate.

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

Les fonctions de formatage datetime suivent la spécification de modèle définie dans JDK, ICU et CLDR, avec des modifications mineures pour une utilisation typique dans JS. Pour plus d’informations, voir la documentation [de la bibliothèque de fermeture de](https://developers.google.com/closure/library/docs/overview)Google.

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

Les éléments marqués avec "*" ne sont pas encore pris en charge.

Les éléments marqués avec "#" fonctionnent différemment que Java.

Le nombre de lettres de modèle détermine le format.

* **** Texte : 4 ou plus, utilisez le formulaire complet. Moins de 4, utilisez un formulaire court ou abrégé s’il existe. (Par exemple : "EEEE" produit "Monday", "EEE" produit "Mon".)
* **** Nombre : nombre minimal de chiffres. Les nombres les plus courts sont précédés de zéro (par exemple : Si "m" produit "6", "mm" produit "06".) L'année est traitée spécialement; en d’autres termes, si le nombre de "y" est de 2, l’année sera tronquée à 2 chiffres. (Par exemple : si "yyy" produit "1997", "yy" produit "97".) Contrairement aux autres champs, les secondes fractionnaires sont ajoutées à droite avec zéro.
* **** Texte et numéro : 3 ou plus, utilisez du texte. Moins de 3, utilisez le numéro. (Par exemple : "M" produit "1", "MM" produit "01", "MMM" produit "Jan" et "MMMM" produit "Janvier".)

Tout caractère du modèle qui ne se trouve pas dans les plages de ["a"..."z’] et ["A"..."Z’] sera traité comme du texte cité. Par exemple, des caractères tels que ":", ".", ", "#" et "@" apparaissent dans le texte temporel résultant, même s’ils ne sont pas pris entre guillemets simples.
