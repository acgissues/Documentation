# Statistieken in de Publisher

De servers van Copernica slaan informatie op over jouw e-mailings en gebruikers, die vervolgens bekeken kan worden in de Publisher applicatie. Je kunt hier bijvoorbeeld zien hoe vaak je e-mail geopend is. Je kunt de resultaten van een mailing ook exporteren met Publisher of [exporteren met de REST API](./rest-get-logfiles-names).

Als uit je statistieken blijkt dat veel van je mails niet aankomen, kun je 
dit [artikel over errors](./soft-and-hard-bounces-error-types-and-delivery-codes) 
bekijken voor meer informatie.

## Individuele statistieken

Vraag jij je af hoe succesvol je laatste mailing was? Gebruik onze mailing statistieken om te zien of jij tevreden bent.

De document of template statistieken geven informatie over de errors, impressions, clicks etc. De statistieken bevatten ook een tabel met kerncijfers.

De statistieken voor alle mailings verzonden met de Publisher applicatie kunnen gevonden worden in het onderdeel **E-mailings**.

-   Selecteer je mailing/template
-   Klik op het **statistieken** tabje en open het volledige rapport.
-   Om de statistieken te bekijken voor mailings die ingeroosterd staan 
voor verwerking kun je onder de scheduled mails kijken.

## Account mailing statistieken

Als je alle mailing statistieken voor een account wil exporteren kun je 
dit doen in het *E-mailings** menu. Klik hier op **Mailings** > **Statistieken** 
en geef het volledige rapport met statistieken weer. Als je nu weer op 
**Mailing** klikt kun je de optie "Exporteer resultaten..." gebruiken.

## Statistieken exporteren

De resultaten van een mailing kunnen geëxporteerd worden via Publisher of 
met de [REST API](./rest-api). Je kunt deze files vervolgens gebruiken 
voor analyse of berekeningen met bijvoorbeeld Excel.

1.  Selecteer eerst de mailing of template waarvan je de statistieken wil 
    exporteren. Vind het document onder **E-mailings** en selecteer deze. 
    Klik op het **Statistieken** tabblad en ga naar het volledige rapport.
2.  Klik op **Resultaten exporteren** in het **Mailings** menu.
3.  Kies welke informatie (destinations, impressions, clicks,
    errors) je wil exporteren en welke database en collectie velden je 
    in de export wil toevoegen.
4.  Afhankelijk van de vorige instellingen moet je nog een aantal stapjes 
    doorlopen.

Om profielen of subprofielen te exporteren gebaseerd op de resultaten 
van een mailing moet je een selectie aanmaken op basis van deze resultaten. 
Je kunt vervolgens onder **Profielen** de optie vinden om deze te exporteren.

# Statistieken: Kerncijfers en dominante resultaten

De tabel met kerncijfers biedt een overzicht van de belangrijkste
resultaten van een e-mailing of een serie mailings.

## Kerncijfers

- **Verzonden mailings:** Laat het totaal aantal **e-mailings** zien dat
in de ingestelde periode is verstuurd met het account, template of
document.

- **Totaal verzonden berichten:** Laat het totaal
aantal **berichten** zien dat is verstuurd met het account, template of
document.

- **Berichten per dag:** Het totaal aantal berichten dat gemiddeld genomen
per dag is verstuurd met het account, template of document.

- **Totaal impressies:** Het totaal aantal geregistreerde impressies. We
kunnen een impressie registreren wanneer een ontvanger de e-mail opent,
en de afbeeldingen uit de e-mail bekijkt. Als de afbeeldingen worden
gedownload van onze server, kunnen we achterhalen wanneer en door wie de
e-mail is geopend. Een ontvanger kan meerdere impressies registreren,
wanneer deze persoon de e-mail bijvoorbeeld zowel thuis, als op het werk
een keer bekijkt.

- **Berichten met impressie:** alle berichten waar een of meerdere
impressies zijn geregistreerd.

- **Percentage geopend:** Berichten met een impressie, gedeeld door het
totaal aantal verzonden berichten, maal 100.

- **Totaal aantal kliks:** het totaal aantal geregistreerde kliks. Als een
ontvanger 3 keer heeft geklikt op 2 verschillende links, dan wordt dit
geteld als 3 kliks.

- **Unieke kliks:** Het aantal bestemmingen waar een klik is
geregistreerd. Elke bestemming is dus 1 keer geteld. Ook al heeft hij of
zij meerdere malen geklikt of dezelfde of op verschillende links in de
e-mail.

- **Click through rate:** het aantal unieke kliks, gedeeld door het aantal
berichten met impressie. En dit dan weer maal 100. Zie ook [dit artikel](./statistics-ctr) 
dat dieper ingaat op de click-through rate.

- **Totaal aantal klachten:** een klacht is een spamregistratie door de
ontvanger. Dit cijfer geeft het totaal aantal keer weer dat een bericht
door een ontvanger als spam is gemarkeerd. Als het totaal aantal
klachten hoger is dan het aantal unieke klachten, dan gaat er
waarschijnlijk iets fout met de klachtenafhandeling. Controleer daarom
of het **uitschrijfgedrag** correct is ingesteld, en dat uitschrijvers
en klagers uit de **nieuwsbriefselectie** worden gefilterd.  

- **Unieke klachten:** alle unieke bestemmingen die 1 keer of meerdere
malen op de spamknop hebben gedrukt naar aanleiding van je e-mailing(s).

- **Percentage klachten:** het aantal unieke klachten, gedeeld door het
totaal aantal bestemmingen maal 100.

## Dominante resultaten

Bij de resultaten van e-mailings worden naast de kerncijfers ook de dominante resultaten van de mailing getoond. Per bestemming wordt het belangrijkste resultaat weergegeven. Een geregistreerde klik is belangrijker dan een impressie. De waarde die wij toekennen aan het resultaat wordt van links naar rechts weergegeven. Een fout is het minst dominant, een spamklacht het meest dominant.

Elke bestemming wordt 1 keer geteld. Het totaal is dus altijd 100 procent. Dus ontvangers die hebben geklikt, zijn niet meegeteld bij impressies. Het aantal kliks in het groene vlak zijn niet het totaal aantal kliks, maar het aantal bestemmingen waar een klik is geregistreerd (en daarna geen uitschrijving of spamklacht). Als geen resultaat is gemeten, staat men in 'Geen terugkoppeling'.

- **Fout** Bij het afleveren van de email is ergens een fout opgetreden. Meer details over de opgetreden fouten van de emailing vind je in het tabblad Errors van de email statistieken, of in het tabblad Campagnes van de bestemming waar de fout is opgetreden.

- **Geen terugkoppeling** We hebben bij deze ontvangers niet kunnen registreren of de mailing is geopend/bekeken/aangeklikt. Dit kan liggen aan instellingen bij de ontvangende mailserver of diegene heeft de mailing niet geopend. Er zijn geen verdere gegevens beschikbaar.

- **Impressie** Toont het aantal bestemmingen die de mailing hebben geopend, maar niet geklikt hebben op een link.

- **Klik** Geeft het aantal unieke bestemmingen weer die op een hyperlink hebben geklikt. Kliks op de {unsubscribe} link worden hier niet in meegeteld.

- **Uitschrijving** Geeft het aantal bestemmingen weer die op de {unsubscribe} link hebben geklikt in de mailing.

- **Spamklacht** Je ziet hoeveel unieke geadresseerden de email naar hun spambox hebben verwezen, of anderzijds een abusemelding hebben ingediend.

## Kerncijfers vs. het dominante resultaat

Bij de kerncijfers (getoond boven de dominante resultaten) worden alle impressies en alle kliks meegeteld en in het dominante resultaat éénmalig.

*Voorbeeld: een profiel heeft een impressie en een klik dan is dit profiel bij de kerncijfers zowel bij de impressies als bij de kliks zichtbaar. Bij het dominante resultaat zal ditzelfde profiel enkel bij de kliks zichtbaar zijn (belangrijkste activiteit).*
