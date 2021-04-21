---
description: Le nombre d’écouteurs est un compteur qui suit le nombre de visiteurs de site pour une application sur une page et affiche ce nombre.
title: Nombre d’écouteurs
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# Nombre d&#39;écouteurs{#listener-count}

Le nombre d’écouteurs est un compteur qui suit le nombre de visiteurs de site pour une application sur une page et affiche ce nombre.

Le nombre d’écouteurs est le nombre de visiteurs du site pour lesquels un navigateur est ouvert à la page sur laquelle une application est instanciée. Cela vous permet de connaître le nombre de visiteurs du site qui se trouvent sur la page à un moment donné, de sorte que vous pouvez les suivre pendant qu’ils regardent en flux continu ou du contenu en direct en temps réel.

Le nombre d&#39;écouteurs de Livefyre fonctionne comme suit :

1. Le site qui contient votre application envoie un ping sur un serveur Livefyre toutes les 60 secondes.
1. Le serveur Livefyre répond par le nombre de visiteurs du site sur la page qui affiche l’application (défini comme le nombre de visiteurs du site avec un navigateur ouvert à cette page).
1. Le nombre de visiteurs du site sur la page avec l’application s’affiche sur l’application.

Applications qui utilisent cette fonctionnalité :

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Critiques](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatars d&#39;écoute {#section_wcn_kxp_vz}

Le nombre d’écouteurs affiche un maximum de 10 avatars et n’affiche des avatars que pour les personnes qui ont cliqué sur **[!UICONTROL Follow]** pour la conversation.

>[!NOTE]
>
>En raison de contraintes d’espace, l’interface mobile affiche uniquement le nombre d’écouteurs et une petite icône &quot;personnes&quot;.

Le nombre d’écouteurs Livefyre affiche le nombre de personnes qui se trouvent activement sur la page à un moment donné, plus le nombre de personnes qui suivent la conversation. Si une personne se trouve sur la page et suit la conversation, cet utilisateur ne sera pas comptabilisé comme doublon. Par exemple, si un utilisateur se trouve sur une page et clique sur **[!UICONTROL Follow]**, le nombre d’écouteurs n’augmente pas ; si cet utilisateur clique ensuite sur **[!UICONTROL Unfollow]**, le nombre ne diminue pas.

Applications qui utilisent cette fonctionnalité :

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Critiques](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
