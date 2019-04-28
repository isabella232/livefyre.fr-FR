---
description: Personnalisez les horodatages de date et d'heure à l'aide de Livefyre. js.
seo-description: Personnalisez les horodatages de date et d'heure à l'aide de Livefyre. js.
seo-title: Personnalisation de la date et de l'heure
solution: Experience Manager
title: Personnalisation de la date et de l'heure
uuid: 632 ea 405-56 b 7-4664-8 d 2 b -0 dd 0 a 7611 bd 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personnalisation de la date et de l&#39;heure{#customize-the-date-and-time-stamp}

Personnalisez les horodatages de date et d&#39;heure à l&#39;aide de Livefyre. js.

Les applications Livefyre fournissent le paramètre d&#39;option, datetimeformat, pour spécifier le format de date comme décrit ci-dessous.

* [Terminologie](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formatage](#c_date_time_stamp/section_ynx_gn4_xz)
* [Désignation du symbole](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologie {#section_xsk_jn4_xz}

* **Les horodatages absolus** sont définis comme des heures exactes et spécifiques (p. ex. : 1 er janvier 2012 à 12 h 00)
* **Les horodatages** relatifs sont définis comme des heures générales et moins précises (il y a 25 secondes, il y a 14 minutes, il y a 1 jour, il y a 1 an, etc.).

## Formatage {#section_ynx_gn4_xz}

Le paramètre datetimeformat présente le comportement par défaut suivant lorsqu&#39;aucun argument n&#39;est donné :

* Format de date de : MMMM d yyyy (pour le 8 janvier 2012)
* 20160 minutes (14 jours) jusqu&#39;à la durée absolue (14 jours jusqu&#39;à ce que les horodatages relatifs deviennent des horodatages absolus)

Le paramètre datetimeformat accepte trois types d&#39;arguments possibles : datetime, format et chaîne.

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

Objet spécifiant absoluteformat et/ou minutesuntilabsolutetime. A minutesuntilabsolutetime avec la valeur -1 rend immédiatement la durée absolue de la temporisation.

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

Fonction qui prend comme argument un objet Date et renvoie une chaîne datetime à afficher.

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

## Désignation du symbole {#section_inq_2n4_xz}

Fonctions de formatage de Datetime suivant les spécifications du modèle définies dans JDK, ICU et CLDR, avec une modification mineure pour une utilisation standard dans JS. Pour plus d&#39;informations, consultez la documentation de la bibliothèque de fermeture [de Google](https://developers.google.com/closure/library/docs/overview).

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

Les éléments marqués de « * » ne sont pas encore pris en charge.

Les éléments marqués de &#39;#&#39;fonctionnent différemment de Java.

Le nombre de lettres détermine le format.

* **Texte :** 4 ou plus, utilisez le formulaire complet. Moins de 4, utilisez un formulaire court ou abrégé s&#39;il existe. (Par exemple : « EEEE » produit « Lundi », « EEE » produit « Mon ».)
* **Nombre :** le nombre minimum de chiffres. Les nombres plus courts sont de zéro à ce montant (par exemple : Si « m » produit « 6 », « mm » produit « 06 ». L&#39;année est gérée spécialement ; autrement dit, si le nombre de « y » est 2, l&#39;année est tronquée à 2 chiffres. (Par exemple : si « yyyy » produit « 1997 », « aa » produit « 97 ».) Contrairement aux autres champs, les secondes fractionnaires sont ajoutées à droite avec zéro.
* **Texte et numéro :** 3 ou plus, utilisez du texte. Moins de 3, utilisez le numéro. (Par exemple : « M » produit « 1 », « MM » produit « 01 », « MMM » produit « Jan » et « MMMM » produit « janvier ».)

Tous les caractères du modèle qui ne sont pas dans les plages [de « a ».&#39;z&#39;] et [&#39;A &#39;.&#39;&#39;Z&#39;] sera traité comme du texte entre guillemets. Par exemple, caractères tels que &#39;: &#39;,&#39;. &#39;,&#39;,&#39;#&#39;et &#39;@&#39;apparaissent dans le texte de l&#39;heure qui en résulte, même ceux qui ne sont pas incorporés dans des guillemets simples.
