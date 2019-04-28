---
description: valeur nulle
seo-description: valeur nulle
seo-title: Utiliser Livefyre avec Adobe Analytics et Dynamic Tag Manager (DTM) lk xavvn vefyre avec Adobe Analytics et Dynamic Tag Manager (DTM)
uuid: 9 a 1 c 25 c 0-c 474-46 ff -82 ac-e 89357007 c 7 f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# Utiliser Livefyre avec Adobe Analytics et Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configurez Adobe Analytics et le gestionnaire dynamique de balises (DTM) pour collecter des données pour les applications Livefyre.

## Étape 1 : Configuration d&#39;événements dans Adobe Analytics {#section_iks_kgd_4cb}

Faites correspondre les événements Livefyre à un ou plusieurs événements de réussite personnalisés dans le Gestionnaire de suites de rapports Adobe Analytics.

Pour plus d&#39;informations sur le Gestionnaire de Report Suites, voir [Gestionnaire de Report Suites](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. Connectez-vous à Adobe Analytics en tant qu&#39;administrateur.
1. Ouvrez le Gestionnaire de Report Suites d&#39;Adobe Analytics.
1. Créez une suite de rapports ou choisissez une suite existante.
1. Modifiez la suite de rapports en cliquant sur la suite de rapports à modifier, puis accédez **[!UICONTROL Edit Settings > Conversion > Success Events]**à la suite.
1. Faites correspondre les événements Livefyre à un ou plusieurs événements de réussite personnalisés.

## Étape 2 : Configuration des variables de conversion

Mappez les variables de conversion Livefyre (evars) aux variables de conversion dans le Gestionnaire de suites de rapports d&#39;Adobe Analytics. Les variables de conversion se comportent comme une fonction de tri pour déterminer comment vous envisagez d&#39;identifier les données rassemblées à partir des événements Livefyre.

1. Dans le Gestionnaire de Report Suites, cliquez **[!UICONTROL Edit Settings > Conversion > Conversion Variables]** sur.
1. Choisissez les variables de conversion (evars) personnalisées pour les utiliser et les mapper aux variables de conversion Livefyre. Pour mapper une variable de conversion Livefyre à une variable de conversion personnalisée :
* Activation de la variable de conversion
* Nommer la variable de conversion
* Donner à la variable de conversion un type
1. Enregistrez les variables de conversion personnalisées.

## Étape 3 : Utiliser la gestion dynamique des balises pour ajouter votre suite de rapports avec des événements Livefyre {#section_t15_2hd_4cb}

Ajoutez Adobe Analytics à la gestion dynamique des balises pour que Analytics fonctionne. Pour ce faire, créez une propriété et un outil et ajoutez la nouvelle suite de rapports avec les événements Livefyre à la propriété. Pour plus d&#39;informations sur la gestion dynamique des balises, voir [la gestion dynamique](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)des balises.

Vous n&#39;avez pas besoin d&#39;effectuer cette étape si vous disposez déjà d&#39;une propriété ou d&#39;un outil configuré pour la suite de rapports que vous configurez avec les événements Livefyre.

1. Dans la gestion dynamique des balises, créez ou modifiez une propriété existante.
1. Créez ou modifiez un outil Adobe Analytics existant.
1. Si un outil Adobe Analytics existant n&#39;existe pas, cliquez sur le **[!UICONTROL Add a Tool]** bouton.
Définissez les paramètres suivants pour l&#39;outil :
* Défini **[!UICONTROL Tool Type]** sur **[!UICONTROL Adobe Analytics]**.
* Activez **[!UICONTROL Automatic Configuration]**.
* Activez **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Ajoutez ou confirmez le nom de la suite de rapports avec les événements Livefyre au **[!UICONTROL Report Suites]** champ.

## Étape 4 : Configuration d&#39;une règle de chargement de page pour configurer la gestion des analyses {#section_jfj_j3d_4cb}

Configurez une règle de chargement de page pour extraire toutes les données. La règle de chargement de page vous permet de placer javascript personnalisé dans la règle qui enregistre l&#39;événement au chargement de la page.

>[!NOTE]
>
>N&#39;utilisez pas de règles basées sur un événement ou de règles d&#39;appel direct.

1. Dans la gestion dynamique des balises, sélectionnez **[!UICONTROL Rules]** onglet.
1. Cliquez **[!UICONTROL Page Load Rules]** sur.
1. Cliquez sur **[!UICONTROL Create New Rule]** le bouton.
1. Ouvrez **[!UICONTROL Conditions]** la section en cliquant sur **[!UICONTROL Plus]** le bouton.
1. Déclenchez la règle. Choisissez **[!UICONTROL DOM Ready]** ou **[!UICONTROL Onload]** déclenchez les types si vous souhaitez retarder ou implémenter la règle de manière asynchrone.
1. (Facultatif) Ajoutez des paramètres supplémentaires pour limiter les pages qui affichent les applications Livefyre. For more information about additional configuration options, see [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Sous **[!UICONTROL Javascript/ Third Party Tags]**, cliquez sur l&#39; **[!UICONTROL Non-sequential]** onglet, puis sur **[!UICONTROL Add New Script]**.
1. Sélectionnez **[!UICONTROL Sequential HTML]** comme type de script.
1. Ajoutez le script suivant dans l&#39;éditeur de code et cliquez **[!UICONTROL Save Code]**sur.
Le script suivant appelle la règle d&#39;appel `livefyre_analytics` direct après le chargement du code JavaScript Livefyre. L&#39;exemple de script suivant vérifie toutes les 400 ms pour savoir si `livefyre.analytics` elles se trouvent sur la page. Une fois la page chargée, livefyre. analytics envoie les informations de suivi.

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

1. Cliquez **[!UICONTROL Save Code]** sur.
1. Cliquez **[!UICONTROL Save Rule]** sur.

## Étape 5 : Création d&#39;une règle d&#39;appel direct pour construire la configuration de mappage Adobe Analytics pour Livefyre {#section_gvp_b1g_pdb}

Il existe d&#39;autres moyens de mettre en œuvre Livefyre avec la gestion dynamique des balises à l&#39;aide d&#39;événements personnalisés, de champs de l&#39;interface utilisateur Adobe Analytics dans la gestion dynamique des balises et d&#39;éléments de données. Ce document utilise Javascript personnalisé pour accomplir le même effet.

1. Dans la gestion dynamique des balises, sélectionnez **l** &#39;onglet Règles, puis cliquez sur Règles d&#39;appel **direct**.
1. Cliquez sur le **bouton Créer une règle** .
1. Nommez la nouvelle règle **Livefyre Analytics**.
1. Développez **la zone** de configuration des conditions.
1. Dans le champ **String,** saisissez `livefyre_analytics`.
1. Développez la section Balises Javascript/tierces et cliquez sur le **bouton Ajouter un script** .
1. Saisissez **la configuration Livefyre Analytics** dans la zone **de saisie Nom** de balise.
1. Sélectionnez **Javascript non séquentiel**.
1. Saisissez le code de configuration Livefyre suivant dans l&#39;éditeur de code, puis cliquez sur le bouton **Enregistrer le code** .

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

* Ajoute un gestionnaire d&#39;analyse pour tous les événements d&#39;analyse de Livefyre. Pour chaque événement, il définit les données d&#39;un objet global, puis distribue l&#39;événement.

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

var s =_ satellite. gettoolsbytype`('sc')[0]`. getS () ;
var evarmap = {appid
: &#39; Evar 81 &#39;,
apptype : &#39; Evar 82 &#39;}
;

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventmap = {flagcancel
: &#39; event 82 &#39;,\
Flagclick : &#39; event 82 &#39;,\
Flagapprove : &#39; event 82 &#39;,\
Flagoffensive : &#39; event 82 &#39;,\
Flagofftopic : &#39; event 82 &#39;,\
Flagspam : &#39; event 82 &#39;,\
J&#39;aime : &#39; event 82 &#39;,
Load : &#39; event 81 &#39;,\
Requestmore : &#39; event 82 &#39;,\
Sharebuttonclick : &#39; event 82 &#39;,\
Sharefacebook : &#39; event 82 &#39;,\
Shareonpostclick : &#39; event 82 &#39;,\
Sharetwitter : &#39; event 82 &#39;,\
Shareurl : &#39; event 82 &#39;,\
Sortstream : &#39; event 82 &#39;,\
Twitterlikeclick : &#39; event 82 &#39;,
twitterreplyclick : &#39; event 82 &#39;,\
Twitterretweetclick : &#39; event 82 &#39;,\
Twitteruserfollow : &#39; event 82 &#39;}
;

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function tracklivefyreevent (data) {\
var event = eventmapdata[. type];
console. log (&#39;Track : &#39;, data. type, event) ;

if (! event) {console.
warn (data. type,&#39;is not mapped to an event in AA &#39;) ;\
return ;}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = [&#39;events &#39;];\
switch (event) {case&#39;event
82 &#39;: s. evar 83 = data. type ;\
vars. push (&#39;evar 83 &#39;) ;\
break ;
default :}

[&#39; generator &#39;,&#39;evars &#39;]. foreach (function (type) {\
var obj = datatype[];
for (var d in obj) {if
(obj. hasownproperty (d) &amp; &amp; evarmapd[]) {\
s [evarmapd[]] = objd[];\
vars. push (evarmapd[]) ;}}})
;

s. linktrackvars = vars. join (&#39;,&#39;) ;\
s. linktrackevents = event ;\
s. events = event ;

console. log (&#39;linktrackvars : &#39;, s. linktrackvars) ;\
console. log (&#39;linktrackevents : &#39;, s. linktrackevents) ;\
console. log (&#39;events : &#39;, s. events) ;

s. tl () ;}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Ajoute un gestionnaire d&#39;analyse pour tous les événements d&#39;analyse de Livefyre. Pour chaque événement, il définit les données d&#39;un objet global, puis distribue l&#39;événement.

*/function
addanalyticshandler () {Livefyre.
analytics. addhandler (function (events) {(events) || []). Foreach (function (data) {console.
log (&#39;Event managed : &#39;, data. type) ;
Tracklivefyreevent (data) ;})
;})
;}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

