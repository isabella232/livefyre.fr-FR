---
description: Le nombre d’écouteurs est un compteur qui suit le nombre de visiteurs du site pour une application sur une page et affiche ce nombre.
seo-description: Le nombre d’écouteurs est un compteur qui suit le nombre de visiteurs du site pour une application sur une page et affiche ce nombre.
seo-title: Nombre d’écouteurs
solution: Experience Manager
title: Nombre d’écouteurs
uuid: fdd7cfe4-ae69-4d31-baa2-8978368fc3e8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Nombre d’écouteurs{#listener-count}

Le nombre d’écouteurs est un compteur qui suit le nombre de visiteurs du site pour une application sur une page et affiche ce nombre.

Le nombre d’écouteurs est le nombre de visiteurs du site qui ont un navigateur ouvert sur la page sur laquelle une application est instanciée. Cela vous permet de connaître le nombre de visiteurs du site qui se trouvent sur la page à un moment donné, de sorte que vous puissiez les suivre pendant qu’ils regardent du contenu en flux continu ou en direct en temps réel.

Le nombre d’écouteurs de Livefyre fonctionne comme suit :

1. Le site qui contient votre application envoie un ping sur un serveur Livefyre toutes les 60 secondes.
1. Le serveur Livefyre répond par le nombre de visiteurs du site sur la page qui affichent l’application (défini comme le nombre de visiteurs du site avec un navigateur ouvert à cette page).
1. Le nombre de visiteurs du site sur la page avec l’application s’affiche sur l’application.

Applications qui utilisent cette fonctionnalité :

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Critiques](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatars d’écoute {#section_wcn_kxp_vz}

Le nombre d’écouteurs affiche un maximum de 10 avatars et affiche des avatars uniquement pour les personnes qui ont cliqué **[!UICONTROL Follow]** pour la conversation.

>[!NOTE]
>
>En raison des contraintes d’espace, l’interface mobile affiche uniquement le nombre d’écouteurs et une petite icône "personnes".

Le nombre d’écouteurs Livefyre affiche le nombre de personnes actives sur la page à un moment donné, plus le nombre de personnes qui suivent la conversation. Si un utilisateur se trouve sur la page et suit la conversation, il n’est pas comptabilisé deux fois. Par exemple, si un utilisateur se trouve sur une page et clique **[!UICONTROL Follow]**, le nombre d’écouteurs n’augmente pas ; si l’utilisateur clique alors **[!UICONTROL Unfollow]**, le nombre ne diminue pas.

Applications qui utilisent cette fonctionnalité :

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Critiques](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

