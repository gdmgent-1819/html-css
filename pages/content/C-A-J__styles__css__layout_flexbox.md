---
title: Lay-out Flexbox
title_long: Lay-out Flexbox
permalink: styles/css/layout/flexbox
published: false
---

CSS Flexbox: Het flexible box model
-----------------------------------

Met behulp van flexbox kunnen we elementen op een webpagina **dynamisch positioneren** zonder hierbij `float` of `position` te gaan gebruiken.
Flexbox zorgt ervoor dat de `width` en `height` van child elementen automatisch wordt aangepast om op een zo optimaal mogelijke manier gebruik te maken van de ruimte in een container. Dit is bijzonder handig wanneer we **responsive en mobiel-vriendelijke** webpaginas willen ontwikkelen.
We onderscheiden twee hoofdcategorieën van elementen bij flexbox: de container en de items. 

Basisprincipes
--------------
{% include shared/figure.html src="https://www.w3.org/TR/css-flexbox-1/images/flex-direction-terms.svg" alt="Flex direction terms" caption="Flex direction terms &copy; W3.org" %}

De flexbox items zullen geplaatst worden op de **main axis** van **main start** tot **main end** of de **cross axis** van **cross start** tot **cross end**.

> - **main axis**: De hoofdas van de flexbox container waarop de flexbox items zullen worden geplaatst. De richting van de items kan worden ingesteld met behulp van de `flexbox-direction` eigenschap.
> - **main start** en **main end**: Het start- en eindpunt op de hoofdas waarop de flexbox items zullen worden geplaatst in de container.
> - **main size**: De `width` & `height` van de flexbox items bepalen de grootte van de as.
> - **cross axis**: De as welke loodrecht op de hoofdas (main axis) staat. De richting van deze as wordt tevens bepaald door de richting van de hoofdas.
> - **cross start** en **cross end**: Het start- en eindpunt of de cross axis waartussen de flexbox items zullen worden geplaatst.
> - **cross size**: De `width` & `height` van de flexbox items bepalen de grootte van de as.

Flexbox **container** = parent
--------------------------

### display

De standaardwaarde van de `display` eigenschap zal `block` of `inline` zijn afhankelijk van het html-element dat zal worden aangesproken.
Zet de waarde van `display` op `flex` of `inline-flex` om flexbox toe te passen voor alle elementen binnen de container (children). 

{% highlight css %}
.container {
  display: flex; /* of inline-flex */
}
{% endhighlight %}

In onderstaand voorbeeld zien we hoe door middel van flexbox onze items (blok 1-6) automatisch de beschikbare ruimte van onze container kunnen laten gebruiken voor het naast elkaar tonen van de blokken. 

<iframe height='400' scrolling='no' title='Flexbox 1' src='//codepen.io/lesso/embed/vQEPGb/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### flex-direction

### flex-wrap

### justify-content

### align-items

### align-content

Flexbox **items** = children
----------------------------

### order

### flex-grow

### flex-shrink

### flex-basis

### align-self

Samenvatting
------------

### Flex Container (parent-element)

> - `display:`{:.p} `flex`{:.k} &#124; `inline-flex`{:.k}
> - `justify-content:`{:.p} `flex-start`{:.k.d} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `space-between`{:.k} &#124; `space-around`{:.k} &#124; `space-evenly`{:.k} 
>   Uitlijning op de **main-axis** (in de richting van de `flex-direction`{:.p}).
> - `align-items:`{:.p} `flex-start`{:.k} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `baseline`{:.k} &#124; `stretch`{:.k.d}  
>   Uitlijning op de **cross-axis** (dwars op de richting van de `flex-direction`{:.p}).  
>   `row`: van boven naar onder  
>   `column`: in de schrijfrichting, afhankelijk of het HTML-attribuut `dir`{:.a}  de waarde `ltr`{:.k} of `rtl`{:.k} is.
> - `align-content:`{:.p} `flex-start`{:.k.d} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `space-between`{:.k} &#124; `space-around`{:.k}  &#124; `stretch`{:.k}  
>    Uitlijning op de **cross-axis**, vergelijkbaar met `justify-content`{:.p}.  
>    Heeft enkel effect met een `flex-wrap:`{:.p} `wrap`{:.k} of `wrap-reverse`{:.k}
> - `flex-flow:`{:.p} `«flex-direction»`{:.v} `«flex-wrap»`{:.v}
>    1. `flex-direction:`{:.p} `row`{:.k.d} &#124; `row-reverse`{:.k} &#124; `column`{:.k} &#124; `column-reverse`{:.k}
>    2. `flex-wrap:`{:.p} `nowrap`{:.k.d} &#124; `wrap`{:.k} &#124; `wrap-reverse`{:.k}

### Flex Items (child-elementen)

> - `align-self:`{:.p} `auto`{:.k.d} &#124; `flex-start`{:.k} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `baseline`{:.k} &#124; `stretch`{:.k}  
>   Overschrijft `align-items`{:.p} voor een specifiek element.
> - `flex:`{:.p} `«flex-grow»`{:.v} `«flex-shrink»`{:.v} `«flex-basis»`{:.v} &#124;  
>   `«flex-grow»`{:.v} `«flex-basis»`{:.v} &#124; `«flex-grow»`{:.v} `«flex-shrink»`{:.v} &#124;  
>   `«flex-basis»`{:.v} &#124; `«flex-grow»`{:.v}
>   1. `flex-grow:`{:.p} `«groeifactor»`{:.v} &#124; `0` &#124; `.5` &#124; `1`{:.d} &#124; `1.5` &#124; `2` &#124; …
>   2. `flex-shrink:`{:.p} `«krimpfactor»`{:.v} &#124; `0` &#124; `.5` &#124; `1`{:.d} &#124; `1.5` &#124; `2` &#124; …
>   3. `flex-basis:`{:.p} `«afmeting-met-eenheid»`{:.v} &#124; `auto`{:.k.d} &#124; `content`{:.k} &#124; `100%` &#124; `123px` &#124; …
> - `order:`{:.p} … `-2` &#124; `-1` &#124; `0`{:.d} &#124; `1` &#124; `2` &#124; …


> Zie ook
> ---
> - [MDN: CSS Flexible Boxes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes)
> - [Flexbox Froggy](http://flexboxfroggy.com)
> - [Flexbox Playground](https://demo.agektmr.com/flexbox/)
> - [Flexy Boxes](http://the-echoplex.net/flexyboxes/)
> - [W3C / CSS Flexible Box Layout Module](https://www.w3.org/TR/css-flexbox/)
> - [CSS Tricks / A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
{:.card.card-book}