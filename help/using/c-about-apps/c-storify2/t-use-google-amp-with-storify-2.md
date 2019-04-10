---
description: Utilisez les API Livefyre pour ajouter une fonctionnalité Google AMP
  à votre page Storify 2 afin de conserver le contenu interactif et adapté au SEO.
seo-description: Utilisez les API Livefyre pour ajouter une fonctionnalité Google
  AMP à votre page Storify 2 afin de conserver le contenu interactif et adapté au
  SEO.
seo-title: Utilisation de Google AMP avec Storify 2
solution: Experience Manager
title: Utilisation de Google AMP avec Storify 2
uuid: 40 c 9 f 083-7284-43 ba-ae 27-53 b 1 ff 9 e 3954
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Utilisation de Google AMP avec Storify 2{#use-google-amp-with-storify}

Utilisez les API Livefyre pour ajouter une fonctionnalité Google AMP à votre page Storify 2 afin de conserver le contenu interactif et adapté au SEO.

Pour utiliser Google AMP avec Storify 2, vous devez créer une page pour votre application Storify 2 avec les annotations Google AMP.

La version AMP de l'application demande des mises à jour à partir de la page d'origine (utilisez le **paramètre pollinterval** dans l'API **amp-live-list** pour définir l'intervalle des requêtes de mise à jour). Pour garantir que les visiteurs de votre page AMP obtiennent rapidement le contenu le plus récent, conservez TTL à faible cache sur vos pages Storify 2 AMP.

Les fichiers non image (par exemple, vidéos) inclus comme publications dans une application Storify 2 doivent utiliser HTTPS comme spécifié par la spécification AMP. Les URL AMP qui utilisent le réseau de diffusion de contenu de Google Cloud utilisent HTTPS.

Pour utiliser Google AMP avec Storify 2 :

1. Créez un modèle validé AMP sur votre site.
1. Utilisez une ou plusieurs des API Google AMP suivantes pour personnaliser votre page Google AMP :
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) pour personnaliser l'affichage Storify 2
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) pour personnaliser l'intervalle de temps des mises à jour
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) pour ajouter un bouton de partage sur réseau social
1. Incluez le contenu de la page Storify 2 AMP suivante dans le CSS de votre page Storify 2 dans la page <style amp-custom> tag : [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Insérez le contenu de l'API Markup 2 AMP suivante dans votre modèle AMP Google : `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` où {{APP_ ID}} correspond à l'ID d'application de l'application Storify 2 dans Livefyre Studio.
   1. Le seul paramètre de requête est **pollinterval**, qui correspond à l'intervalle dans lequel l'application recherche les mises à jour (définies en millisecondes).
   1. L'URL comprend le contenu des publications les plus récentes (y compris Tweets, Vidéos, etc.)
   1. La page de l'éditeur doit obtenir le contenu de cette URL aussi souvent que vous souhaitez que la page Google AMP soit mise à jour.
