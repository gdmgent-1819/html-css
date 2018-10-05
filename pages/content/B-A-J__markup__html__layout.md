---
title: Lay-out
title_long: Lay-out
permalink: markup/html/layout/
---

Lay-out Elementen
-----------------

- `<main>`
- `<article>`
- `<section>`
- `<aside>`
- `<header>`
- `<nav>`
- `<div>`
- `<span>` 

> References
> ---
> - [Mozilla Developer Network: Layout elements](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
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
