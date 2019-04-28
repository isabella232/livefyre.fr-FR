---
description: valeur nulle
seo-description: valeur nulle
seo-title: Courriels pour Livefyre Identité
solution: Experience Manager
title: Courriels pour Livefyre Identité
uuid: 4 e 807803-687 e -4 df 0-94 d 1-b 18 a 48 d 024 e 8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Courriels pour Livefyre Identité{#emails-for-livefyre-identity}

Livefyre Identity envoie les courriers électroniques suivants :

* [Adresse électronique de réinitialisation du mot de passe](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Adresse électronique de vérification](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Envoyer la vérification de courrier électronique pour les utilisateurs](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Courriel de bienvenue](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Envoyer un courriel de bienvenue aux utilisateurs](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Vous pouvez personnaliser l&#39;aspect de tous les courriers électroniques d&#39;identité Livefyre dans **[!UICONTROL Integration Settings > Email Notifications.]**

## Adresse électronique de réinitialisation du mot de passe {#section_nd1_whs_p1b}

Livefyre envoie automatiquement un courrier électronique de réinitialisation du mot de passe lorsqu&#39;un utilisateur tente de réinitialiser son mot de passe.

L&#39;adresse électronique de réinitialisation du mot de passe ressemble à ceci :

**Objet :** Réinitialiser le mot de passe

**Corps :**

Hey there *&lt; username &gt;*,

Une demande de modification du mot de passe de votre profil a été effectuée sur *&lt; nom du réseau &gt;*.

Si vous l&#39;avez demandé, cliquez sur le lien suivant pour choisir un nouveau mot de passe : *&lt; URL de réinitialisation du mot de passe &gt;*.

*&lt; Nom d&#39;utilisateur &gt;*, *&lt; nom du réseau &gt;*et *&lt; URL de réinitialisation du mot de passe &gt;* sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Adresse électronique de vérification {#section_ak5_xhs_p1b}

Vous pouvez envoyer un courriel vérifiant l&#39;adresse électronique d&#39;un utilisateur. Pour envoyer des courriers électroniques de vérification, vous devez activer l&#39;option dans **Paramètres d&#39;intégration &gt; Identité Livefyre**.

L&#39;adresse électronique de vérification ressemble à ceci :

**Objet :** Vérification de courrier électronique

**Corps :**

Hello *&lt; username &gt;*,

Cliquez sur le lien suivant (ou collez-le dans votre navigateur) pour vérifier votre compte : *&lt; URL de vérification &gt;*.

Ce lien expirera dans 24 heures.

Merci,

The *&lt;customer name&gt;* Team

*&lt; Nom d&#39;utilisateur &gt;*, *&lt; nom du réseau &gt;*et *&lt; URL de vérification &gt;* sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Envoi d&#39;une vérification par courrier électronique aux utilisateurs {#section_vyv_yhs_p1b}

Vous pouvez envoyer un courrier électronique à un utilisateur pour vérifier l&#39;adresse électronique qu&#39;il utilise pour s&#39;inscrire à un compte. Pour envoyer un courriel de vérification :

1. Dans Studio, cliquez sur l&#39;icône représentant un engrenage pour modifier les paramètres réseau.
1. Cliquez sur **Paramètres d&#39;intégration &gt; Identité Livefyre.**

1. Accédez aux types **de connexion**.
1. Cliquez **sur Exiger la vérification de courriel** pour envoyer un courrier électronique aux utilisateurs qui vérifient l&#39;adresse électronique qu&#39;ils utilisent pour s&#39;inscrire à un compte.
1. Accédez à Courriel **réseau** pour configurer **le logo pour le courrier électronique**, l&#39;adresse électronique à utiliser comme adresse électronique (**adresse électronique de)** et le nom d&#39;affichage à utiliser pour l&#39;adresse électronique de l&#39;expéditeur (**nom d&#39;affichage de courriel**).

## Courriel de bienvenue {#section_z2v_zhs_p1b}

Vous pouvez envoyer un courriel de bienvenue aux utilisateurs. Pour envoyer des e-mails de bienvenue, vous devez activer l&#39;option dans **Paramètres d&#39;intégration** &gt; **Identité Livefyre**.

L&#39;e-mail de bienvenue ressemble à ceci :

**Objet :** Bienvenue dans *&lt; nom du client &gt;*

**Corps :**

Hello *&lt; username &gt;*,

Un compte a été créé pour vous sur *&lt; nom du client &gt;*.

Ce compte a été créé sur *&lt; URL de référence &gt;* depuis l&#39;adresse IP *&lt; adresse IP &gt;*.

Dans ce cas, vous pouvez ignorer ce message en toute sécurité.

Si vous n&#39;avez pas effectué cette opération, veuillez contacter `support@livefyre.com`

Merci

The *&quot;customer name&quot;* Team

*« Nom d&#39;utilisateur », « Nom du client », « URL de référence »* et « Adresse IP » sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Envoyer un courriel de bienvenue à un utilisateur {#section_kjp_c3s_p1b}

Vous pouvez envoyer un courriel de bienvenue à un utilisateur après l&#39;avoir inscrit à un compte. Studio envoie ce courrier électronique après l&#39;envoi d&#39;un courrier électronique de vérification, si vous avez configuré un courrier électronique de vérification. Pour envoyer un courriel de bienvenue :

1. Dans Studio, cliquez sur l&#39;icône représentant un engrenage pour modifier les paramètres réseau.
1. Cliquez sur **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Accédez **[!UICONTROL Email Settings]**à.

1. Cliquez sur **[!UICONTROL Send Welcome Emails To New Users]** pour envoyer des courriers électroniques.
1. Accédez au **[!UICONTROL Network Email]***logo pour le courrier électronique*, à l&#39;adresse électronique à utiliser comme adresse d&#39;expéditeur (**adresse électronique de)** et au nom d&#39;affichage à utiliser pour l&#39;adresse électronique de l&#39;expéditeur (**nom d&#39;affichage de courriel**).
