---
description: valeur nulle
seo-description: valeur nulle
seo-title: Utilisation de Livefyre avec Adobe Analytics et le gestionnaire dynamique de balises (DTM) lk xavvn vefyre avec Adobe Analytics et Dynamic Tag Manager (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# Utilisation de Livefyre avec Adobe Analytics et Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configurez Adobe Analytics et Dynamic Tag Manager (DTM) pour collecter des données pour les applications Livefyre.

## Étape 1 : Configuration d’événements dans Adobe Analytics {#section_iks_kgd_4cb}

Faites correspondre les événements Livefyre à un ou plusieurs événements de réussite personnalisés dans le Gestionnaire de Report Suites d’Adobe Analytics.

Pour plus d’informations sur le Gestionnaire de Report Suites, voir Gestionnaire [](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)de Report Suites.

1. Connectez-vous à Adobe Analytics en tant qu’utilisateur administrateur.
1. Ouvrez le Gestionnaire de Report Suites d’administration d’Adobe Analytics.
1. Créez une suite de rapports ou choisissez une suite existante.
1. Modifiez la suite de rapports en cliquant sur la suite de rapports à modifier, puis accédez à **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Faites correspondre les événements Livefyre à un ou plusieurs événements de réussite personnalisés.

## Étape 2 : Configuration des variables de conversion

Faites correspondre les variables de conversion Livefyre (eVars) aux variables de conversion dans le Gestionnaire de Report Suites d’administration d’Adobe Analytics. Les variables de conversion se comportent comme une fonction de tri pour déterminer comment vous prévoyez d’identifier les données collectées à partir des événements Livefyre.

1. Dans le Gestionnaire de Report Suites, cliquez sur **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Sélectionnez les variables de conversion personnalisées (eVars) à utiliser et faites-les correspondre aux variables de conversion Livefyre. Pour mapper une variable de conversion Livefyre à une variable de conversion personnalisée :
* Activation de la variable de conversion
* Nommer la variable de conversion
* Attribuer un type à la variable de conversion
1. Enregistrez les variables de conversion personnalisées.

## Étape 3 : Utilisation de la gestion dynamique des balises pour ajouter votre suite de rapports à des événements Livefyre {#section_t15_2hd_4cb}

Ajoutez Adobe Analytics à la gestion dynamique des balises pour que Analytics fonctionne. Pour ce faire, créez une nouvelle propriété et un nouvel outil et ajoutez la nouvelle suite de rapports avec les événements Livefyre à la propriété. Pour plus d’informations sur la gestion dynamique des balises, voir [Gestion dynamique des balises](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Vous n’avez pas besoin d’effectuer cette étape si vous avez déjà configuré une propriété ou un outil pour la suite de rapports que vous avez configurée avec les événements Livefyre.

1. Dans la gestion dynamique des balises, créez ou modifiez une propriété existante.
1. Créez ou modifiez un outil Adobe Analytics existant.
1. Si un outil Adobe Analytics existant n’existe pas, cliquez sur le **[!UICONTROL Add a Tool]** bouton.
Définissez les paramètres suivants pour l’outil :
* Set **[!UICONTROL Tool Type]** to **[!UICONTROL Adobe Analytics]**.
* Enable **[!UICONTROL Automatic Configuration]**.
* Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Ajoutez ou confirmez le nom de la suite de rapports avec les événements Livefyre dans le **[!UICONTROL Report Suites]** champ.

## Étape 4 : Configuration d’une règle de chargement de page pour configurer la gestion d’Analytics {#section_jfj_j3d_4cb}

Configurez une règle de chargement de page pour extraire toutes les données. La règle de chargement de page vous permet de placer du code JavaScript personnalisé dans la règle qui enregistre l’événement au chargement de la page.

>[!NOTE]
>
>N’utilisez pas de règles basées sur un événement ni de règles d’appel direct.

1. Dans la gestion dynamique des balises, sélectionnez **[!UICONTROL Rules]** un onglet.
1. Cliquez sur **[!UICONTROL Page Load Rules]**.
1. Cliquez sur le **[!UICONTROL Create New Rule]** bouton.
1. Ouvrez la **[!UICONTROL Conditions]** section en cliquant sur le **[!UICONTROL Plus]** bouton.
1. Déclenchez la règle. Choisissez **[!UICONTROL DOM Ready]** ou **[!UICONTROL Onload]** déclenchez des types si vous souhaitez retarder ou mettre en oeuvre la règle de manière asynchrone.
1. (Facultatif) Ajoutez des paramètres supplémentaires pour limiter les pages qui affichent les applications Livefyre. Pour plus d’informations sur les autres options de configuration, voir [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Sous **[!UICONTROL Javascript/ Third Party Tags]**, cliquez sur l’ **[!UICONTROL Non-sequential]** onglet, puis sur **[!UICONTROL Add New Script]**.
1. Sélectionnez **[!UICONTROL Sequential HTML]** comme type de script.
1. Ajoutez le script suivant dans l’éditeur de code, puis cliquez sur **[!UICONTROL Save Code]**.
Le script suivant appelle la règle d’appel `livefyre_analytics` direct après le chargement du code JavaScript Livefyre. L’exemple de script suivant vérifie tous les 400 ms si `livefyre.analytics` se trouve sur la page. Une fois la page chargée, livefyre.analytics envoie les informations de suivi.

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

Il existe d’autres méthodes pour implémenter Livefyre avec la gestion dynamique des balises en utilisant des événements personnalisés, des champs d’interface utilisateur Adobe Analytics dans la gestion dynamique des balises et des éléments de données. Ce document utilise le code JavaScript personnalisé pour obtenir le même résultat.

1. Dans la gestion dynamique des balises, sélectionnez l’onglet **Règles** , puis cliquez sur Règles **d’appel** direct.
1. Click on the **Create New Rule** button.
1. Nommez la nouvelle règle **Livefyre Analytics**.
1. Développez la zone de configuration des **conditions** .
1. Dans le champ **Chaîne** , saisissez `livefyre_analytics`.
1. Développez la section Balise JavaScript / tierce et cliquez sur le bouton **Ajouter un nouveau script** .
1. Saisissez **Livefyre Analytics Config** dans la zone de saisie Nom **de la** balise.
1. Sélectionnez Javascript **non séquentiel**.
1. Entrez le code de configuration Livefyre suivant dans l'éditeur de code et cliquez sur le bouton **Enregistrer le code** .

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

* Ajoute un gestionnaire d’analyses pour tous les événements d’analyse de Livefyre. Pour chaque événement, il définit les données sur un objet global, puis distribue l’événement.

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
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {appId : 'eVar81',appType: 'eVar82'};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventMap = {FlagCancel: 'event82',\
FlagClick : 'event82',\
FlagDisokay : 'event82',\
FlagOffensive : 'event82',\
FlagOffTopic : 'event82',\
FlagSpam : 'event82',\
J’aime : 'event82',Charger: 'event81',\
RequestMore : 'event82',\
ShareButtonClick : 'event82',\
ShareFacebook : 'event82',\
ShareOnPostClick : 'event82',\
ShareTwitter : 'event82',\
ShareURL : 'event82',\
SortStream : 'event82',\
TwitterLikeClick : 'event82',TwitterReplyClick: 'event82',\
TwitterRetweetClick : 'event82',\
TwitterUserFollow : 'event82'};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function trackLivefyreEvent(data) {\
var event =[eventMapdata.type];
console.log('Track:', data.type, event);

if (!event) {console.warn(data.type, 'n'est pas mappé à un événement dans AA');\
return;
}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = ['events'];\
switch (event) {case 'event82' : s.eVar83 = data.type;\
vars.push('eVar83');\
break;
default :
}

['generator', 'evars'].foreach(function (type) {\
var obj =[datatype];
for (var d dans obj) {if (obj.hasOwnProperty(d) &amp;&amp;[evarMapd]) {\
s[[evarMapd]] =[objd];\
vars.push([evarMapd]);
}}});

s.linkTrackVars = vars.join(',');\
s.linkTrackEvents = event;\
s.events = event;

console.log('linkTrackVars:', s.linkTrackVars);\
console.log('linkTrackEvents:', s.linkTrackEvents);\
console.log('events:', s.events);

s.tl();
}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Ajoute un gestionnaire d’analyses pour tous les événements d’analyse de Livefyre. Pour chaque événement, il définit les données sur un objet global, puis distribue l’événement.

*/function addAnalyticsHandler() {Livefyre.analytics.addHandler(function (events) {(events)|| []).foreach(function (data) {console.log('Event managed:', data.type);
trackLivefyreEvent(data);
});
});
}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

