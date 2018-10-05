---
title: Lay-out
title_long: Lay-out
permalink: markup/html/layout/
---

Gekende web lay-outs
-------------------

> References
> ---
> - [Mozilla Developer Network: What do common web layouts contain?](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Common_web_layouts)
{:.card.card-source}

https://developer.mozilla.org/en-US/docs/Web/CSS/Layout_mode
https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Introduction


Lay-out Elementen
-----------------

- `<main>`
- `<article>`
- `<section>`
- `<aside>`
- `<header>`
- `<footer>`
- `<nav>`
- `<div>`
- `<span>` 

> References
> ---
> - [Mozilla Developer Network: Layout elements](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
{:.card.card-source}

### `<main>`{:.e}-element

> Definitie
> ---
> Een `<main>`-element representeert de unieke hoofdinhoud op de webpagina, kortom in het <body>-element van een webdocument. De inhoud binnen dit element is gerelateerd tot bepaalde inhoud in de <head> van de webpagina, zoals: title, description, keywords, OpenGraph informatie, … . Er kan slechts één `<main>`-element zijn in een webpagina. 
{:.card.card-definition}

{% highlight html %}

<!-- other content -->

<main>
  <h1>New Media Development (Multimediaproductie)</h1>
  <p>Zijn Websites, Mobiele Applicaties, Internet of Things, Mixed Reality en Smart Assistants voor jou nu al passé? Werk mee aan de hype van morgen en ontwikkel bij ons de skills van de toekomst!</p>
  
  <article>
    <h2>Hackathon-week NMD 2de jaar</h2>
    <p>Onze studenten New Media Development ruilden voor een kleine week hun vertrouwde omgeving te Mariakerke in voor enkele workshops en een coole onderwijsvorm en dit op een vreemde locatie met focus op één opleidingsonderdeel Mobile Development II.</p>
    <p>... </p>
    <p>... </p>
  </article>

  ...
</main>

<!-- other content -->

{% endhighlight %}


> References
> ---
> - [Mozilla Developer Network: Main element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)
{:.card.card-source}

### `<article>`{:.e}-element

> Definitie
> ---
> Een `<article>`-element representeert een component op een webpagina dat bestaat uit een vrijstaande compositie in een document, pagina, applicatie of site. Indien we alle inhoud rondom een `<article>`-element wegdenken blijft dit element verstaanbaar. 
{:.card.card-definition}

Het is herbruikbaar en onafhankelijk distribueerbaar in syndicatie. Het kan een nieuwsartikel, commentaar, forum post, widget of elk ander onafhankelijke inhoud zijn. Wanneer een section wordt gedeeld in andere blogs, twitter, facebook, reddit, RSS feed … gebruik dan een `<article>`-element. De inhoud van statische pagina’s in een site, zoals "About" en "Contact" pagina, worden meestal omsloten door een article element.

{% highlight html %}

<!-- other content -->

<main>
  <h1>New Media Development (Multimediaproductie)</h1>
  <p>Zijn Websites, Mobiele Applicaties, Internet of Things, Mixed Reality en Smart Assistants voor jou nu al passé? Werk mee aan de hype van morgen en ontwikkel bij ons de skills van de toekomst!</p>
  
  <article>
    <h2>Hackathon-week NMD 2de jaar</h2>
    <p>Onze studenten New Media Development ruilden voor een kleine week hun vertrouwde omgeving te Mariakerke in voor enkele workshops en een coole onderwijsvorm en dit op een vreemde locatie met focus op één opleidingsonderdeel Mobile Development II.</p>
    <p>... </p>
    <p>... </p>
  </article>

  ...
</main>

<!-- other content -->

{% endhighlight %}

> Opmerking
> ---
> - Elk `<article>`-element moet geidentificeerd worden met een heading, meestal als eerst kind-element.
> - Een genest `<article>`-element (binnen een andere `<article>`-element) is gerelateerd met het buiten of ouder element.
{:.card.card-remark}

> References
> ---
> - [Mozilla Developer Network: Article element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article)
{:.card.card-source}

### `<section>`{:.e}-elementen

> Definitie
> ---
> Een `<section>`-element definieert een sectie in een web-document. Het groepeert gelijksoortige inhoud die samen slechts een eigenschap of thema vormen.
{:.card.card-definition}

{% highlight html %}
<article>
    <h1>Lay-out</h1>
    <section>
        <h2>Gekende web lay-outs</h2>
        <p>...</p>
    </section>
    <section>
        <h2>Lay-out Elementen</h2>
        <p>...</p>
    </section>
    <section>
        ...
    </section>
/<article>
{% endhighlight %}

> Opmerking
> ---
> - Een section bevat meestal een hoofdding. Iedere section zou geïdentificeerd moeten worden via `<h1>`-`<h6>`-element als een kind van dit element.
> - Een section mag niet gebruikt worden als een generieke container. 
> - Een section verschijnt in de ouline van het web-document via zijn hoofdding. 
> - Een section mag niet gebruikt worden in het geval dat article, aside of nav elementen beter geschikt zijn in bepaalde situaties.
{:.card.card-remark}

> References
> ---
> - [Mozilla Developer Network: Section element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)
{:.card.card-source}

### `<aside>`{:.e}-elementen

> References
> ---
> - [Mozilla Developer Network: Aside element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside)
{:.card.card-source}

### `<header>`{:.e}-elementen

> References
> ---
> - [Mozilla Developer Network: Header element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)
{:.card.card-source}

### `<footer>`{:.e}-elementen

> References
> ---
> - [Mozilla Developer Network: Footer element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer)
{:.card.card-source}

### `<nav>`{:.e}-elementen

> References
> ---
> - [Mozilla Developer Network: Nav element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)
{:.card.card-source}

### `<span>`{:.e}-elementen

> Definitie
> ---
> `<span>` is een **inline** non-semantisch (zonder waardevolle betekenis) element, die we gebruiken om een of meerdere woorden te stijlen bij voorkeur met behulp van een `class`-attribuut (met een specifieke waarde).
{:.card.card-definition}

{% highlight html %}
<span class="baseline">Like Graphics Love Code and make cool shit.</span>
{% endhighlight %}

### `<div>`{:.e}-elementen

> Definitie
> ---
> `<div>` is een **blok** non-semantisch element die we gebruiken wanneer het omsloten blok geen waardevolle betekenis bevat.
{:.card.card-definition}

{% highlight html %}
<div class="shopping-cart">
  <h2>Shopping cart</h2>
  <ul>
    <li>
      <p><a href=""><strong>Lynda.com</strong></a>: 25€.</p>
      <img src="http://blogs.nhtv.nl/nhtv-library/files/2016/03/lynda.png" alt="Lynda.com logo">
    </li>
    <li>
      ...
    </li>
  </ul>
  <p>Total cost: 164€</p>
</div>
{% endhighlight %}

Een winkelmandje (Eng.: Shopping Cart) behoort niet tot (ter zijde van `<aside>` of als onderdeel van `<section>`) de hoofdinhoud op een webpagina. Het is in dit geval ok om een `<div>`-element te gebruiken.

> Opmerking
> ---
> Gebruik enkel een `<div>` wanneer er geen betere sematische oplossing van toepassing is. Beperk het gebruik van `<div>`-elementen binnen een webpagina omdat dit zorgt voor een onoverzichtelijke structuur.
{:.card.card-remark}
