Een formulier zorgt voor een interactie tussen de gebruiker (bezoeker van de website) en de website/webapplicatie. Dankzij een formulier kan er data verzonden worden. Meestal wordt die data naar een web server gestuurd (om de data bijvoorbeeld te mailen naar een ontvanger of in een database te bewaren).

{% include shared/figure.html src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bc6f0c2-fdfd-42d0-86d1-93d72a370521/member-sign-in.jpg" caption="Bron: smashingmagazine.com" %}


Het kan echter ook dat de data niet verzonden wordt nar een webserver, maar de webpagina de data interpreteert voor bijvoorbeeld interactieve doeleinden.

Werking
--------

1. De gebruiker vult gegevens in, in een formulier op een webpagina.
2. De gebruiker verzendt het formulier.
3. De server ontvangt de gegevens en doet er iets mee
4. De server stuurt een antwoord terug naar de browser van de gebruiker.
5. De browser toont het antwoord aan de gebruiker.

Het verwerken van de data op de server zal gebeuren met een andere taal, een server-side taal zoals PHP.

Opbouw
-------
Een formulier wordt steeds omvat door `form`-tags. 
{% highlight html %}
<form>
    <!-- Hier komen alle elementen om data te verzamelen -->
</form>
{% endhighlight %}
Binnen de form-tags staan alle elementen die we nodig hebben om de data te verzamelen van de gebruiker.

### Attributen 

De `form`-tag kan een aantal attributen bevatten.

Hieronder is een beknopt overzicht te vinden van alle attributen die kunnen voorkomen op de form-tag en waarvoor ze worden gebruikt:


| Attibuut      | Waarde         | Betekenis                                                           |
|---------------|----------------|---------------------------------------------------------------------|
| `accept-charset`{:.a}   | `«character-set»`{:.v}   | welke character encoding op de server zal geaccepteerd worden (bijvoorbeeld UTF-8).<br> Meerdere waardes kunnen worden gescheiden door een spatie.     |
| `action`{:.a} | `«URL»`{:.v} | de URI van het programma of script dat de afhandeling van het formulier zal verzorgen.                    |
| `autocomplete`{:.a} | `on`{:.v} | de browser mag de velden automatisch invullen / aanvullen.                  |
|               | `off`{:.v}   | geen auto-aanvulling |
| `enctype`{:.a} | `application/x-www-form-urlencoded`{:.v}   | standaard mediatype ([MIME type](https://en.wikipedia.org/wiki/Media_type)) dat zal worden verstuurd naar de server. |
|               | `multipart/form-data`{:.v}   | nodig bij versturen van bestanden |
|               | `text/plain`{:.v}   | html-5 |
| `method`{:.a} | `get`{:.v}   | De [HTTP method](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) die moet worden toegepast.<br> GET: via de URL als name/value pair |
|               | `post`{:.v}   | De form-data zit in het HTTP-request |
| `name`{:.a} | `«name»`{:.v}   | De (unieke) naam van het formulier. |
| `novalidate`{:.a} | `novalidate`{:.v}   | wanneer dit attribuut wordt toegevoegd, zal het formulier niet worden gevalideerd aan client side. |
| `target`{:.a} | `...`{:.v}   | Waar het antwoord op het verstuurde formulier wordt getoond. Analoog aan het target attribuut bij anker-elementen. Mogelijke waarden zijn: `_blank`, `_top`, `_self` en `_parent`. |
|---------------|----------------|---------------------------------------------------------------------|
{:.table.table--primary}

{% highlight html %}
<form action='./scripts/form.php' method='get' name='formuliertje' id='formuliertje'>
    <!-- Elementen -->
</form>
{% endhighlight %}

### Label-elementen


### Input-elementen

Input is het meest voorkomende element binnen een form tag. 
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

Indien er geen ondersteuning is voor een bepaalde `type` dan zal de browser een gewoon tekst-vlak tonen. Hieronder een voorbeeld van hoe bovenstaande types kunnen worden gebruikt.

<iframe height='400' scrolling='no' title='Formulieren: input types' src='//codepen.io/lesso/embed/ZmVvge/?height=407&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

{% highlight html %}
<form>
    <input type="text" id="voornaam" name="voornaam">
</form>
{% endhighlight %}

Hierna volgt een overzicht van de belangrijkste attributen van input-elementen:
> - `type`: hiermee kan het type input-element worden gekozen.
> - `name`: een naam dat gegeven kan worden aan het input-element.
> - `placeholder`: een stukje tekst dat wordt getoond in het element als hint.
> - `disabled`: hiermee kan het element uitgeschakeld worden = het is niet mogelijk de waarde van het element aan te passen. Dit attribuut hoeft geen waarde te krijgen, de naam van het attribuut gebruiken is voldoende.
> - `required`: hiermee geven we aan dat het veld verplicht in te vullen is. Het formulier kan niet zonder een waarde verzonden worden. Dit attribuut hoeft geen waarde te krijgen, de naam van het attribuut gebruiken is voldoende.
> - `pattern`: hier kan een [reguliere expressie](https://en.wikipedia.org/wiki/Regular_expression) ingegeven worden om een bepaalde waarde af te dwingen (bijvoorbeeld: 3 numerieke karakters -> [0-9]{3}).
> - `form`: hier kan een `id` van een form element aan meegegeven worden om het element aan het formulier te koppelen.
> - `value`: met dit attribuut kan de waarde van het input-element ingesteld worden. 

### Textarea-elementen

<iframe height='400' scrolling='no' title='Formulieren: textarea' src='//codepen.io/lesso/embed/aQXVQo/?height=407&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

{% highlight html %}
<form>
    <textarea name="langeTekst" id="langeTekst" cols="100" rows="10" placeholder="Geef je tekst hier in..."></textarea>
</form>
{% endhighlight %}

### Select-elementen

<iframe height='400' scrolling='no' title='Formulieren: select' src='//codepen.io/lesso/embed/zMePeg/?height=407&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

{% highlight html %}
<form>
    <select name="hobbys" id="hobbys">
        <option value="">--Gelieve een hobby te selecteren--</option>
        <option value="voetbal">Voetbal</option>
        <option value="slapen">Slapen</option>
        <option value="dansen">Dansen</option>
        <option value="netflix">Netflix kijken</option>
        <option value="fietsen">Fietsen</option>
        <option value="eten">Eten</option>
    </select>
</form>
{% endhighlight %}

Validatie
---------
Bij form validatie zal alle ingegeven (en niet ingegeven ;-)) data worden nagekeken en gevalideerd. Bij het optreden van validatiefouten zal de gebruiker een foutboodschap op het scherm zien verschijnen met de vraag om de foutieve velden aan te passen. Een accurate validatie van een formulier is niet onbelangrijk. We willen namelijk:
- De juiste data ontvangen, in het correcte formaat
- Onszelf beschermen tegen kwaadaardige acties van buitenaf

<!-- Er zijn twee types van validatie: validatie langs de client kant en validatie langs de kant van de server. Het is belangrijk om beide types toe te passen omdat aanvallen langs beide kanten mogelijk zijn.
Sinds de komst van HTML5 is er ingebouwde -client side- validatie mogelijk. Hieronder een summiere samenvatting van hoe we gebruik kunnen maken van de ingebouwde validatie: -->