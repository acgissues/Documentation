# REST API: GET emailingdocument

Dit is een methode om meta gegevens van een emailingdocument op te vragen. 
Deze methode ondersteunt geen parameters. De methode is aan te 
roepen met een HTTP GET request naar de volgende URL:

`https://api.copernica.com/v1/emailingdocument/$id?access_token=xxxx`

Als **$id** kun je de numerieke identifier van een emailingdocument opgeven.

## Geretourneerde velden

* id: 			uniek ID;
* template_id: 		uniek ID van template;
* name: 		naam van document;
* from_address: 		afzenderadres van document;
* subject: 		onderwerp van document;
* source: 		broncode van het document;

## Voorbeeld in PHP

Het volgende PHP script demonstreert hoe je de API methode kunt aanroepen:

```php
// vereiste scripts
require_once("copernica_rest_api.php");

// verander dit in je access token
$api = new CopernicaRestApi("your-access-token");

// voer de opdracht uit en print het resultaat
print_r($api->get("emailingdocument/id"));
```

Dit voorbeeld vereist de [REST API class](rest-php).


## Meer informatie

* [Overzicht van alle API calls](rest-api)
