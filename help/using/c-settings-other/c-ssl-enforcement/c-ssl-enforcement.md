---
title: Application SSL
description: Application SSL
exl-id: 033e15d9-84f6-42d5-8457-04263dcbd11c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# Application SSL{#ssl-enforcement}

Pour garantir la sécurité de vos données, nous abandonnons le protocole HTTP en faveur du protocole HTTPS. L&#39;Adobe Livefyre désactivera complètement tous les chiffreurs SSL/TLS HTTP et non sécurisés d&#39;ici la fin août 2018. Il s&#39;agit d&#39;un Adobe Standard conçu pour protéger la confidentialité de vous et de vos utilisateurs.

## Qui est affecté ? {#section_jf2_4yz_kcb}

Cela pourrait avoir un impact sur les clients de Livefyre qui ont :

* Appels serveur à serveur à partir de leur CRM, CMS, WordPress ou d’un autre client.
* Intégrations mobiles (applications Android et iOS)
* Applications personnalisées ou code personnalisé

## Que dois-je faire ?{#section_unv_dc5_kcb}

1. Tous les clients Livefyre doivent communiquer avec toutes les API via HTTPS pour tout le trafic, notamment :

   * Intégrations serveur à serveur (CRM, CMS, WordPress, etc.)
   * Intégrations mobiles (applications Android et iOS)
   * Applications personnalisées (SDK Streamhub ou directement codées).

1. Les clients HTTP Server to Server et Mobile doivent prendre en charge TLS 1.2
1. Remplacez les noms d’hôte de `{*}.<network>.fyre.co` par `<network>.{*}.fyre.co`. Par exemple, le nom d’hôte `example.network.fyre.co` passe à `network.`example.fyre.co&quot;. Par exemple :

   * `bootstrap.<network_name>.fyre.co`sur `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co`sur `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co`sur `<network_name>.admin.fyre.co`

## Comment puis-je savoir si j&#39;ai apporté les changements ? {#section_sqk_5d5_kcb}

Vous pouvez déjà utiliser HTTPS, mais Livefyre vous recommande de vérifier les doublons, en particulier si vous avez :

* Appels serveur à serveur à partir de votre CMS ou de votre gestion de la relation client.
* Code personnalisé ou utilisation de SDK pour les applications personnalisées dans JavaScript ou Mobile.
* Si votre intégration a plus d’un an.
* Si la technologie de votre pile est plus vieille qu&#39;un an.

Même si vous utilisez déjà HTTPS, vous devez vérifier que vos clients API prennent en charge TLS 1.2.

## Comment puis-je vérifier que mes clients API prennent en charge TLS 1.2 ? {#section_nd1_j25_kcb}

Une personne qui travaille au développement de votre site peut :

* Identifiez le logiciel client.
* Identifiez la version.
* Lisez la documentation pour vous assurer que le client API prend en charge TLS 1.2.
* Activez le mode de débogage, si nécessaire.

## Prise en charge de Java pour TLS 1.2 {#section_lwn_rwk_ycb}

Les JVM Oracle et OpenJDK pour Java 8 et versions ultérieures sont configurés pour utiliser TLS 1.2, par défaut, pour toutes les connexions SSL. Vous n’avez pas besoin d’effectuer d’autres actions si vous utilisez Java 8 ou une version ultérieure.

Les utilisateurs de Java 7 ou version antérieure doivent consulter la documentation publique sur la façon d&#39;activer TLS 1.2.

## Pourquoi dois-je changer les noms de mes hôtes ? {#section_d5q_p25_kcb}

Livefyre ne possède pas de certificats SSL sur les domaines `{*}.<network>.fyre.co`. Il vous suffit de modifier l’URL en HTTPS pour rompre l’application.

## Dois-je effectuer la mise à niveau vers la dernière version des SDK Livefyre ? {#section_dw5_s25_kcb}

Non. Vous pouvez à la place corriger le code. Pour corriger le code, vous modifiez certaines chaînes statiques et recréez le code. Si votre client HTTP est obsolète, vous devrez également le mettre à niveau ou en utiliser un autre.

## Combien de temps cela prendra-t-il ? {#section_lgd_v25_kcb}

La durée de cette opération dépend de votre configuration. Si vous avez une mise en oeuvre simple, la confirmation ne devrait pas prendre beaucoup de temps. Si vous avez de nombreuses personnalisations, vous devrez tester et déployer du code mis à jour sur vos serveurs ou de nouvelles applications sur les boutiques d’applications. Pour obtenir de meilleurs résultats, nous vous recommandons de procéder à une vérification initiale du travail afin que vous puissiez planifier tout travail à plus long terme.

## Quel est le calendrier pour terminer ce travail ? {#section_kgk_w25_kcb}

Livefyre désactivera le port 80 (HTTP) de nos services d&#39;ici la fin août 2018 et ne prendra en charge que les connexions à 443 (HTTPS). Les navigateurs et autres clients qui tentent d’utiliser HTTP échouent.

## Quand dois-je terminer ce travail ? {#section_rvb_x25_kcb}

Tous les clients doivent utiliser HTTPS d&#39;ici la fin juillet 2018. Si vous ne pouvez pas respecter cette date limite, contactez notre équipe à l&#39;adresse prioritysupport@livefyre.com.
