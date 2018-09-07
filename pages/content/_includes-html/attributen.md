Attributen
----------

### Wat zijn attributen?

HTML-elementen kunnen **attributen** hebben met een bepaalde waarde. Attributen bestaan uit een sleutel en hebben meestal ook een waarde: `sleutel="waarde"`

> Opgelet
> ---
> Attributen staan **enkel op de begintag** en **nooit** op de eindtag!
{:.card.card-warning}

In het voorbeeld wordt de **taal** *(Eng.: **lang**uage)* van het volledige HTML-document als Nederlands ingesteld met de *[ISO 639](http://www.iso.org/iso/home/standards/language_codes.htm) Part 1*-code.

{% highlight html %}
<html lang="nl">
<!-- … -->
</html>
{% endhighlight %}

Elementen kunnen attributen hebben met een bepaalde waarde.

In het voorbeeld wordt de **leesrichting** *(Eng.: **dir**ection)* van de taal ingesteld:

| Waarde     | Betekenis     |
|-----------:|---------------|
| `ltr`{:.v} | left to right |
| `rtl`{:.v} | right to left |
{:.table.table--primary}

{% highlight html %}
<p dir="ltr" lang="nl">Deze tekst is in het Nederlands.</p>
{% endhighlight %}

Het resultaat in de browser:

<p dir="ltr" lang="nl">Deze tekst is in het Nederlands.</p>

{% highlight html %}
<p dir="rtl" lang="ar">هذا النص باللغة العربية.</p>
{% endhighlight %}

Het resultaat in de browser:

<p dir="rtl" lang="ar">هذا النص باللغة العربية.</p>

### Globale attributen

Globale attributen zijn toepasbaar op elk element.

| Attribuut      | Betekenis                                                             |
|---------------:|-----------------------------------------------------------------------|
|   `class`{:.a} | CSS-stijlklasse(s) die op het element van toepassing zijn.            |
|      `id`{:.a} | Unieke identifier van het element.                                    |
|    `lang`{:.a} | Taal *(Eng.: **lang**uage)* van de inhoud van het element.            |
|   `style`{:.a} | Inline-stijlen met CSS. **Probeer dit zoveel mogelijk te vermijden!** |
{:.table.table--primary}

{% highlight html %}
<p id="alinea-1" class="cursief vet" lang="nl">In Gent</p>
{% endhighlight %}
