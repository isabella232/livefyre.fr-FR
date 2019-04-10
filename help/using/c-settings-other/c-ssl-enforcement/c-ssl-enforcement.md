---
description: valeur nulle
seo-description: valeur nulle
seo-title: Application SSL
solution: Experience Manager
title: Application SSL
uuid: e 64 af 8 c 2-3 ab 6-4034-b 385-0 e 552 d 828 c 6 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Application SSL{#ssl-enforcement}

Pour garantir que vos données restent sécurisées, nous abandonnons le HTTP en faveur du protocole HTTPS. Adobe Livefyre désactivera entièrement tous les chiffrements SSL/TLS non sécurisés d'ici fin août 2018. Il s'agit d'une norme Adobe Standard visant à protéger la confidentialité de vos utilisateurs et de vos utilisateurs.

## Qui est affecté ? {#section_jf2_4yz_kcb}

Cela peut avoir une incidence sur les clients Livefyre qui possèdent :

* Appels serveur à serveur à partir de leur CRM, CMS, Wordpress ou d'un autre client.
* Intégrations mobiles (applications Android et ios)
* Applications personnalisées ou code personnalisé

## Que dois-je faire ? {#section_unv_dc5_kcb}

1. Tous les clients Livefyre doivent communiquer avec toutes les API via HTTPS pour tout le trafic, notamment :

   * Server to Server Integrations (CRM, CMS, Wordpress, etc.)
   * Intégrations mobiles (applications Android et ios)
   * Applications personnalisées (SDK Streamhub ou directement codées).

1. Serveur aux serveurs HTTP et Mobile HTTP doit prendre en charge TLS 1.2
1. Change hostnames from `{*}.<network>.fyre.co` to `<network>.{*}.fyre.co`. Par exemple, le nom d'hôte `example.network.fyre.co` se transforme en `network.`exemple. fyre. co. Par exemple :

   * `bootstrap.<network_name>.fyre.co` to `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` to `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` to `<network_name>.admin.fyre.co`

## Comment puis-je savoir si j'ai apporté les modifications ? {#section_sqk_5d5_kcb}

Vous utilisez peut-être déjà HTTPS, mais Livefyre vous conseille de vérifier deux fois, en particulier si vous avez :

* Appels serveur à serveur à partir de votre CMS ou de votre gestion de la relation client.
* Code personnalisé ou utilisez des kits SDK pour les applications personnalisées dans Javascript ou Mobile.
* Si votre intégration compte plus d'un an - ancienne.
* Si la technologie de votre pile est supérieure à un an.

Même si vous utilisez déjà HTTPS, vous devez vérifier que les clients API prennent en charge TLS 1.2.

## Comment puis-je vérifier que mes clients API prennent en charge TLS 1.2 ? {#section_nd1_j25_kcb}

Une personne qui travaille sur le développement de votre site peut :

* Identifiez le logiciel client.
* Identifiez la version.
* Lisez la documentation pour vous assurer que le client API prend en charge TLS 1.2.
* Activez le mode de débogage, si nécessaire.

## Prise en charge Java pour TLS 1.2 {#section_lwn_rwk_ycb}

Les JVM Oracle et openjdk pour Java 8 et les versions ultérieures sont configurés pour utiliser TLS 1.2, par défaut, pour toutes les connexions SSL. Vous n'avez pas besoin de prendre d'autres mesures si vous utilisez Java 8 ou une version ultérieure.

Les utilisateurs de Java 7 ou d'une version antérieure doivent consulter la documentation publique sur la manière d'activer TLS 1.2.

## Pourquoi dois-je modifier mes noms d'hôtes ? {#section_d5q_p25_kcb}

Livefyre ne dispose pas de certificats SSL sur `{*}.<network>.fyre.co` les domaines. La modification de l'URL en HTTPS interrompt l'application.

## Dois-je mettre à niveau la dernière version des SDK Livefyre ? {#section_dw5_s25_kcb}

Non. Vous pouvez à la place corriger le code. Pour corriger le code, vous modifiez certaines chaînes statiques et recréez le code. Si le client HTTP est en panne - de - date, vous devez également effectuer la mise à niveau ou utiliser un autre paramètre.

## Combien de temps cela prend-il ? {#section_lgd_v25_kcb}

La durée de cette opération dépend de votre configuration. Si vous disposez d'une implémentation simple, cette opération ne devrait prendre que peu de temps. Si vous avez de nombreuses personnalisations, vous devez tester et déployer le code mis à jour sur vos serveurs ou nouvelles applications dans les boutiques d'applications. Pour un résultat optimal, nous vous recommandons d'effectuer une vérification initiale du travail afin que vous puissiez planifier un travail à plus long terme.

## Quel est le plan de montage chronologique pour effectuer cette opération ? {#section_kgk_w25_kcb}

Livefyre désactivera le port 80 (HTTP) à nos services d'ici la fin août 2018 et ne prend en charge que les connexions à 443 (HTTPS). Les navigateurs et autres clients qui tentent d'utiliser HTTP échoueront.

## Quand dois-je terminer cette opération ? {#section_rvb_x25_kcb}

Tous les clients doivent utiliser HTTPS d'ici la fin juillet 2018. Si vous ne pouvez pas respecter cette échéance, contactez notre équipe à l'adresse prioritysupport@livefyre.com.
