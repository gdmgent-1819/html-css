---
title: Syntaxis
title_long: Syntaxis van HTML
permalink: markup/html/syntaxis/
---

Het HTML-element
----------------

> Opmerking
> ---
> HTML-elementen worden met **kleine letters** geschreven. 
{:.card.card-remark}

### Soorten HTML-elementen

#### Tweeledig

Tweeledige elementen en bestaan uit een **begintag** *(Eng.: opening tag)* en een **eindtag** *(Eng.: closing tag)*.

{% highlight html %}
<html> <!-- Begintag -->

</html> <!-- Eindtag -->
{% endhighlight %}

#### Zelfsluitend

Zelfsluitende elementen hebben maar een tag, een **zelfsluitende tag** *(Eng.: self-closing tag)*. 

{% highlight html %}
<meta> <!-- Zelfsluitend tag in HTML5 -->
{% endhighlight %}

Er is ook een XHTML-notatie (die de striktere regels van XML volgt) van die duidelijker is, maar tegenwoordig nog maar **weinig gebruikt** wordt.

{% highlight html %}
<meta /> <!--Zelfsluitend tag in XHTML5 -->
{% endhighlight %}

> Opmerking
> ---
> Zelfsluitende elementen hebben in XHTML een **forward slash** (`/`) als voorlaatste teken.
{:.card.card-remark}

> Opgelet
> ---
> - **HTML geniet de voorkeur** boven XHTML, omdat de code compacter is en ook omdat in de praktijk zelden perfecte XHTML-code geschreven werd.
> - XHTML en HTML mag je **niet mengen**.
{:.card.card-warning}

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


HTML-commentaar
---------------

Soms is het handig of zelfs nodig om HTML-code te becommentariëren. Door commentaar te voorzien help je de code te verduidlijken, niet enkel voor andere HTML-coders, maar ook voor je toekomstige zelf, want weet je over pakweg een jaar nog hoe je die complexe webpagina precies hebt opgebouwd? Die commentaar is enkel zichtbaar in de broncode en nooit op de pagina zelf.

Commentaar schrijven tussen de HTML-code doe je tussen de **begintag** (`<!--`{:.e}) en **eindtag** (`-->`{:.e}).

{% highlight html %}
<!-- Dit is commentaar. Alles, ook HTML-elementen, binnen deze twee tags wordt genegeerd door de browser. -->
{% endhighlight %}

> Opmerking
> ---
> Overdrijf niet met HTML-commentaar, want bij elk paginabezoek moet die ook gedownload worden terwijl dit geen enkel nut heeft voor de doorsnee websitebezoeker. Liefst wordt de commentaar verwijderd voor de website op de productieserver geplaatst wordt.
>
> Duidelijk geschreven code heeft weinig tot geen commentaar nodig, maar als beginner kan het wel een handige geheugensteun zijn. 
{:.card.card-remark}

> Tip
> ---
> Omdat de browser HTML-tags binnen commentaar negeert kan je dit gebruiken om code tijdelijk uit te schakelen, bijvoorbeeld om iets uit te proberen.
{:.card.card-tip}