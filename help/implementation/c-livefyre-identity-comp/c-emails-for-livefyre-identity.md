---
title: Courriels pour l’identité Livefyre
description: Courriels pour l’identité Livefyre
exl-id: c8127eef-8fb8-4703-ba34-ef12453f1754
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 1%

---

# Courriers électroniques pour l’identité Livefyre{#emails-for-livefyre-identity}

Livefyre Identity envoie les courriels suivants :

* [Message électronique de réinitialisation de mot de passe](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Courriel de vérification](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Envoyer la vérification par courrier électronique aux utilisateurs](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Courriel de bienvenue](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Envoyer un courriel de bienvenue aux utilisateurs](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Vous pouvez personnaliser l’aspect de tous les courriels d’identité Livefyre dans **[!UICONTROL Integration Settings > Email Notifications.]**

## Message électronique de réinitialisation de mot de passe {#section_nd1_whs_p1b}

Livefyre envoie automatiquement un courrier électronique de réinitialisation de mot de passe lorsqu’un utilisateur tente de réinitialiser son mot de passe.

Le courrier électronique de réinitialisation du mot de passe ressemble à ceci :

**Objet :** Réinitialiser le mot de passe

**Corps :**

Hé, là *&lt;nom d&#39;utilisateur>*,

Une demande de modification du mot de passe de votre profil a été émise sur *&lt;nom du réseau>*.

Si vous l&#39;avez demandé, cliquez sur le lien suivant pour choisir un nouveau mot de passe : *&lt;password reset URL>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>* et  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Courriel de vérification {#section_ak5_xhs_p1b}

Vous pouvez envoyer un courrier électronique vérifiant l’adresse électronique d’un utilisateur. Pour envoyer des courriers électroniques de vérification, vous devez activer l’option dans **Paramètres d’intégration > Identité Livefyre**.

Le courrier électronique de vérification ressemble à ceci :

**Objet : Vérification** par courriel

**Corps :**

Bonjour *&lt;nom_utilisateur>*,

Veuillez cliquer sur le lien suivant (ou coller dans votre navigateur) pour vérifier votre compte : *&lt;URL de vérification>*.

Ce lien expirera dans 24 heures.

Merci,

L&#39;équipe *&lt;nom du client>*

*&lt;username>*,  *&lt;network name=&quot;&quot;>* et  *&lt;verification URL=&quot;&quot;>* sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Envoyer une vérification par courrier électronique aux utilisateurs {#section_vyv_yhs_p1b}

Vous pouvez envoyer un courrier électronique à un utilisateur afin de vérifier l’adresse électronique qu’il utilise pour s’inscrire à un compte. Pour envoyer un courriel de vérification :

1. Dans Studio, cliquez sur l&#39;icône d&#39;engrenage pour modifier les paramètres réseau.
1. Cliquez sur **Paramètres d’intégration > Identité Livefyre.**

1. Accédez à **Types de connexion**.
1. Cliquez sur **Exiger la vérification du courrier électronique** pour envoyer un courrier électronique aux utilisateurs qui vérifie l’adresse électronique qu’ils utilisent pour s’inscrire à un compte.
1. Accédez à **Adresse électronique réseau** pour configurer le **logo de l&#39;adresse électronique**, l&#39;adresse électronique à utiliser comme adresse de l&#39;adresse électronique (**Adresse électronique**) et le nom d&#39;affichage à utiliser pour l&#39;adresse électronique de l&#39;adresse électronique de l&#39;adresse électronique de l&#39;adresse électronique de **.**

## Courriel de bienvenue {#section_z2v_zhs_p1b}

Vous pouvez envoyer un e-mail de bienvenue aux utilisateurs. Pour envoyer des e-mails de bienvenue, vous devez activer l&#39;option **Paramètres d&#39;intégration** > **Identité Livefyre**.

Le courriel de bienvenue ressemble à ceci :

**Objet :** Bienvenue dans  *&lt;customer name=&quot;&quot;>*

**Corps :**

Bonjour *&lt;nom_utilisateur>*,

Un compte a été créé pour vous le *&lt;nom du client>*.

Ce compte a été créé le *&lt;URL de référence>* à partir de l’adresse IP *&lt;Adresse IP>*.

Si vous avez fait cela, vous pouvez ignorer ce courriel en toute sécurité.

Si vous ne l’avez pas fait, veuillez contacter `support@livefyre.com`

Merci

L&#39;équipe *&quot;nom du client&quot;*

*&quot;Nom d’utilisateur&quot;, &quot;nom du client&quot;, &quot;URL de référence&quot;* et &quot;Adresse IP&quot; sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Envoyer un courriel de bienvenue à un utilisateur {#section_kjp_c3s_p1b}

Vous pouvez envoyer un e-mail de bienvenue à un utilisateur après son inscription à un compte. Studio envoie ce courrier électronique après l’envoi d’un courrier électronique de vérification, si vous configurez un courrier électronique de vérification. Pour envoyer un courriel de bienvenue :

1. Dans Studio, cliquez sur l&#39;icône d&#39;engrenage pour modifier les paramètres réseau.
1. Cliquez sur **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Accédez à **[!UICONTROL Email Settings]**.

1. Cliquez sur **[!UICONTROL Send Welcome Emails To New Users]** pour activer l’envoi de courriers électroniques.
1. Accédez à **[!UICONTROL Network Email]** pour configurer le *logo du courriel*, l&#39;adresse électronique à utiliser comme adresse de départ (**Courriel de**) et le nom d&#39;affichage à utiliser pour l&#39;adresse de courriel de départ (**Nom d&#39;affichage du courriel**).
