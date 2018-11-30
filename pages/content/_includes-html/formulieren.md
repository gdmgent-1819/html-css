
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
Type-mogelijkheden: button, checkbox, color, date, datetime-local, email, file, hidden, image, month, number, password, radio, range, reset, search, submit,...

Indien er geen ondersteuning is voor een bepaalde `type` dan zal de browser een gewoon tekst-vlak tonen.


{% highlight html %}
<form>
    <input type="text">
</form>
{% endhighlight %}

### Textarea-elementen

### Select-elementen

### Label-elementen

### Button-elementen

Validatie
---------
