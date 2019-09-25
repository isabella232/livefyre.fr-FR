---
description: valeur nulle
seo-description: valeur nulle
seo-title: SSL Enforcement
solution: Experience Manager
title: SSL Enforcement
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# SSL Enforcement{#ssl-enforcement}

To ensure your data remains secure, we are deprecating HTTP in favor of HTTPS. Adobe Livefyre will disable all HTTP and insecure SSL/TLS ciphers completely by end of August 2018. This is an Adobe Standard designed to protect the privacy of you and your users.

## Who is affected? {#section_jf2_4yz_kcb}

This could impact Livefyre customers who have:

* Appels serveur à serveur à partir de leur CRM, CMS, WordPress ou d’un autre client.
* Intégrations mobiles (applications Android et iOS)
* Applications personnalisées ou code personnalisé

## Que dois-je faire ?{#section_unv_dc5_kcb}

1. Tous les clients Livefyre doivent communiquer avec toutes les API via HTTPS pour tout le trafic, notamment :

   * Intégrations serveur à serveur (CRM, CMS, WordPress, etc.)
   * Intégrations mobiles (applications Android et iOS)
   * Applications personnalisées (SDK Streamhub ou directement codées).

1. Serveur vers serveur et clients HTTP mobiles doivent prendre en charge TLS 1.2
1. Change hostnames from  to . `{*}.<network>.fyre.co``<network>.{*}.fyre.co` Par exemple, le nom d’hôte `example.network.fyre.co` devient `network.`example.fyre.co". Par exemple :

   * `bootstrap.<network_name>.fyre.co`sur `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co`sur `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co`sur `<network_name>.admin.fyre.co`

## Comment puis-je savoir si j'ai fait les changements ? {#section_sqk_5d5_kcb}

Vous pouvez déjà utiliser le protocole HTTPS, mais Livefyre vous recommande de vérifier deux fois, surtout si vous avez :

* Appels serveur à serveur à partir de votre CMS ou CRM.
* Code personnalisé ou utilisation de SDK pour les applications personnalisées dans JavaScript ou Mobile.
* Si votre intégration a plus d’un an.
* Si la technologie dans votre pile est plus ancienne qu'un an.

Même si vous utilisez déjà HTTPS, vous devez vérifier que vos clients API prennent en charge TLS 1.2.

## Comment puis-je vérifier que mes clients API prennent en charge TLS 1.2 ? {#section_nd1_j25_kcb}

Une personne qui travaille au développement de votre site peut :

* Identifiez le logiciel client.
* Identifiez la version.
* Lisez la documentation pour vous assurer que le client API prend en charge TLS 1.2.
* Activez le mode de débogage, si nécessaire.

## Prise en charge de Java pour TLS 1.2 {#section_lwn_rwk_ycb}

Les JVM Oracle et OpenJDK pour Java 8 et versions ultérieures sont configurés pour utiliser TLS 1.2, par défaut, pour toutes les connexions SSL. Vous n’avez pas besoin d’effectuer d’autres actions si vous utilisez Java 8 ou une version ultérieure.

Les utilisateurs de Java 7 ou version antérieure doivent consulter la documentation publique pour savoir comment activer TLS 1.2.

## Pourquoi dois-je changer le nom de mon hôte ? {#section_d5q_p25_kcb}

Livefyre ne possède pas de certificats SSL sur `{*}.<network>.fyre.co` les domaines. Il suffit de modifier l’URL en HTTPS pour rompre l’application.

## Dois-je effectuer la mise à niveau vers la dernière version des SDK Livefyre ? {#section_dw5_s25_kcb}

Non. Vous pouvez le corriger. Pour corriger le code, vous modifiez certaines chaînes statiques et recréez le code. Si votre client HTTP est obsolète, vous devrez également le mettre à niveau ou en utiliser un autre.

## Combien de temps cela prendra-t-il ? {#section_lgd_v25_kcb}

Le temps que cela prend dépend de votre configuration. Si vous disposez d’une implémentation simple, la confirmation ne devrait pas prendre beaucoup de temps. Si vous avez de nombreuses personnalisations, vous devrez tester et déployer du code mis à jour sur vos serveurs ou sur de nouvelles applications dans les boutiques d’applications. Pour obtenir de meilleurs résultats, nous vous recommandons de procéder à une vérification initiale du travail afin que vous puissiez planifier tout travail à plus long terme.

## Quel est le calendrier pour terminer ce travail ? {#section_kgk_w25_kcb}

Livefyre désactivera le port 80 (HTTP) de nos services d'ici fin août 2018 et ne prendra en charge que les connexions à 443 (HTTPS). Les navigateurs et autres clients qui tentent d’utiliser HTTP échouent.

## Quand dois-je terminer ce travail ? {#section_rvb_x25_kcb}

Tous les clients doivent utiliser HTTPS d’ici la fin juillet 2018. Si vous ne pouvez pas respecter cette date limite, contactez notre équipe à l’adresse prioritysupport@livefyre.com.
