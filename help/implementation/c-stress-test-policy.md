---
description: Exécutez des tests de résistance sur la plate-forme Livefyre.
title: Stratégie de test de stress
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Stratégie de test de stress{#stress-test-policy}

Exécutez des tests de résistance sur la plate-forme Livefyre.

Ce document fournit des conseils sur l&#39;exécution de tests de résistance sur la plateforme Livefyre. Les tests ad hoc effectués par les clients sans notification sont strictement interdits. Pour en savoir plus sur [les activités interdites et autorisées](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Les tests de stress sont facultatifs. Vous n&#39;êtes pas tenu ou prévu d&#39;effectuer un test de résistance. L&#39;Adobe Livefyre effectue régulièrement des tests de résistance et des validations dans le cadre du processus de publication. Si vous choisissez d&#39;exécuter des tests, ce document décrit les exigences et les contraintes liées à la réalisation de tests de résistance.

## Notification {#section_ihs_bfz_vdb}

Vous devez aviser votre spécialiste de la réussite client et votre consultant technique en Adobe Livefyre de vos tests planifiés trois semaines ou plus avant le début.

Pour aviser Livefyre, envoyez les informations suivantes à votre spécialiste du succès client Livefyre et à votre consultant technique en Adobe :

* Objet et description de l&#39;essai
* Le cas d’utilisation que vous testez
* Liste des API Livefyre que vous prévoyez d’utiliser dans le test
* Date, heure et durée du test
* Adresses IP à partir desquelles vous allez lancer les tests

## Conditions requises {#section_khs_bfz_vdb}

Vous ne pouvez effectuer des tests que s’ils satisfont aux exigences suivantes :

* Vous devez recevoir l&#39;approbation explicite et écrite d&#39;un conseiller technique Adobe 3 semaines ou plus avant de commencer le test.
* **Vous pouvez uniquement effectuer des tests sur le réseau UAT.**
* Vous devez tester par rapport à des scénarios réalistes. Par exemple, vous ne pouvez pas présumer que votre propriété traitera *des millions* de demandes de publication chaque jour, car il ne s’agit pas d’un scénario réaliste. Si vous avez besoin d&#39;aide pour déterminer si votre scénario est réaliste ou non, demandez à votre spécialiste de la réussite client Livefyre ou à votre consultant technique en Adobe.
* Les essais doivent être effectués pendant les heures d&#39;ouverture pour le fuseau horaire standard du Pacifique \(UTC -7\).
* Vous devrez peut-être produire des données et expliquer le test.

## Gouvernance {#section_mhs_bfz_vdb}

Livefyre se réserve le droit de terminer un test à tout moment si vous effectuez un test :

* Sur le réseau de production.
* Sans l&#39;approbation explicite et écrite d&#39;un conseiller technique Adobe trois semaines ou plus à l&#39;avance.
* Contre des scénarios irréalistes.

Livefyre termine les tests en bloquant l&#39;accès aux API, en désactivant Livefyre Networks et en refusant une demande de test de charge si elle ne répond pas aux exigences.
