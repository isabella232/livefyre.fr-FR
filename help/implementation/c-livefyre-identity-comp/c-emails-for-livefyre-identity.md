---
description: valeur nulle
seo-description: valeur nulle
seo-title: Emails for Livefyre Identity
solution: Experience Manager
title: Emails for Livefyre Identity
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Emails for Livefyre Identity{#emails-for-livefyre-identity}

Livefyre Identity envoie les courriers électroniques suivants :

* [Password Reset Email](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Verification Email](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Envoyer la vérification par courrier électronique aux utilisateurs](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Courriel de bienvenue](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Send Welcome Email to Users](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Vous pouvez personnaliser l’apparence de tous les courriers électroniques d’identité de Livefyre dans **[!UICONTROL Integration Settings > Email Notifications.]**

## Courrier électronique de réinitialisation de mot de passe {#section_nd1_whs_p1b}

Livefyre envoie automatiquement un courrier électronique de réinitialisation de mot de passe lorsqu’un utilisateur tente de réinitialiser son mot de passe.

Le courrier électronique de réinitialisation du mot de passe se présente comme suit :

**** Objet: Réinitialiser le mot de passe

**Corps :**

Hé, *&lt;nom d'utilisateur&gt;*,

Une demande de modification du mot de passe de votre profil a eu lieu sur *&lt;nom du réseau&gt;*.

Si vous l’avez demandé, cliquez sur le lien suivant pour choisir un nouveau mot de passe : *&lt;password reset URL&gt;*.

*&lt;Username&gt;, &lt;network name&gt;, and &lt;password reset URL&gt; are all dynamically generated based on the site visitor and your network.*****

## E-mail de vérification {#section_ak5_xhs_p1b}

You can send an email verifying the email address of a user. Pour envoyer des courriers électroniques de vérification, vous devez activer l’option dans Paramètres **d’intégration &gt; Identité** Livefyre.

Le courrier électronique de vérification ressemble à ceci :

**** Objet: Vérification par courrier électronique

**Corps :**

Bonjour *&lt;nom_utilisateur&gt;*,

Veuillez cliquer sur le lien suivant (ou coller dans votre navigateur) pour vérifier votre compte : *&lt;URL de vérification&gt;*.

Ce lien expirera dans 24 heures.

Merci,

L’équipe *&lt;nom du client&gt;*

*&lt;Nom d’utilisateur&gt;*, *&lt;nom du réseau&gt;* et *&lt;URL de vérification&gt;* sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Envoyer une vérification par courrier électronique aux utilisateurs {#section_vyv_yhs_p1b}

Vous pouvez envoyer un courrier électronique à un utilisateur afin de vérifier l’adresse électronique qu’il utilise pour s’inscrire à un compte. Pour envoyer un courrier électronique de vérification :

1. Dans Studio, cliquez sur l'icône d'engrenage pour modifier les paramètres réseau.
1. Cliquez sur Paramètres **d’intégration &gt; Identité Livefyre.**

1. Accédez à Types de **connexion**.
1. Cliquez sur **Exiger une vérification** par courrier électronique pour envoyer un courrier électronique aux utilisateurs qui vérifie l’adresse électronique qu’ils utilisent pour s’inscrire à un compte.
1. Accédez à Courriel **** réseau pour configurer le **logo du courriel**, l’adresse électronique à utiliser comme adresse de départ (**E-mail de**) et le nom d’affichage à utiliser pour l’adresse de départ (Nom d’affichage du **courriel).**

## Courriel de bienvenue {#section_z2v_zhs_p1b}

Vous pouvez envoyer un e-mail de bienvenue aux utilisateurs. Pour envoyer des courriers électroniques de bienvenue, vous devez activer l’option dans Paramètres **d’** intégration &gt; Identité **** Livefyre.

Le message de bienvenue ressemble à ceci :

**** Subject: Welcome to &lt;customer name&gt;**

**Corps :**

Hello &lt;username&gt;,**

An account was created for you on &lt;customer name&gt;.**

This account was created on &lt;referral URL&gt; from IP address &lt;IP Address&gt;.****

If you did this, you can safely disregard this email.

If you didn’t do this, please contact `support@livefyre.com`

Merci

The "customer name" Team **

*"Username", "customer name", "referral URL", and "IP Address" are all dynamically generated based on the site visitor and your network.*

## Send a Welcome Email to a User {#section_kjp_c3s_p1b}

You can send a welcome email to a user after they sign up for an account. Studio sends this email after it sends a verification email, if you set up a verification email. To send a welcome email:

1. In Studio, click on the gear icon to modify network settings.
1. Cliquez sur **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Accédez à **[!UICONTROL Email Settings]**.

1. Cliquez sur **[!UICONTROL Send Welcome Emails To New Users]** pour activer l’envoi de courriers électroniques.
1. Accédez à **[!UICONTROL Network Email]** la configuration du *logo pour le courrier électronique*, de l’adresse électronique à utiliser comme adresse de départ (**Courriel de**) et du nom d’affichage à utiliser pour l’adresse de courriel de départ (Nom **d’affichage du** courrier électronique).
