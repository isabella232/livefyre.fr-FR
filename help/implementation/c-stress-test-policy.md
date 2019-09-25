---
description: Exécutez des tests de résistance contre la plateforme Livefyre.
seo-description: Exécutez des tests de résistance contre la plateforme Livefyre.
seo-title: Stratégie de test de stress
solution: Experience Manager
title: Stratégie de test de stress
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Stratégie de test de stress{#stress-test-policy}

Exécutez des tests de résistance contre la plateforme Livefyre.

Ce document fournit des conseils sur l'exécution de tests de résistance contre la plateforme Livefyre. Les tests ad hoc effectués par les clients sans notification sont strictement interdits. Pour en savoir plus sur les activités [autorisées et](#c_stress_test_policy/section_mhs_bfz_vdb)interdites.

>[!NOTE]
>
>Les tests de résistance sont facultatifs. Vous n’êtes pas tenu ou attendu d’effectuer un test de stress. Adobe Livefyre effectue régulièrement des tests de résistance et des validations dans le cadre du processus de publication. Si vous choisissez d’exécuter des tests, ce document décrit les exigences et les contraintes liées à la réalisation des tests de résistance.

## Notification {#section_ihs_bfz_vdb}

Vous devez informer votre spécialiste de la réussite client Livefyre et votre consultant technique Adobe de vos tests planifiés trois semaines ou plus avant le début de votre projet.

Pour avertir Livefyre, envoyez les informations suivantes à votre spécialiste du succès client Livefyre et à votre consultant technique Adobe :

* Objet et description de l'essai
* Le cas d’utilisation que vous testez
* Liste des API Livefyre que vous prévoyez d’utiliser dans le test
* Date, heure et durée du test
* Adresses IP à partir desquelles vous allez lancer les tests

## Conditions requises {#section_khs_bfz_vdb}

Vous ne pouvez effectuer des tests que s’ils répondent aux exigences suivantes :

* Vous devez recevoir l’approbation écrite explicite d’un conseiller technique Adobe 3 semaines ou plus avant de commencer le test.
* **Vous pouvez uniquement effectuer des tests sur le réseau UAT.**
* Vous devez tester par rapport à des scénarios réalistes. Par exemple, vous ne pouvez pas supposer que votre propriété répondra à *des millions* de demandes de publication chaque jour, car il ne s’agit pas d’un scénario réaliste. Si vous avez besoin d’aide pour déterminer si votre scénario est réaliste ou non, adressez-vous à votre spécialiste du succès client Livefyre ou à votre consultant technique Adobe.
* Les essais doivent être effectués pendant les heures de bureau pour le fuseau horaire standard du Pacifique \(UTC -7\).
* Vous devrez peut-être produire des données et expliquer votre raisonnement pour le test.

## Gouvernance {#section_mhs_bfz_vdb}

Livefyre se réserve le droit de terminer un test à tout moment si vous effectuez un test :

* Sur le réseau de production.
* Sans l’autorisation écrite explicite d’un conseiller technique Adobe trois semaines ou plus à l’avance.
* Contre des scénarios irréalistes.

Livefyre met fin aux tests en bloquant l’accès aux API, en désactivant Livefyre Networks et en refusant une demande de test de charge si elle ne satisfait pas aux exigences.
