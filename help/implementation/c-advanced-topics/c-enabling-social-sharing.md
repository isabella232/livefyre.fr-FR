---
description: Configurez des informations d’identification qui permettent aux utilisateurs de partager du contenu sur divers réseaux sociaux.
seo-description: Configurez des informations d’identification qui permettent aux utilisateurs de partager du contenu sur divers réseaux sociaux.
seo-title: Activation du partage sur les réseaux sociaux
solution: Experience Manager
title: Activation du partage sur les réseaux sociaux
uuid: f584a0ae-46c7-48c1-aea4-36da9f1e259b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---


# Activation du partage sur les réseaux sociaux {#enabling-social-sharing}

Configurez des informations d’identification qui permettent aux utilisateurs de partager du contenu sur divers réseaux sociaux.

Pour permettre aux utilisateurs de partager du contenu sur les sites de médias sociaux, mettez en oeuvre la fonctionnalité de partage sur les réseaux sociaux de Livefyre et créez un système OAuth pour fournir une authentification appropriée à ces sites. Avec ce système, Livefyre agit au nom de l&#39;utilisateur lorsqu&#39;il choisit de partager du contenu sur les réseaux sociaux.

>[!NOTE]
>
>Différents fournisseurs ont des exigences OAuth différentes. Veuillez consulter vos fournisseurs pour obtenir les informations associées à leur mise en oeuvre d&#39;OAuth.

## Identifiants sociaux requis {#section_gff_cjm_b1b}

Si vous utilisez un système d’identité d’utilisateur personnalisé, vous devez fournir vos informations d’identification sociales pour permettre aux utilisateurs de partager sur Twitter, Facebook ou LinkedIn à partir d’une application Livefyre.

>[!NOTE]
>
>Les clients qui utilisent Janrain Engage doivent uniquement fournir leur domaine Interagir et leur clé API Interagir.

Utilisez le panneau Paramètres d’intégration du Admin Console pour saisir ou mettre à jour les informations d’identification sociales suivantes.

### Informations d&#39;identification requises :

* **Redirection du proxy OAuth** FacebookClient ID
* **Secret de l&#39;API de clé** LinkedInAPI
* **Clé secrète de l&#39;API de Secret de jeton d&#39;accès de jeton** TwitterAccess

## Twitter {#section_qp5_1yl_b1b}

Les informations d’identification Twitter sont disponibles sur le Tableau de bord d’applications Twitter. Pour rechercher ces informations d’identification :

* Ouvrez [la page App Dev de Twitter](https://dev.twitter.com/apps) en tant que propriétaire de l’application, recherchez votre application, puis cliquez sur le titre.
* Faites défiler l’écran jusqu’à &quot;Votre jeton d&#39;accès&quot; et prenez les valeurs de &quot;Jeton d&#39;accès&quot; et &quot;Secret de jeton d&#39;accès&quot;.

Vous devez :

* Entrez une valeur pour le champ URL de rappel dans l’application Twitter. Bien que ce champ puisse être un simple espace réservé, il ne peut pas être laissé vide.
* Définissez le type d’application pour qu’il ait accès à **read** et **write**.
* Vérifiez que l’URL du site Web de l’application Twitter se trouve sur le même domaine hôte que l’application LiveCycle Core.

>[!NOTE]
>
>Toutes les applications qui affichent du contenu Twitter doivent respecter leurs exigences d’affichage. Pour plus d&#39;informations, consultez les [Lignes directrices sur l&#39;affichage Twitter](https://dev.twitter.com/terms/display-requirements).

## LinkedIn {#section_lfz_zxl_b1b}

Les informations d’identification LinkedIn sont disponibles dans la section Clés OAuth des clés d’API de l’application LinkedIn.

* Connectez-vous à votre compte à partir de la page Developers de LinkedIn [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Placez le pointeur de la souris sur votre nom en haut à droite et sélectionnez Clés d’API dans le menu déroulant.
* Cliquez sur le titre de la demande.
* Saisir les valeurs de clé d&#39;API et de clé secrète dans la section Clés OAuth

## Facebook {#section_zyb_gpl_b1b}

Les informations d’identification Facebook sont disponibles sur votre page Applications développeur.

* Ouvrez [la page Applications de développement de Facebook](https://developers.facebook.com/apps) en tant que propriétaire de l&#39;application, recherchez votre application, puis cliquez sur le titre.
* Saisissez les valeurs de l’ID d’application et de la clé secrète d’application. Pour la clé secrète de l’application, vous devrez peut-être cliquer sur le bouton Afficher pour l’afficher.

Le partage sur Facebook nécessite la configuration d’une page de redirection pour répondre aux demandes Facebook et respecter les pratiques de domaine requises par [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). La page doit être hébergée sur votre domaine pour que Facebook puisse vérifier que la demande provient d’une source légitime.

### Redirection Facebook

La page hébergée doit inclure le code suivant :

### Ruby

Voici un exemple d&#39;utilisation de Ruby et Rails pour rediriger Facebook OAuth.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

Voici un exemple d&#39;utilisation de Python et Django pour rediriger Facebook OAuth.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

Il s’agit d’un exemple d’utilisation de NodeJS et de Sail/Express pour rediriger Facebook OAuth.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Voici un exemple d’utilisation des contrôleurs Java et Spring pour rediriger Facebook OAuth.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## Configuration des fournisseurs &quot;Post to&quot; {#section_rdk_dpl_b1b}

Par défaut, les boutons &quot;Publier sur&quot; Facebook, LinkedIn et Twitter s’affichent sur les applications principales Livefyre. Utilisez le paramètre postToButtons pour configurer les fournisseurs qui s’afficheront lors de l’intégration de l’application Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` est un tableau avec n&#39;importe quel sous-ensemble des options suivantes :

* tw : Twitter
* fb : Facebook
* li: LinkedIn
