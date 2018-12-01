
Een formulier laat de eindgebruiker toe data via je pagina te verzenden.

Werking
--------

1. De gebruiker vult gegevens in, in een formulier op een webpagina.
2. De gebruiker verzend het formulier.
3. De server ontvangt de gegevens en doet er iets mee
4. De server stuurt een antwoord terug naar de browser van de gebruiker.
5. De browser toont het antwoord aan de gebruiker.

Het verwerken van de data op de server zal gebeuren met een andere taal, een server-side taal zoals PHP.

Opbouw
-------
Een formulier wordt opgemaakt door het gebruik van form-tags. 
{% highlight html %}
<form>
    <!-- Hier komen alle elementen om data te verzamelen -->
</form>
{% endhighlight %}
Binnen de form-tags staan alle elementen die we nodige hebben om de data te verzamelen van de gebruiker.

### Attributen 
Hieronder is een beknopt overzicht te vinden van alle attributen die kunnen voorkomen op de form-tag en waarvoor ze worden gebruikt:
> - `accept-charset`: welke character encoding op de server zal geaccepteerd worden (bijvoorbeeld UTF-8). Meerdere waardes kunnen worden gescheiden door een spatie.
> - `action`: de URI van het programma of script dat de afhandeling van het formulier zal verzorgen. 
> - `autocomplete`: of de browser autoaanvulling mag gebruiken op de aanwezige elementen. Mogelijke waarden zijn: `off` en `on`.
> - `enctype`: instellen van het mediatype ([MIME type](https://en.wikipedia.org/wiki/Media_type)) dat zal worden verstuurd naar de server. Mogelijke waarden zijn: `application/x-www-form-urlencoded` (standaard), `multipart/form-data` (bij versturen van bestanden) en `text/plain (HTML5)`.
> - `method`: de [HTTP method](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) die moet worden toegepast. De meest gebruikte waarden zijn: `get` en `post`. 
> - `name`: de (unieke) naam van het formulier.
> - `novalidate`: wanneer dit attribuut wordt toegevoegd, zal het formulier niet worden gevalideerd aan client side.
> - `target`: waar het antwoord op het verstuurde formulier wordt getoond. Analoog aan het target attribuut bij anker-elementen. Mogelijke waarden zijn: `_blank`, `_top`, `_self` en `_parent`.

{% highlight html %}
<form action='./scripts/form.php' method='get' name='formuliertje'>
    <!-- Elementen -->
</form>
{% endhighlight %}

### Input-elementen

Input is het meest voorkomende form-element. 
Door de waarde in het attribuut `type` aan te passen kan het verschillende doeleinden hebben. 
Er is een heel gamma aan input types beschikbaar om de gebruiker toe te laten verschillende soorten data in te voeren.

- `<input type="checkbox">`: een enkele waarde die kan aan- of afgevinkt worden.
- `<input type="color">`: een element waarmee een kleur kan gekozen worden. Toont in de meeste browsers een colorpicker.
- `<input type="date">`:  een element waarmee een datum kan worden ingegeven. Toont in de meeste browsers een datepicker.
- `<input type="datetime-local">`: een element waarmee een datum en tijd kan worden ingegeven. 
- `<input type="email">`: een element waarmee een emailadres kan worden ingegeven.
- `<input type="file">`: een element waarmee een bestand kan geselecteerd worden en opgeladen.
- `<input type="hidden">`: een element dat niet zichtbaar is voor de gebruiker, maar wel een waarde kan krijgen. Deze waarde wordt meestal ingesteld via javascript.
- `<input type="month">`: een element waarmee een maand kan worden ingegeven.
- `<input type="number">`: een element waarmee een nummer kan worden ingegeven.
- `<input type="password">`: een element waarmee een wachtwoord kan worden ingegeven. De alfanumerieke tekens zijn onleesbaar gemaakt.
- `<input type="radio">`: een element waarmee een enkele waarde kan worden geselecteerd uit een groep van waardes.
- `<input type="range">`: een element waarmee een nummer kan worden geselecteerd uit een bepaalde range. Toont in de meeste browsers een slider.
- `<input type="reset">`: een button die na klikken alle waarden in het formulier te wissen = resetten.
- `<input type="search">`: een element om een zoekterm in te geven.
- `<input type="submit">`: een button die na klikken alle waarden in het formulier zal verzenden naar de ingestelde locatie.
- `<input type="tel">`: een element om een telefoonnummer in te geven.
- `<input type="text">`: een standaard textvak. Indien het er geen ander element kan gevonden worden is dit meestal de keuze die zal overblijven.
- `<input type="time">`: een element om een tijdstip in te geven.
- `<input type="url">`: een element om een url in te geven.
- `<input type="week">`: een element om een week in te geven.

Indien er geen ondersteuning is voor een bepaalde `type` dan zal de browser een gewoon tekst-vlak tonen.

<iframe height='400' scrolling='no' title='Flexbox: align-content' src='//codepen.io/lesso/embed/ZmVvge/?height=407&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

{% highlight html %}
<form>
    <input type="text" name="voornaam">
</form>
{% endhighlight %}

Hierna volgt een overzicht van de belangrijkste attributen van input-elementen:
> - `type`:
> - `name`:
> - `placeholder`:
> - `disabled`:
> - `required`:
> - `pattern`:
> - `form`:
> - `value`:  

### Textarea-elementen

### Select-elementen

### Label-elementen

Validatie
---------
Bij form validatie zal alle ingegeven (en niet ingegeven ;-)) data worden nagekeken en gevalideerd. Bij het optreden van validatiefouten zal de gebruiker een foutboodschap op het scherm zien verschijnen met de vraag om de foutieve velden aan te passen. Een accurate validatie van een formulier is niet onbelangrijk. We willen namelijk:
- De juiste data ontvangen, in het correcte formaat
- Onszelf beschermen tegen kwaadaardige acties van buitenaf

<!-- Er zijn twee types van validatie: validatie langs de client kant en validatie langs de kant van de server. Het is belangrijk om beide types toe te passen omdat aanvallen langs beide kanten mogelijk zijn.
Sinds de komst van HTML5 is er ingebouwde -client side- validatie mogelijk. Hieronder een summiere samenvatting van hoe we gebruik kunnen maken van de ingebouwde validatie: -->