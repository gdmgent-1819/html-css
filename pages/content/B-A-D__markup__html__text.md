---
title: Tekst
title_long: Tekst
permalink: markup/html/text/
---

**H**eading *(Ned.: kop)*
-------------------

Er zijn 6 niveaus van koppen:

 1. `<h1>`{:.e} … `</h1>`{:.e}: niveau 1 is het **meest** belangrijk.
 2. `<h2>`{:.e} … `</h2>`{:.e} 
 3. `<h3>`{:.e} … `</h3>`{:.e} 
 4. `<h4>`{:.e} … `</h4>`{:.e} 
 5. `<h5>`{:.e} … `</h5>`{:.e} 
 6. `<h6>`{:.e} … `</h6>`{:.e}: niveau 6 is het **minst** belangrijk.

Een descendant van `<body>`{:.e}

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements


**P**aragraph *(paragraaf, alinea)*
-----------------------------------

`<p>` … `</p>`

- Groepeert zinnen die bij elkaar horen.
- Een descendant van `<body>`


**Span**
--------

De volgende markupelementen hebben te maken met **paragrafen**:

- `<span>`{:.e}

**Em**phasis
-------------

De volgende markupelementen hebben te maken met **paragrafen**:

- `<em>`{:.e}


**I**talic
-------------

`<i>` … `</i>`

Wordt gebruikt om tekst cursief te zetten, zonder speciale betekenis.

> ##### **Opmerking** :point_up:
> ---
> - Vermijd dit element!
> - Je gebruikt beter `<em>` of CSS!
{:.alert.alert-info}

- Een descendant van `<body>`

Verkorte schrijfwijze van:

{% highlight html %}
<span style="font-style: italic"> … </span>
{% endhighlight %}

**Strong** importance *(sterke nadruk)*
---------------------------------------

`<strong>` … `</strong>`

Wordt gebruikt om sterke nadruk te leggen op bepaalde woorden.

 - De standaardopmaak is vet.
 - Een descendant van `<body>`

**B**old *(vet)*
----------------

`<b>` … `</b>`

Wordt gebruikt om tekst vet te zetten, zonder speciale betekenis.

 - Een descendant van `<body>`

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