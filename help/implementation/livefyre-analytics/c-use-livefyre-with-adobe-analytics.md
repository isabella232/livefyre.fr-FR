---
description: Configurez Adobe Analytics et Dynamic Tag Manager (DTM) pour collecter des données pour les applications Livefyre.
title: Utilisation de Livefyre avec Adobe Analytics et Dynamic Tag Manager (DTM)
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 1%

---

# Utilisation de Livefyre avec Adobe Analytics et Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configurez Adobe Analytics et Dynamic Tag Manager (DTM) pour collecter des données pour les applications Livefyre.

## Étape 1 : Configuration des événements dans Adobe Analytics {#section_iks_kgd_4cb}

Mappage des événements Livefyre à un ou plusieurs événements de succès personnalisés dans le Gestionnaire de suites de rapports Adobe Analytics.

Pour plus d’informations sur le Gestionnaire de suites de rapports, voir [Gestionnaire de suites de rapports](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en).

1. Connectez-vous à Adobe Analytics en tant qu’utilisateur administrateur.
1. Ouvrez le Gestionnaire de suites de rapports d’administration Adobe Analytics.
1. Créez une suite de rapports ou sélectionnez-en une existante.
1. Modifiez la suite de rapports en cliquant sur la suite de rapports à modifier, puis accédez à **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Faites correspondre les événements Livefyre à un ou plusieurs événements de succès personnalisés.

## Étape 2 : Configuration des variables de conversion

Mappez les variables de conversion Livefyre (eVars) aux variables de conversion dans le Gestionnaire de suites de rapports d’administration d’Adobe Analytics. Les variables de conversion agissent comme une fonction de tri pour déterminer la manière dont vous prévoyez d’identifier les données collectées à partir des événements Livefyre.

1. Dans le Gestionnaire de suites de rapports, cliquez sur **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Sélectionnez les variables de conversion personnalisées (eVars) à utiliser et mappez-les aux variables de conversion Livefyre. Pour mapper une variable de conversion Livefyre à une variable de conversion personnalisée :

   * Activation de la variable de conversion
   * Nommer la variable de conversion
   * Attribuer un type à la variable de conversion

1. Enregistrez les variables de conversion personnalisées.

## Étape 3 : Utilisation de la gestion dynamique des balises pour ajouter votre suite de rapports à des événements Livefyre {#section_t15_2hd_4cb}

Utilisez les balises pour intégrer Analytics aux événements Livefyre. Pour ce faire, créez une propriété et un outil, puis ajoutez la nouvelle suite de rapports avec les événements Livefyre à la propriété . Pour plus d’informations, voir [Présentation des balises](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).

Vous n’avez pas besoin d’effectuer cette étape si une propriété ou un outil est déjà configuré pour la suite de rapports que vous avez configurée avec les événements Livefyre.

1. Dans la gestion dynamique des balises, créez ou modifiez une propriété existante.
1. Créez ou modifiez un outil Adobe Analytics existant.
1. Si aucun outil Adobe Analytics n’existe, cliquez sur le bouton **[!UICONTROL Add a Tool]**.
Définissez les paramètres suivants pour l’outil :

   * Définissez **[!UICONTROL Tool Type]** sur **[!UICONTROL Adobe Analytics]**.
   * Activer **[!UICONTROL Automatic Configuration]**.
   * Activer **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Ajoutez ou confirmez le nom de la suite de rapports avec les événements Livefyre dans le champ **[!UICONTROL Report Suites]**.

## Étape 4 : Configuration d’une règle de chargement de page pour configurer la gestion des analyses {#section_jfj_j3d_4cb}

Configurez une règle de chargement de page pour extraire toutes les données. La règle de chargement de page vous permet de placer du code JavaScript personnalisé dans la règle qui enregistre l’événement au chargement de la page.

>[!NOTE]
>
>N’utilisez pas de règles basées sur un événement ni de règles d’appel direct.

1. Dans DTM, sélectionnez l’onglet **[!UICONTROL Rules]** .
1. Cliquez sur **[!UICONTROL Page Load Rules]**.
1. Cliquez sur le bouton **[!UICONTROL Create New Rule]** .
1. Ouvrez la section **[!UICONTROL Conditions]** en cliquant sur le bouton **[!UICONTROL Plus]** .
1. Déclenchez la règle. Choisissez les types de déclencheur **[!UICONTROL DOM Ready]** ou **[!UICONTROL Onload]** si vous souhaitez retarder ou mettre en oeuvre la règle de manière asynchrone.
1. (Facultatif) Ajoutez des paramètres supplémentaires pour limiter les pages qui affichent les applications Livefyre. Pour plus d’informations sur les options de configuration supplémentaires, voir [Présentation des balises](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).
1. Sous **[!UICONTROL Javascript/ Third Party Tags]**, cliquez sur l’onglet **[!UICONTROL Non-sequential]**, puis sur **[!UICONTROL Add New Script]**.
1. Sélectionnez **[!UICONTROL Sequential HTML]** comme type de script.
1. Ajoutez le script suivant dans l’éditeur de code et cliquez sur **[!UICONTROL Save Code]**.

   Le script suivant appelle la règle d’appel direct `livefyre_analytics` après le chargement du code JavaScript Livefyre. L’exemple de script suivant vérifie toutes les 400 ms si `livefyre.analytics` se trouve sur la page. Une fois la page chargée, livefyre.analytics envoie les informations de suivi.

   ```
   /**
   * Poll for Livefyre.analytics object to exist since it gets loaded via the
   * Livefyre.js JavaScript file. Depending on the timing, this could already
   * exist or need a little time.
   */
   function pollForAnalytics() {
   if (Livefyre.analytics) {
     _satellite.track('livefyre_analytics');
       return true;
     }
     setTimeout(pollForAnalytics, 400);
   }
   setTimeout(pollForAnalytics, 400);
   ```

1. Cliquez sur **[!UICONTROL Save Code]**.
1. Cliquez sur **[!UICONTROL Save Rule]**.

## Étape 5 : Création d’une règle d’appel direct pour créer la configuration de mappage Adobe Analytics pour Livefyre {#section_gvp_b1g_pdb}

Il existe d’autres façons d’implémenter Livefyre avec la gestion dynamique des balises en utilisant des événements personnalisés, des champs d’interface utilisateur Adobe Analytics dans la gestion dynamique des balises et des éléments de données. Ce document utilise du code JavaScript personnalisé pour obtenir le même résultat.

1. Dans la gestion dynamique des balises, sélectionnez l’onglet **Règles**, puis cliquez sur **Règles d’appel direct**.
1. Cliquez sur le bouton **Créer une règle** .
1. Nommez la nouvelle règle **Livefyre Analytics**.
1. Développez la zone de configuration **conditions** .
1. Dans le champ **Chaîne**, saisissez `livefyre_analytics`.
1. Développez la section JavaScript / Balise tierce et cliquez sur le bouton **Ajouter un nouveau script** .
1. Saisissez **Livefyre Analytics Config** dans la zone de saisie **Nom de balise**.
1. Sélectionnez **Javascript Non Séquentiel**.
1. Saisissez le code de configuration Livefyre suivant dans l’éditeur de code, puis cliquez sur le bouton **Enregistrer le code** .

   ```
   var s = _satellite.getToolsByType('sc')[0].getS();
   
   var evarMap = {
     appId: 'eVar81',
     appType: 'eVar82'
   };
   
   var eventMap = {
     FlagCancel: 'event82',
     FlagClick: 'event82',
     FlagDisagree: 'event82',
     FlagOffensive: 'event82',
     FlagOffTopic: 'event82',
     FlagSpam: 'event82',
     Like: 'event82',
     Load: 'event81',
     RequestMore: 'event82',
     ShareButtonClick: 'event82',
     ShareFacebook: 'event82',
     ShareOnPostClick: 'event82',
     ShareTwitter: 'event82',
     ShareURL: 'event82',
     SortStream: 'event82',
     TwitterLikeClick: 'event82',
     TwitterReplyClick: 'event82',
     TwitterRetweetClick: 'event82',
     TwitterUserFollow: 'event82'
   };
   
    function trackLivefyreEvent(data) {
     var event = eventMap[data.type];
     console.log('Track:', data.type, event);
   
     if (!event) {
       console.warn(data.type, 'is not mapped   to an event in AA');
       return;
     }
     var vars = ['events'];
     switch (event) {
       case 'event82': s.eVar83 = data.type;
         vars.push('eVar83');
         break;
       default:
     }
       ['generator', 'evars'].forEach(function (type) {
       var obj = data[type];
       for (var d in obj) {
         if (obj.hasOwnProperty(d) && evarMap[d]) {
           s[evarMap[d]] = obj[d];
           vars.push(evarMap[d]);
         }
       }
     });
     s.linkTrackVars = vars.join(',');
     s.linkTrackEvents = event;
     s.events = event;
   
     console.log('linkTrackVars:',  s.linkTrackVars);
     console.log('linkTrackEvents:',  s.linkTrackEvents);
     console.log('events:', s.events);
     s.tl();
     }
     ]
   
     /**
   ```

   * Ajoute un gestionnaire d’analyse pour tous les événements d’analyse de Livefyre. Pour chaque événement, il définit les données sur un objet global, puis répartit l’événement.

   ```
   */
   function addAnalyticsHandler() {
     Livefyre.analytics.addHandler(function (events) {
       (events || []).forEach(function (data) {
         console.log('Event handled:', data.type);
         trackLivefyreEvent(data);
       });
     });
   }
   addAnalyticsHandler();
   ```

1. Cliquez sur **Enregistrer la règle**.

## Étape 6 : Approbation des modifications de la règle de chargement de page {#section_pxc_11t_ycb}

1. Accédez à l’onglet **[!UICONTROL Approvals]** .
1. Cliquez sur **[!UICONTROL Approve]**.
1. Cliquez sur **[!UICONTROL Yes, approve]** pour confirmer votre approbation.
1. Atteindre **[!UICONTROL Overview > Publish Queue]**.
1. Sélectionnez la règle à publier.
1. Cliquez sur **[!UICONTROL Publish Selected]**.
1. Cliquez sur **[!UICONTROL Publish]** pour confirmer que vous souhaitez publier.

## Script {#section_xkb_vft_mcb}

L’exemple de code suivant mappe les eVars spécifiques aux eVars Livefyre disponibles. Le nom de la variable de conversion Livefyre ( `eVar`) (par exemple, `appId`) correspond au nom que vous avez configuré dans le Gestionnaire de suites de rapports (par exemple, `eVar81`). Remplacez les noms `eVar` de ce script par les variables de conversion personnalisées.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {
  appId: 'eVar81',
  appType: 'eVar82'
};
```

L’exemple de code suivant mappe les événements spécifiques que vous configurez dans le Gestionnaire de suites de rapports avec les événements Livefyre disponibles. Dans cet exemple, `event82` est configuré comme tout événement d’interaction utilisateur sans différencier le type d’événement d’interaction utilisateur (par exemple, aimer ou partager du contenu). Il s’agit d’un moyen efficace d’enregistrer toutes les informations d’interaction de l’utilisateur dans un bloc. Vous pouvez également mapper les événements dans l’interface utilisateur de DTM Analytics avec le référencement des éléments de données.

```
var eventMap = {
  FlagCancel: 'event82',
  FlagClick: 'event82',
  FlagDisagree: 'event82',
  FlagOffensive: 'event82',
  FlagOffTopic: 'event82',
  FlagSpam: 'event82',
  Like: 'event82',
  Load: 'event81',
  RequestMore: 'event82',
  ShareButtonClick: 'event82',
  ShareFacebook: 'event82',
  ShareOnPostClick: 'event82',
  ShareTwitter: 'event82',
  ShareURL: 'event82',
  SortStream: 'event82',
  TwitterLikeClick: 'event82',
  TwitterReplyClick: 'event82',
  TwitterRetweetClick: 'event82',
  TwitterUserFollow: 'event82'
};
```

L’exemple suivant indique que s’il n’y a pas d’événement dans cette liste, ne faites rien. Vous n’avez pas besoin de modifier cette section de code.

```
function trackLivefyreEvent(data) {
  var event = eventMap[data.type];
  console.log('Track:', data.type, event);

  if (!event) {
    console.warn(data.type, 'is not mapped to an event in AA');
    return;
  }
```

Le code suivant différencie les types d’événements enregistrés par `event82`. La variable de conversion `eVar83` enregistre le type d’interaction de l’utilisateur, et le script configure `eVar83` pour séparer les données d’interaction de l’utilisateur par type. `eVar83` vous permet donc de ventiler les données enregistrées en types spécifiques d’interactions utilisateur.

```
  var vars = ['events'];
  switch (event) {
    case 'event82': s.eVar83 = data.type;
      vars.push('eVar83');
      break;
    default:
  }

  ['generator', 'evars'].forEach(function (type) {
    var obj = data[type];
    for (var d in obj) {
      if (obj.hasOwnProperty(d) && evarMap[d]) {
        s[evarMap[d]] = obj[d];
        vars.push(evarMap[d]);
      }
    }
  });

  s.linkTrackVars = vars.join(',');
  s.linkTrackEvents = event;
  s.events = event;

  console.log('linkTrackVars:', s.linkTrackVars);
  console.log('linkTrackEvents:', s.linkTrackEvents);
  console.log('events:', s.events);

  s.tl();
}
```

L’exemple de code suivant ajoute un gestionnaire pour écouter tous les événements qui se produisent. Il utilise la règle de chargement de page au chargement, attend que des événements existent, puis configure un gestionnaire pour tous les événements de l’application et effectue le suivi de ces événements. Vous n’avez pas besoin de modifier ce code.

```
/**
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event.
*/
function addAnalyticsHandler() {
  Livefyre.analytics.addHandler(function (events) {
    (events || []).forEach(function (data) {
      console.log('Event handled:', data.type);
      trackLivefyreEvent(data);
    });
  });
}
```

## Plus d’infos

Pour plus d’informations sur les sujets abordés sur cette page, voir :

* [Gestionnaire de suites de rapports](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)
* [Présentation des balises](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
