---
description: Exécutez des tests de contraintes par rapport à la plate-forme Livefyre.
seo-description: Exécutez des tests de contraintes par rapport à la plate-forme Livefyre.
seo-title: Stratégie de test de contraintes
solution: Experience Manager
title: Stratégie de test de contraintes
uuid: f 2 d 49 b 55-f 4 fc -485 f -9 aea-a 17 ce 64813 ee
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Stratégie de test de contraintes{#stress-test-policy}

Exécutez des tests de contraintes par rapport à la plate-forme Livefyre.

Ce document décrit l'exécution des tests de contraintes par rapport à la plate-forme Livefyre. Les tests ad hoc effectués par les clients sans notification sont strictement interdits. Pour plus d'informations sur [les activités interdites et autorisées](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Les tests de contraintes sont facultatifs. Vous n'avez pas besoin d'effectuer un test de contraintes ou ne l'avez pas prévu. Adobe Livefyre effectue des tests et des validations de contraintes régulières dans le cadre du processus de publication. Si vous choisissez d'exécuter des tests, ce document décrit les exigences et les contraintes liées à la réalisation des tests de contraintes.

## Notification {#section_ihs_bfz_vdb}

Vous devez informer votre spécialiste de succès Livefyre et votre conseiller technique Adobe de vos tests planifiés de trois semaines ou plus avant de commencer à démarrer.

Pour avertir Livefyre, envoyez les informations suivantes à votre spécialiste de succès client Livefyre et à votre consultant technique Adobe :

* Objectif et description du test
* Cas d'utilisation que vous testez par rapport à
* Liste des API Livefyre que vous prévoyez d'utiliser dans le test
* Date, heure et durée du test
* Adresses IP à partir desquelles vous lancerez les tests

## Conditions requises {#section_khs_bfz_vdb}

Vous pouvez effectuer des tests uniquement s'ils satisfont aux exigences suivantes :

* Vous devez recevoir une approbation explicite écrite d'un consultant technique Adobe 3 semaines ou plus avant de commencer le test.
* **Vous pouvez uniquement effectuer des tests sur le réseau UAT.**
* Vous devez tester les scénarios réalistes. Par exemple, vous ne supposez pas que votre propriété génère *quotidiennement des millions* de requêtes de publication, car ce scénario n'est pas réaliste. Si vous avez besoin d'aide pour déterminer si votre scénario est réaliste ou non, demandez à votre spécialiste de succès Livefyre ou à votre consultant technique Adobe.
* Les tests doivent être effectués pendant les heures ouvrées du fuseau horaire du Pacifique\ (UTC -7\).
* Vous devrez peut-être produire des données et votre raisonnement pour le test.

## Gouvernance {#section_mhs_bfz_vdb}

Livefyre se réserve le droit d'interrompre un test à tout moment si vous effectuez un test :

* Sur le réseau Production.
* Sans approbation explicite, écrite par un consultant technique Adobe trois semaines ou plus à l'avance.
* Par rapport aux scénarios inréels.

Livefyre termine les tests en bloquant l'accès aux API, en désactivant Livefyre Networks et en refusant une demande de test de charge s'il ne satisfait pas aux exigences.
