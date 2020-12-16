---
description: Installation des bibliothèques pour les tâches côté serveur Livefyre
seo-description: Installation des bibliothèques pour les tâches côté serveur Livefyre
seo-title: Installation
solution: Experience Manager
title: Installation
uuid: f60b4cc7-178f-4a16-ba75-f1d0d171c52f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---


# Installation{#installation}


## Java {#section_yd3_3zk_rz}

Pour installer la bibliothèque Java, ajoutez cette dépendance au POM de votre projet :

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

La bibliothèque Java dépend des modules suivants :

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

Pour plus d’informations, consultez la documentation Java ou la source sur [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Pour installer la bibliothèque NodeJS, exécutez la ligne suivante :

`$ npm install livefyre`

La bibliothèque NodeJS dépend des modules suivants :

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Pour plus d’informations, consultez la documentation de NodeJs ou la source sur [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Liens : [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Pour installer la bibliothèque PHP avec Composer, ajoutez ceci à votre compositeur.json :

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Installez ensuite à l’aide de :

```
composer.phar install 
```

Si **vous n’utilisez pas** Composer, obtenez la dernière version de la bibliothèque à l’aide de :

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Pour utiliser la bibliothèque, ajoutez ce qui suit à votre script PHP :

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

La bibliothèque PHP dépend des modules suivants :

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Pour plus d&#39;informations, lisez les documents PHP ou consultez la source sur [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Liens : [ext-json](https://php.net/manual/en/book.json.php), [Demandes](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Pour installer la bibliothèque Python, exécutez la ligne suivante :

`$ pip install livefyre`

La bibliothèque Python a des dépendances sur les modules suivants :

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Pour plus d&#39;informations, consultez les documents Python ou consultez la source sur [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Liens : [PyJWT](https://github.com/progrium/pyjwt), [Demandes](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Pour installer la bibliothèque Ruby, ajoutez cette ligne au fichier Gemfile de votre application :

```
gem 'livefyre' 
```

Ou installez-le vous-même :

`$ gem install livefyre`

La bibliothèque Ruby dépend des modules suivants :

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Pour plus d&#39;informations, consultez les documents Ruby ou consultez la source sur [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Liens : [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [Client REST](https://github.com/rest-client/rest-client/), [Adressable](https://github.com/sporkmonger/addressable)
