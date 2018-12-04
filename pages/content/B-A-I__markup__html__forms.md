---
title: Formulieren
title_long: Formulieren
permalink: markup/html/forms/
published: true
---

Een formulier zorgt voor een interactie tussen de gebruiker (bezoeker van de website) en de website/webapplicatie. Dankzij een formulier kan er data verzonden worden. Meestal wordt die data naar een web server gestuurd (om de data bijvoorbeeld te mailen naar een ontvanger of in een database te bewaren).

{% include shared/figure.html src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bc6f0c2-fdfd-42d0-86d1-93d72a370521/member-sign-in.jpg" caption="Bron: smashingmagazine.com" %}


Het kan echter ook dat de data niet verzonden wordt naar een webserver, maar de webpagina de data interpreteert voor bijvoorbeeld interactieve doeleinden.

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
| `novalidate`{:.a} | `novalidate`{:.v}   | Bij invullen zal het formulier niet worden gevalideerd aan client side. |
| `target`{:.a} | `_blank_`{:.v}   | Waar het antwoord op het verstuurde formulier wordt getoond.<br> Analoog aan het target attribuut bij anker-elementen.<br> `_blank`: in een nieuw tabblad. |
|               | `_top_`{:.v}   | In de volledige body van het venster |
|               | `_self`{:.v}   | Standaard, in het huidige frame |
|               | `_parent`{:.v}   | In het parent frame |
|---------------|----------------|---------------------------------------------------------------------|
{:.table.table--primary}

{% highlight html %}
<form action='./scripts/form.php' method='get' name='formuliertje' id='formuliertje'>
    <!-- Elementen -->
</form>
{% endhighlight %}

### Label-elementen
Labels zijn stukjes tekst die bij een formulierveld verschijnen. Ze geven aan wat van de gebruiker verwacht wordt als waarde in de verschillende velden. Met behulp van het `for` attribuut op het label element wordt het label gekoppeld aan het element. In de `for` wordt de `id` van het element in kwestie meegegeven.

{% highlight html %}
<form>
    <label for="firstname">Last name (required)</label>
    <input type="text" name="firstname" id="firstname" required>
</form>
{% endhighlight %}


### Input-elementen

Input is het meest voorkomende element binnen een form tag. 

{% highlight html %}
<form>
    <input type="text" id="voornaam" name="voornaam">
</form>
{% endhighlight %}

#### Attributen

Een overzicht van de belangrijkste attributen van input-elementen:
> - `type`: hiermee kan het type input-element worden gekozen.
> - `name`: een naam dat gegeven kan worden aan het input-element.
> - `placeholder`: een stukje tekst dat wordt getoond in het element als hint.
> - `disabled`: hiermee kan het element uitgeschakeld worden = het is niet mogelijk de waarde van het element aan te passen. Dit attribuut hoeft geen waarde te krijgen, de naam van het attribuut gebruiken is voldoende.
> - `required`: hiermee geven we aan dat het veld verplicht in te vullen is. Het formulier kan niet zonder een waarde verzonden worden. Dit attribuut hoeft geen waarde te krijgen, de naam van het attribuut gebruiken is voldoende.
> - `pattern`: hier kan een [reguliere expressie](https://en.wikipedia.org/wiki/Regular_expression) ingegeven worden om een bepaalde waarde af te dwingen (bijvoorbeeld: 3 numerieke karakters -> [0-9]{3}).
> - `form`: hier kan een `id` van een form element aan meegegeven worden om het element aan het formulier te koppelen.
> - `value`: met dit attribuut kan de waarde van het input-element ingesteld worden. 

Door de waarde in het attribuut `type` aan te passen kan het verschillende doeleinden hebben. 
Er is een heel gamma aan input types beschikbaar om de gebruiker toe te laten verschillende soorten data in te voeren.

#### Type-Attribuut

##### Text - Search - Tel - Email - Url - Password - Number

`<input type="text">`  
Een standaard textvak. Indien het er geen ander element kan gevonden worden is dit meestal de keuze die zal overblijven.

`<input type="search">`  
Een element om een zoekterm in te geven.

`<input type="tel">`  
Een element om een telefoonnummer in te geven.

`<input type="email">`  
Een element waarmee een emailadres kan worden ingegeven.

`<input type="url">`  
Een element om een url in te geven.

`<input type="password">`  
Een element waarmee een wachtwoord kan worden ingegeven. De alfanumerieke tekens zijn **onleesbaar** gemaakt.

`<input type="number">`  
Een element waarmee enkel een nummer kan worden ingegeven.

<iframe height='575' scrolling='no' title='Input - Text/Search/Tel/Email/Url/Password/Number' src='//codepen.io/fredroeg/embed/qQgGzL/?height=572&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

##### Checkbox & Radiobutton

`<input type="checkbox">`  
Een enkele waarde die kan aan- of afgevinkt worden.  
In een groep van checkboxes kunnen **één of meerdere waarden** aangevinkt worden.

`<input type="radio">`  
Een element waarmee een enkele waarde kan worden geselecteerd uit een groep van waardes.  
In een groep van radiobuttons kan **slechts één waarde** aangevinkt worden.


<iframe height='415' scrolling='no' title='Input - Checkbox' src='//codepen.io/fredroeg/embed/rQPgKY/?height=414&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

##### Color

`<input type="color">` 

Een element waarmee een kleur kan gekozen worden. Toont in de meeste browsers een colorpicker.

<iframe height='265' scrolling='no' title='Input - Color' src='//codepen.io/fredroeg/embed/QJYRZK/?height=265&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

##### Date - Datetime - Month - Time - Week

`<input type="date">`  
Een element waarmee een datum kan worden ingegeven. Toont in de meeste browsers een datepicker.

`<input type="datetime-local">`  
Een element waarmee een datum en tijd kan worden ingegeven. 

<iframe height='400' scrolling='no' title='Input - Date(time)' src='//codepen.io/fredroeg/embed/mQvYQN/?height=200&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

`<input type="month">`  
Een element waarmee een maand kan worden ingegeven.

`<input type="time">`  
Een element om een tijdstip in te geven.  

`<input type="week">`  
Een element om een week in te geven.

##### Reset - Submit

`<input type="reset">`  
Een button die na klikken alle waarden in het formulier te wissen = resetten.

`<input type="submit">`  
Een button die na klikken alle waarden in het formulier zal verzenden naar de ingestelde locatie.

> Opmerking
> ---
> Het is beter de ```<button>```-tag binnen een formulier te gebruiken i.p.v. een ```<input type="submit">```. Een button heeft een openings en sluitgins-tag en kan daarom content bevatten.
{:.card.card-remark}

##### File - Hidden - Range

`<input type="file">`  
Een element waarmee een bestand kan geselecteerd worden en opgeladen.

`<input type="hidden">`  
Een element dat niet zichtbaar is voor de gebruiker, maar wel een waarde kan krijgen. Deze waarde wordt meestal ingesteld via javascript.

`<input type="range">`  
Een element waarmee een nummer kan worden geselecteerd uit een bepaalde range. Toont in de meeste browsers een slider.


Indien er geen ondersteuning is voor een bepaalde `type` dan zal de browser een gewoon tekst-vlak tonen. 

##### Overzicht (voorbeeld)

Hieronder een totaalvoorbeeld van hoe de bovenstaande types kunnen worden gebruikt.

<iframe height='400' scrolling='no' title='Formulieren: input types' src='//codepen.io/lesso/embed/ZmVvge/?height=407&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### Textarea-elementen
In een textarea kan een tekst ingegeven worden van meerdere lijnen. 

Het aantal rijen en kolommen kan worden ingesteld met de attributen `cols` en `rows`, hoewel het aangeraden is om dit via css te stijlen.  
Er kan een standaard tekst worden meegegeven door de tekst binnen de `<textarea></textarea>` tags te plaatsen.

<iframe height='400' scrolling='no' title='Formulieren: textarea' src='//codepen.io/lesso/embed/aQXVQo/?height=407&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

{% highlight html %}
<form>
    <textarea name="langeTekst" id="langeTekst" cols="100" rows="10" placeholder="Geef je tekst hier in...">
        Dit is mijn standaard tekst!
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris tempus tellus ut velit accumsan, sit amet suscipit lacus egestas. Cras sit amet eleifend sem. Aenean dictum vehicula ante, ut hendrerit magna tempor eu.
    </textarea>
</form>
{% endhighlight %}

### Select-elementen
Met het select element kan een dropdownlijst worden samengesteld. 

Dit element wordt gebruikt wanneer we een gebruiker een voorgedefinieerde waarde willen laten kiezen uit een lijst.   
Deze lijst kan worden samengesteld door binnen de `<select></select>` tag verschillende `<option></option>` tags te definieren. 

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
Bij form validatie zal alle (al dan niet) ingegeven data worden nagekeken en gevalideerd. 

Bij het optreden van validatiefouten zal de gebruiker een **foutboodschap** op het scherm zien verschijnen met de vraag om de foutieve velden aan te passen. Een accurate validatie van een formulier is niet onbelangrijk. 

We willen namelijk:
- De juiste data ontvangen, in het correcte formaat
- Onszelf beschermen tegen kwaadaardige acties van buitenaf

Er zijn twee types van formuliervalidatie mogelijk: validatie langs de kant van de gebruiker (**client side**) en validatie langs de kant van de server (**server side**). Het is belangrijk om naast de client side validatie, via de ingebouwde browser validatie en/of javascript, ook server validatie toe te passen op de ontvangen data.

### Het `required`-attribuut
Door het attribuut `required` toe te voegen aan een form element, geven we aan dat de gebruiker dit veld verplicht moet invullen. 

Wanneer de gebruiker het formulier probeert te verzenden zonder een waarde in te vullen, zal de verzending worden gestopt en een foutmelding getoond. 

{% highlight html %}
<form>
    <label for="firstname">First name (required)</label>
    <input type="text" name="firstname" id="firstname" required>
</form>
{% endhighlight %}

### Correct gebruik van input types
Door een correct semantisch gebruik van de verschillende input types, zal de data ook navenant gevalideerd worden. 

Bijvoorbeeld: bij `<input type="email">` zal worden nagekeken of er weldegelijk een emailadres met '@' wordt ingevuld. Het is dus belangrijk om correct gebruik te maken van de verschillende input types.

### Het `pattern` attribuut
Indien er geen aangepast input type bestaat kan er worden gekozen voor `<input type="text">` met een `pattern` attribuut. In het pattern attribuut kan een [reguliere expressie](https://en.wikipedia.org/wiki/Regular_expression) worden ingegeven waarnaar we de ingevoerde data willen laten valideren (bijvoorbeeld: 3 numerieke karakters -> [0-9]{3}).

{% highlight html %}
<form>
    <label for="numeric">Numerieke code van 3 cijfers (required)</label>
    <input type="text" name="numeric" id="numeric" required pattern="[0-9]{3}">
</form>
{% endhighlight %}

<iframe height='400' scrolling='no' title='Formulieren: validatie' src='//codepen.io/lesso/embed/EOrrOL/?height=407&theme-id=0&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

<!-- 
- Datalist
- Fieldset (+legend)
- Optgroup
 -->
