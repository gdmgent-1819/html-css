---
title: Tekst
title_long: Tekst
permalink: markup/html/text/
---



**H**eading *(Ned.: kop)*
-------------------

> Definitie
> ---
> Heading geeft in HTML de koppen van een tekst weer. Dit gaat van kop 1 tot kop 6.
{:.card.card-definition}

Er zijn 6 niveaus van koppen:

 1. `<h1>`{:.e} … `</h1>`{:.e}: niveau 1 is het **meest** belangrijk.
 2. `<h2>`{:.e} … `</h2>`{:.e} 
 3. `<h3>`{:.e} … `</h3>`{:.e} 
 4. `<h4>`{:.e} … `</h4>`{:.e} 
 5. `<h5>`{:.e} … `</h5>`{:.e} 
 6. `<h6>`{:.e} … `</h6>`{:.e}: niveau 6 is het **minst** belangrijk.


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

`<p>` … `</p>`


> References
> ---
> - [Mozilla Developer Network: The Paragraph element](https://developer.mozilla.org/nl/docs/Web/HTML/Element/p)
{:.card.card-source}


### **I**talic

> Definitie
> ---
>  `<i>` … `</i>` wordt gebruikt om tekst cursief te zetten, zonder speciale betekenis.
{:.card.card-definition}


`<i>` … `</i>`

> ##### **Opmerking** :point_up:
> ---
> - Vermijd dit element!
> - Je gebruikt beter `<em>` of CSS!
{:.alert.alert-info}

> References
> ---
> - [Mozilla Developer Network: <i>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i)
{:.card.card-source}

**Strong** importance *(sterke nadruk)*
---------------------------------------

> Definitie
> ---
> `<strong>` … `</strong>` wordt gebruikt om sterke nadruk te leggen op bepaalde woorden.
{:.card.card-definition}

`<strong>` … `</strong>`

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

`<b>` … `</b>`

> ##### **Opmerking** :point_up:
> ---
> - Vermijd dit element!
> - Je gebruikt beter `<strong>` of CSS!
{:.alert.alert-info}

Verkorte schrijfwijze van:

{% highlight html %}
<span style="font-weight: bold"> … </span>
{% endhighlight %}


**Code** *(programmeercode)*
----------------------------

`<code>` … `</code>`

Wordt gebruikt om code in de inhoud te zetten

- Een descendant van `<body>`
- Standaard wordt een monospace lettertype gebruikt.

{% highlight html %}
<code>&lt;meta&gt;</code>
{% endhighlight %}

Ziet er dan zo uit:

<code>&lt;meta&gt;</code>

**Pre**formatted text *(voorgeformateerde tekst)*
-------------------------------------------------

`<pre>` … `</pre>`

Wordt gebruikt om de witruimte van voorgeformaatterde tekst te behouden.

- Een descendant van `<body>`
- Standaard wordt een monospace lettertype gebruikt.


**Abbr**eviation *(afkorting)*
------------------------------

> `<abbr>`{:.e} … `</abbr>`{:.e}

Wordt gebruikt om een afkorting te verklaren. De verklaring wordt getoond via het `title`{:.a}-attribuut als je over het `<abbr>`{:.e}-element hovert.

- Een descendant van `<body>`

{% highlight html %}
<abbr title="Hypertext Markup Language">HTML</abbr>
{% endhighlight %}

Line **br**eak *(Ned.: regeleinde)*
-----------------------------------

`<br>`{:.e}

 - Is een descendant van `<body>`
 - Zelfsluitende tag.

> Opmerking
> ---
> Gebruik dit zo weinig mogelijk!
{:.card.card-remark}

> Opgelet
> ---
> Gebruik dit element **nooit** om tekst te schikken, want daar moet je CSS voor gebruiken.
{:.card.card-warning}

**H**orizontal **r**uler *(Ned.: horizontale lijn)*
---------------------------------------------------

`<hr>`{:.e}

Wordt gebruikt om een **thematic break** *(Ned.: veranderend onderwerp)* tussen paragraafelementen (`<p>`{:.e}) aan te geven.

 - Een descendant van `<body>`
 - Zelfsluitende tag.

HTML Character Entities
-----------------------

Soms worden speciale tekens niet goed afgebeeld.

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

> Zie ook
> ---
> - <https://dev.w3.org/html5/html-author/charref>
> - Handboek p. 193-194!
{:.card.card-link}