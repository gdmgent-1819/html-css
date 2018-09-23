---
title: Tekst
title_long: Tekst
permalink: markup/html/text/
---

**H**eading *(Ned.: kop)*
-------------------------

> Definitie
> ---
> Een heading-element omschrijft kort het onderwerp over de sectie die het introduceert. Zoekmachines gebruiken de headings om de structuur en inhoud van een webpagina te indexeren. Heading geeft in HTML de koppen van een tekst weer. Dit gaat van kop 1 tot kop 6, kop 1 is de belangrijkste tot kop 6 de minst belangrijke. 
{:.card.card-definition}

Er zijn 6 niveaus van koppen:

 1. `<h1>`{:.e} … `</h1>`{:.e}: niveau 1 is het **meest** belangrijk.
 2. `<h2>`{:.e} … `</h2>`{:.e} 
 3. `<h3>`{:.e} … `</h3>`{:.e} 
 4. `<h4>`{:.e} … `</h4>`{:.e} 
 5. `<h5>`{:.e} … `</h5>`{:.e} 
 6. `<h6>`{:.e} … `</h6>`{:.e}: niveau 6 is het **minst** belangrijk.

{% highlight html linenos %}
<body>
  <h1>Web &amp; New Media</h1>
  <h2>Semester 1<h2>
  <h3>Webtechnology I<h3>
  <h2>Semester 2<h2>
  <h3>Webtechnology II<h3>
</body>
{% endhighlight %}{:data-file="index.html"}

Dit resulteert visueel in:

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/headings_1.PNG" alt="Headings: voorbeeld 1" caption="Headings: voorbeeld 1" %}

Dit resulteert in de volgende outline of structuur:

- 1\. Web & New Media
  - 1.1 Semester 1
    - 1.1.1 Webtechnology I
  - 1.2 Semester 2
    - 1.2.1 Webtechnology II

> Opmerking
> ---
> - Heading-elementen zijn blokelementen.
> - Sla geen niveau over.
> - Gebruik niet de lagere niveau's om de lettergrootte aan de passen, daarvoor dient [CSS](../../../styles/css).
> - Heading-informatie wordt gebruikt door [user agents](https://nl.wikipedia.org/wiki/Useragent) om een inhoudsopgave (Eng.: Table of contents) te genereren van de webpagina.
> - Bezoekers scannen meestal eerst de headings om een beknopt verhaal te kennen. Wekt dit hun interresse op, dan lezen ze meer.
{:.card.card-remark}

> References
> ---
> - [Mozilla Developer Network: Heading elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)
{:.card.card-source}

**P**aragraph *(paragraaf, alinea)*
-----------------------------------

> Definitie
> ---
> `<p>` … `</p>` groepeert zinnen die bij elkaar horen.
{:.card.card-definition}

{% highlight html linenos %}
<body>
  <p>
    HTML-elementen of tags zijn **case-insensitive**. Dit betekent dat ze geschreven kunnen worden in hoofd- en kleine letters.
  </p>
  <p>
    Toch zullen we steeds, als **Best practice** alle tags of elementen schrijven met **kleine letters (lowercase)**   
    geschreven om de leesbaarheid en de consistentie te bevorderen. 
  </p>
</body>
{% endhighlight %}{:data-file="index.html"}

Dit resulteert visueel in:

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/paragraaf_1.png" alt="Paragraaf: voorbeeld 1" caption="Paragraaf: voorbeeld 1" %}

> References
> ---
> - [Mozilla Developer Network: The Paragraph element](https://developer.mozilla.org/nl/docs/Web/HTML/Element/p)
{:.card.card-source}


### **I**talic

> Definitie
> ---
>  `<i>` … `</i>` wordt gebruikt om tekst cursief te zetten, zonder speciale betekenis.
{:.card.card-definition}

> Opmerking
> ---
> - Vermijd dit element!
> - Je gebruikt beter `<em>` of CSS!
{:.card.card-remark}

{% highlight html linenos %}
<body>
  <p>
    HTML-elementen of tags zijn <i>case-insensitive</i>. Dit betekent dat ze geschreven kunnen worden in hoofd- en kleine letters.
  </p>
</body>
{% endhighlight %}{:data-file="index.html"}

Dit resulteert visueel in:

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/italic_1.png" alt="Italic: voorbeeld 1" caption="Italic: voorbeeld 1" %}

> References
> ---
> - [Mozilla Developer Network: i](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i)
{:.card.card-source}

**Strong** importance *(sterke nadruk)*
---------------------------------------

> Definitie
> ---
> `<strong>` … `</strong>` wordt gebruikt om sterke nadruk te leggen op bepaalde woorden.
{:.card.card-definition}

 - De standaardopmaak is vet.

> References
> ---
> - [Mozilla Developer Network: The Strong Importance element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong)
{:.card.card-source}

**B**old *(vet)*
----------------
> Definitie
> ---
> `<b>` … `</b>` Wordt gebruikt om tekst vet te zetten, zonder speciale betekenis.
{:.card.card-definition}

> Opmerking
> ---
> - Vermijd dit element!
> - Je gebruikt beter `<strong>` of CSS!
{:.card.card-remark}

> References
> ---
> - [Mozilla Developer Network: b: The Bring Attention To element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b)
{:.card.card-source}


**Code** *(programmeercode)*
----------------------------
> Definitie
> ---
> `<code>` … `</code>` Wordt gebruikt om code in de inhoud te zetten.
{:.card.card-definition}


- Een descendant van `<body>`
- Standaard wordt een monospace lettertype gebruikt.

{% highlight html %}
<code>&lt;meta&gt;</code>
{% endhighlight %}

Dit resulteert visueel in:

<code>&lt;meta&gt;</code>

> References
> ---
> - [Mozilla Developer Network: code: The Inline Code element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code)
{:.card.card-source}

**Pre**formatted text *(voorgeformateerde tekst)*
-------------------------------------------------
> Definitie
> ---
> `<pre>` … `</pre>` wordt gebruikt om de witruimte van voorgeformaatterde tekst te behouden.
{:.card.card-definition}

`<pre>` … `</pre>`

- Een descendant van `<body>`
- Standaard wordt een monospace lettertype gebruikt.


**Abbr**eviation *(afkorting)*
------------------------------
> Definitie
> ---
> `<abbr>`{:.e} … `</abbr>` wordt gebruikt om een afkorting te verklaren. De verklaring wordt getoond via het `title`{:.a}-attribuut als je over het `<abbr>`{:.e}-element hovert.
{:.card.card-definition}

> `<abbr>`{:.e} … `</abbr>`{:.e}

- Een descendant van `<body>`

{% highlight html %}
<abbr title="Hypertext Markup Language">HTML</abbr>
{% endhighlight %}

Line **br**eak *(Ned.: regeleinde)*
-----------------------------------

> Definitie
> ---
> `<br>`-element geeft een regeleinde weer in een tekst. De tekst zal op de volgende lijn starten.
{:.card.card-definition}

`<br>`
 - Is een descendant van `<body>`
 - Zelfsluitende tag.

{% highlight html %}
<p>
  Roses are red,<br>
  Violets are blue,<br>
  sugar is sweet,<br>
  And so are you.<br>
</p>
{% endhighlight %}

Dit resulteert visueel in:

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/linebreak_1.png" alt="Line break: voorbeeld 1" caption="Line break: voorbeeld 1" %}

> Opmerking
> ---
> Gebruik dit zo weinig mogelijk!
{:.card.card-remark}

> Opgelet
> ---
> Gebruik dit element **nooit** om tekst te schikken, want daar moet je CSS voor gebruiken.
{:.card.card-warning}

> References
> ---
> - [Mozilla Developer Network: : br: The Line Break element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br)
{:.card.card-source}


**H**orizontal **r**uler *(Ned.: horizontale lijn)*
---------------------------------------------------

> Definitie
> ---
> `<hr>` wordt gebruikt om een **thematic break** *(Ned.: veranderend onderwerp)* tussen paragraafelementen (`<p>`{:.e}) aan te geven.
{:.card.card-definition}

`<hr>`{:.e}

 - Een descendant van `<body>`
 - Zelfsluitende tag.

HTML Character Entities
-----------------------

> Definitie
> ---
> Soms worden speciale tekens niet goed afgebeeld. Entiteiten worden gebruikt om die gereserveerde tekens, die door HTML anders worden geïnterpreteerd, weer te geven. 
{:.card.card-definition}

 - Gebruik UTF-8 als tekenset (zie `<meta charset="UTF-8">`)
 - Indien dat niet helpt, gebruik dan **Escape Characters**

| Teken | Entity     | Betekenis                                   |
|-------|------------|---------------------------------------------|
| `<`   | `&lt;`     | **l**ess **t**han                           |
| `>`   | `&gt;`     | **g**reater **t**han                        |
|-------|------------|---------------------------------------------|
| `à`   | `&agrave;` |                                             |
| `ç`   | `&ccedil;` |                                             |
| `é`   | `&eacute;` |                                             |
| `ê`   | `&ecirc;`  |                                             |
| `è`   | `&egrave;` |                                             |
| `ë`   | `&euml;`   |                                             |
| `ï`   | `&iuml;`   |                                             |
| `€`   | `&euro;`   | **euro** sign                               |
| `&`   | `&amp;`    | **amp**ersand                               |
| `×`   | `&times;`  | vermenigvuldigingsteken                     |
| `…`   | `&hellip;` | **H**orizontal **ellip**sis (beletselteken) |
{:.table.table--primary}


> References
> ---
> - [Mozilla Developer Network: Entity](https://developer.mozilla.org/en-US/docs/Glossary/Entity)
> - [Officiele lijst met entiteiten](https://dev.w3.org/html5/html-author/charref)
{:.card.card-source}
