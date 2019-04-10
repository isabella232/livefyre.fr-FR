---
description: Installation des bibliothèques pour les tâches côté serveur Livefyre
seo-description: Installation des bibliothèques pour les tâches côté serveur Livefyre
seo-title: Installation
solution: Experience Manager
title: Installation
uuid: f 60 b 4 cc 7-178 f -4 a 16-ba 75-f 1 d 0 d 171 c 52 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Installation{#installation}


## Java {#section_yd3_3zk_rz}

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

Pour plus d'informations, lisez la documentation Java ou la source sur [github](https://github.com/Livefyre/livefyre-java-utils).

## Nodejs {#section_swj_pwq_rz}

Pour installer la bibliothèque nodejs, exécutez la ligne suivante :

`$ npm install livefyre`

La bibliothèque nodejs possède des dépendances aux modules suivants :

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Pour plus d'informations, lisez la documentation nodejs ou la source sur [github](https://github.com/Livefyre/livefyre-nodejs-utils).

Liens : [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Pour installer la bibliothèque PHP avec le compositeur, ajoutez-la à votre compositeur. json :

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Ensuite, effectuez l'installation à l'aide de :

```
composer.phar install 
```

Si vous **n** 'utilisez pas le compositeur, procurez-vous la dernière version de la bibliothèque à l'aide de :

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Pour utiliser la bibliothèque, ajoutez les éléments suivants à votre script PHP :

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

La bibliothèque PHP possède des dépendances aux modules suivants :

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Pour plus d'informations, lisez la documentation PHP ou la source sur [github](https://github.com/Livefyre/livefyre-php-utils).

Liens : [ext-json](https://php.net/manual/en/book.json.php), [Requests](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Pour installer la bibliothèque Python, exécutez la ligne suivante :

`$ pip install livefyre`

La bibliothèque Python dépend des modules suivants :

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Pour plus d'informations, lisez la documentation Python ou la source sur [github](https://github.com/Livefyre/livefyre-python-utils).

Liens : [Pyjwt](https://github.com/progrium/pyjwt), [Requêtes](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum 34](https://pypi.python.org/pypi/enum34), [ordereddict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Pour installer la bibliothèque Ruby, ajoutez cette ligne au fichier Gemfichier de l'application :

```
gem 'livefyre' 
```

Ou installez-la vous-même :

`$ gem install livefyre`

La bibliothèque Ruby dispose des dépendances des modules suivants :

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Pour plus d'informations, lisez la documentation Ruby ou la source sur [github](https://github.com/Livefyre/livefyre-ruby-utils).

Liens : [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Addressable](https://github.com/sporkmonger/addressable)
