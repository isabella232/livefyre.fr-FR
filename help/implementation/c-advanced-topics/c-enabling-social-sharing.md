---
description: Configurez les informations d'identification qui permettent aux utilisateurs de partager du contenu sur divers réseaux sociaux.
seo-description: Configurez les informations d'identification qui permettent aux utilisateurs de partager du contenu sur divers réseaux sociaux.
seo-title: Activation du partage sur les réseaux sociaux
solution: Experience Manager
title: Activation du partage sur les réseaux sociaux
uuid: f 584 a 0 ae -46 c 7-48 c 1-aea 4-36 da 9 f 1 e 259 b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830

---


# Activation du partage sur les réseaux sociaux {#enabling-social-sharing}

Configurez les informations d&#39;identification qui permettent aux utilisateurs de partager du contenu sur divers réseaux sociaux.

Pour permettre aux utilisateurs de partager du contenu sur des sites de médias sociaux, mettez en œuvre la fonction de partage sur les réseaux sociaux de Livefyre et créez un système oauth pour fournir une authentification appropriée à ces sites. Avec ce système, Livefyre agit au nom de l&#39;utilisateur lorsqu&#39;il choisit de partager du contenu par le biais de médias sociaux.

>[!NOTE]
>
>Différents fournisseurs possèdent des exigences oauth différentes. Contactez vos fournisseurs pour obtenir les informations associées à leur implémentation d&#39;oauth.

## Informations d&#39;identification sociales requises {#section_gff_cjm_b1b}

Si vous utilisez un système d&#39;identité utilisateur personnalisé, vous devez fournir vos informations d&#39;identification sociales pour permettre aux utilisateurs de partager sur Twitter, Facebook ou linkedin à partir d&#39;une application Livefyre.

>[!NOTE]
>
>Les clients qui utilisent Janrain impliquent ne doivent fournir que leur domaine d&#39;interaction et la clé d&#39;API Interagir.

Utilisez le panneau Paramètres d&#39;intégration de la Console d&#39;administration pour saisir ou mettre à jour les informations d&#39;identification sociales suivantes.

### Informations d&#39;identification requises :

* **Identifiant** du client Facebook Secret du client oauth Redirection du proxy
* **Clé API Key** API linkedin
* **Jeton** d&#39;accès de jeton d&#39;accès Twitter clé secrète API clé secrète

## Twitter {#section_qp5_1yl_b1b}

Les informations d&#39;identification Twitter sont disponibles à partir du tableau de bord de l&#39;application Twitter. Pour trouver ces informations d&#39;identification :

* Ouvrez [la page de développement d&#39;applications Twitter](https://dev.twitter.com/apps) en tant que propriétaire de l&#39;application, recherchez votre application, puis cliquez sur le titre.
* Faites défiler l&#39;écran jusqu&#39;à « Votre jeton d&#39;accès » et saisissez les valeurs de « Jeton d&#39;accès » et « Secret d&#39;accès ».  » »

Vous devez :

* Saisissez une valeur pour le champ URL de rappel dans l&#39;application Twitter. Bien que ce champ soit un espace réservé simple, il ne peut pas rester vide.
* Définissez le type d&#39;application pour qu&#39;il dispose à la fois **d&#39;un accès en lecture** et **en écriture** .
* Vérifiez que l&#39;URL du site Web de l&#39;application Twitter se trouve sur le même domaine hôte que l&#39;application Livefyre Core.

>[!NOTE]
>
>Toutes les applications qui affichent du contenu Twitter sont requises pour répondre aux exigences d&#39;affichage. Pour plus d&#39;informations, [consultez les instructions](https://dev.twitter.com/terms/display-requirements) d&#39;affichage Twitter.

## Linkedin {#section_lfz_zxl_b1b}

Les informations d&#39;identification linkedin sont disponibles dans la section Clés oauth des clés d&#39;API de l&#39;application linkedin.

* Connectez-vous à votre compte à partir de la page Développeurs linkedin [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Passez la souris sur votre nom en haut à droite et sélectionnez Clés d&#39;API dans le menu déroulant.
* Cliquez sur le titre de l&#39;application.
* Capture des valeurs Clé API et Clé secrète dans la section Clés oauth

## Facebook {#section_zyb_gpl_b1b}

Les informations d&#39;identification Facebook sont disponibles sur la page Applications développeur.

* Ouvrez [la page Applications développeur Facebook](https://developers.facebook.com/apps) comme propriétaire de l&#39;application, recherchez votre application, puis cliquez sur le titre.
* Prenez les valeurs de l&#39;ID d&#39;application et de la clé secrète de l&#39;application. Pour le secret d&#39;application, vous devrez peut-être cliquer sur le bouton Afficher pour l&#39;afficher.

Le partage sur Facebook requiert que vous configuriez une page de redirection pour répondre aux demandes Facebook et respecter les pratiques de domaine requises par [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). La page doit être hébergée sur votre domaine afin que Facebook puisse vérifier que la requête provient d&#39;une source légitime.

### Redirection Facebook

La page hébergée doit inclure le code suivant :

### Ruby

Il s&#39;agit d&#39;un exemple utilisant Ruby et Rails pour effectuer la redirection Oauth Facebook.

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

Il s&#39;agit d&#39;un exemple utilisant Python et Django pour effectuer la redirection oauth Facebook.

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

### Nodejs

Il s&#39;agit d&#39;un exemple utilisant nodejs et Sail/Express pour effectuer la redirection oauth Facebook.

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

Il s&#39;agit d&#39;un exemple utilisant les contrôleurs Java et Spring pour effectuer la redirection oauth Facebook.

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

## Configuration des fournisseurs de publication {#section_rdk_dpl_b1b}

Par défaut, les boutons Facebook, linkedin et Twitter « Publier vers » s&#39;affichent sur les applications Livefyre Core. Utilisez le paramètre posttobuttons pour configurer les fournisseurs qui apparaîtront lors de l&#39;intégration de l&#39;application Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` est un tableau avec n&#39;importe quel sous-ensemble des options suivantes :

* tw : Twitter
* fb : Facebook
* li : Linkedin
