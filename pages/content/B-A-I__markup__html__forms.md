---
title: Formulieren
title_long: Formulieren
permalink: markup/html/forms/
---

Een formulier laat de eindgebruiker toe data via je pagina te verzenden. 

Werking
--------

- De gebruiker vult gegevens in, in een formulier op een webpagina.
- De gebruiker verzend het formulier.
- De server ontvangt de gegevens en doet er iets mee
- De server stuurt een antwoord terug naar de browser van de gebruiker.
- De browser toont het antwoord aan de gebruiker.

Het verwerken van de data op de server zal gebeuren met een andere taal, een server-side taal zoals PHP.

Opbouw
-------
Een fomrulier wordt opgemaakt door het gebruik van de form-tags.  
Binnen de form-tags staan alle elementen die we nodige hebben om de data te verzamelen van de gebruiker.

### Input

Input is het meest voorkomende form-element. 
Door de waarde in het attribuut `type` aan te passen kan het verschillende doeleinden hebben. 
Type-mogelijkheden: button, checkbox, color, date, datetime-local, email, file, hidden, image, month, number, password, radio, range, reset, search, submit,...

Indien er geen ondersteuning is voor een bepaalde `type` dan zal de browser een gewoon tekst-vlak tonen.


{% highlight html %}
<form>
    <input type="text">
</form>
{% endhighlight %}

### label