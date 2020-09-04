---
description: Utilisez les API Livefyre pour ajouter la fonctionnalité Google AMP à votre page Storify 2 afin de garder le contenu interactif et convivial.
seo-description: Utilisez les API Livefyre pour ajouter la fonctionnalité Google AMP à votre page Storify 2 afin de garder le contenu interactif et convivial.
seo-title: Utiliser Google AMP avec Storify 2
solution: Experience Manager
title: Utiliser Google AMP avec Storify 2
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 65d931e5bd04964db44f8e3a0e000ecec2652893
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# Utiliser Google AMP avec Storify 2{#use-google-amp-with-storify}

Utilisez les API Livefyre pour ajouter la fonctionnalité Google AMP à votre page Storify 2 afin de garder le contenu interactif et convivial.

Pour utiliser Google AMP avec Storify 2, vous devez créer une page pour votre application Storify 2 avec balisage Google AMP.

La version AMP de l’application demande des mises à jour à partir de la page d’origine (utilisez le paramètre **pollInterval** dans l’API **amp-live-liste** pour définir l’intervalle des demandes de mise à jour). Pour garantir que les visiteurs de votre page AMP obtiennent rapidement le contenu le plus à jour, conservez une TTL à faible cache sur vos pages Storify 2 AMP.

Les ressources autres que les images (par exemple, les vidéos) incluses comme publications dans une application Storify 2 doivent utiliser le protocole HTTPS, comme spécifié par la spécification AMP. Les URL AMP qui utilisent le réseau CDN (Google Cloud Content Diffusion Network) utilisent le protocole HTTPS.

Pour utiliser Google AMP avec Storify 2 :

1. Créez un modèle validé par AMP sur votre site.
1. Utilisez une ou plusieurs des API AMP Google suivantes pour personnaliser votre page AMP Google :
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) pour personnaliser l’affichage Storify 2
   1. [amp-live-liste](https://www.ampproject.org/docs/reference/components/amp-live-list) pour personnaliser l’intervalle de temps des mises à jour
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) pour ajouter un bouton de partage sur les réseaux sociaux
1. Insérez le contenu de la page AMP Storify 2 suivante dans le fichier CSS de votre page Storify 2 dans la `<style amp-custom>` balise : [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Insérez le contenu de l’API de balisage AMP Storify 2 suivante dans votre modèle AMP Google : `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` où {{APP_ID}} correspond à l’ID d’application de l’application Storify 2 dans Livefyre Studio.
   1. Le seul paramètre de requête est **pollInterval**, qui est l’intervalle dans lequel l’application recherche les mises à jour (défini en millisecondes).
   1. L’URL comprend le contenu des publications les plus récentes (y compris les tweets, les vidéos, etc.)
   1. La page d’éditeur doit obtenir le contenu de cette URL aussi souvent que vous souhaitez que la page AMP de Google soit mise à jour.
