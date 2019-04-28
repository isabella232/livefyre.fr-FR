---
description: Le nombre d'écouteurs est un compteur qui suit le nombre de visiteurs du site pour une application sur une page et affiche ce nombre.
seo-description: Le nombre d'écouteurs est un compteur qui suit le nombre de visiteurs du site pour une application sur une page et affiche ce nombre.
seo-title: Nombre d'écouteurs
solution: Experience Manager
title: Nombre d'écouteurs
uuid: fdd 7 cfe 4-ae 69-4 d 31-baa 2-8978368 fc 3 e 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Nombre d&#39;écouteurs{#listener-count}

Le nombre d&#39;écouteurs est un compteur qui suit le nombre de visiteurs du site pour une application sur une page et affiche ce nombre.

Le nombre d&#39;écouteurs est le nombre de visiteurs du site qui disposent d&#39;un navigateur ouvert sur la page sur laquelle est instanciée une application. Vous pouvez ainsi connaître le nombre de visiteurs du site qui se trouvent sur la page à un moment donné, afin que vous puissiez les suivre pendant qu&#39;ils regardent le contenu en flux continu ou en direct en réel.

Le nombre d&#39;écouteurs de Livefyre fonctionne comme suit :

1. Site contenant votre application sur un serveur Livefyre toutes les 60 secondes.
1. Le serveur Livefyre répond avec le nombre de visiteurs du site sur la page qui affiche l&#39;application (défini comme le nombre de visiteurs du site avec un navigateur ouvert sur cette page).
1. Le nombre de visiteurs du site sur la page avec l&#39;application s&#39;affiche sur l&#39;application.

Applications utilisant cette fonctionnalité :

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Révisions](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatars d&#39;écouteur {#section_wcn_kxp_vz}

Le nombre d&#39;écouteurs affiche un maximum de 10 avatars et affiche des avatars uniquement pour les personnes qui ont cliqué **[!UICONTROL Follow]** pour la conversation.

>[!NOTE]
>
>En raison des contraintes d&#39;espace, l&#39;interface mobile affiche uniquement le nombre d&#39;écouteurs et une petite icône « people ».

Le nombre d&#39;écouteurs Livefyre affiche le nombre de personnes actives sur la page à un moment donné, plus le nombre de personnes qui suivent la conversation. Si une personne se trouve sur la page et après la conversation, cet utilisateur n&#39;est pas comptabilisé deux fois. Par exemple, si un utilisateur se trouve sur une page et clique **[!UICONTROL Follow]** sur, le nombre d&#39;écouteurs n&#39;augmente pas ; si cet utilisateur clique **[!UICONTROL Unfollow]** ensuite sur, le nombre ne diminue pas.

Applications utilisant cette fonctionnalité :

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commentaires](/help/using/c-about-apps/c-comments/c-comments.md)
* [Révisions](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

