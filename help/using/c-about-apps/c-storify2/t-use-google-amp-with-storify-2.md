---
description: Utilisez les API Livefyre pour ajouter la fonctionnalité Google AMP à votre page Storify 2 afin de conserver le contenu interactif et convivial.
seo-description: Utilisez les API Livefyre pour ajouter la fonctionnalité Google AMP à votre page Storify 2 afin de conserver le contenu interactif et convivial.
seo-title: Utiliser Google AMP avec Storify 2
solution: Experience Manager
title: Utiliser Google AMP avec Storify 2
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utiliser Google AMP avec Storify 2{#use-google-amp-with-storify}

Utilisez les API Livefyre pour ajouter la fonctionnalité Google AMP à votre page Storify 2 afin de conserver le contenu interactif et convivial.

Pour utiliser Google AMP avec Storify 2, vous devez créer une page pour votre application Storify 2 avec balisage Google AMP.

La version AMP des demandes d’application se met à jour à partir de la page d’origine (utilisez le paramètre **pollInterval** dans l’API **amp-live-list** pour définir l’intervalle des demandes de mise à jour). Pour vous assurer que les visiteurs de votre page AMP obtiennent rapidement le contenu le plus à jour, conservez un TTL à faible cache sur vos pages Storify 2 AMP.

Les fichiers autres que des images (par exemple, les vidéos) inclus comme publications dans une application Storify 2 doivent utiliser le protocole HTTPS, comme spécifié par la spécification AMP. Les URL AMP qui utilisent le réseau CDN (Google Cloud Content Delivery Network) utilisent le protocole HTTPS.

Pour utiliser Google AMP avec Storify 2 :

1. Créez un modèle validé par AMP sur votre site.
1. Utilisez une ou plusieurs des API Google AMP suivantes pour personnaliser votre page Google AMP :
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) pour personnaliser l’affichage Storify 2
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) pour personnaliser l’intervalle de temps des mises à jour
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) pour ajouter un bouton de partage sur les réseaux sociaux
1. Insérez le contenu de la page Storify 2 AMP suivante dans le fichier CSS de votre page Storify 2 dans le <style amp-custom> tag : [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Insérez le contenu de l’API de balisage AMP Storify 2 suivante dans votre modèle Google AMP : `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` où {{APP_ID}} correspond à l’ID de l’application Storify 2 dans Livefyre Studio.
   1. Le seul paramètre de requête est **pollInterval**, c’est-à-dire l’intervalle dans lequel l’application vérifie la présence de mises à jour (défini en millisecondes).
   1. L’URL inclut le contenu des publications les plus récentes (y compris les tweets, les vidéos, etc.)
   1. La page d’éditeur doit obtenir le contenu de cette URL aussi souvent que vous souhaitez que la page Google AMP soit mise à jour.
