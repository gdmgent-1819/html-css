---
title: Lay-out Flexbox
title_long: Lay-out Flexbox
permalink: styles/css/layout/flexbox
published: true
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

Alle eigenschappen die in volgende sectie worden besproken zijn toepasbaar op flexbox **container** elementen. Met andere woorden: het parent element die de flexbox items zal bevatten.

### display

De standaardwaarde van de `display` eigenschap zal `block` of `inline` zijn afhankelijk van het html-element dat zal worden aangesproken.
Zet de waarde van `display` op `flex` of `inline-flex` om flexbox toe te passen voor alle elementen binnen de container (children). 

{% highlight css %}
.container {
  display: flex; /* of inline-flex */
}
{% endhighlight %}

In onderstaand voorbeeld zien we hoe door middel van flexbox onze items (blok 1-6) automatisch de beschikbare ruimte van onze container kunnen laten gebruiken voor het naast elkaar tonen van de blokken. 

<iframe height='400' scrolling='no' title='Flexbox: display' src='//codepen.io/lesso/embed/vQEPGb/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### flex-direction

Met deze eigenschap kunnen we instellen welke richting de items in de container moeten volgen. Standaardwaarde is hier `row` waarbij de items worden uitgezet van links naar rechts. Andere mogelijke waarden zijn: `row-reverse` &#124; `column` &#124; `column-reverse`.

{% highlight css %}
.container {
  display: flex; 
  flex-direction: row-reverse;
}
{% endhighlight %}

In onderstaand voorbeeld worden alle mogelijke waarden voor `flexbox-direction` getoond.

<iframe height='400' scrolling='no' title='Flexbox: flexbox-direction' src='//codepen.io/lesso/embed/QJNbEO/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### flex-wrap

Standaard zal de browser met `flex-wrap` op `no-wrap` alle items in een container proberen te doen passen op één lijn. Met de waarde op `wrap` of `wrap-reverse` te zetten kan toegestaan worden dat items op de volgende lijn(en) worden gezet.

{% highlight css %}
.container {
  display: flex; 
  flex-wrap: wrap;
}
{% endhighlight %}

In onderstaand voorbeeld worden alle mogelijke waarden voor `flex-wrap` getoond.

<iframe height='400' scrolling='no' title='Flexbox: flex-wrap' src='//codepen.io/lesso/embed/JeYQOr/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### justify-content

Met de `justify-content` eigenschap kan worden ingesteld hoe de items in een container moeten worden verdeeld over de **main-axis** en hoe er moet worden omgegaan met eventuele witruimte in de container. De standaardwaarde van `justify-content` is `flex-start` waarmee eventuele witruimte aan de rechtkant van de items terechtkomt. Andere mogelijke waarden voor deze eigenschap zijn: `flex-end` &#124; `center` &#124; `space-between` &#124; `space-around` &#124; `space-evenly`.

{% highlight css %}
.container {
  display: flex; 
  justify-content: center;
}
{% endhighlight %}

In onderstaand voorbeeld worden alle mogelijke waarden voor `justify-content` getoond.

<iframe height='400' scrolling='no' title='Flexbox: justify-content' src='//codepen.io/lesso/embed/GwpbGz/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### align-items

Met `align-items` kan worden ingesteld hoe items moeten worden geplaatst op de **cross-axis** op de huidige lijn. De default waarde hiervan is `stretch`, waardoor -standaard- de items alle beschikbare ruimte in de container zullen opvullen. We kunnen hier echter van afwijken door de waarde in te stellen op: `flex-end` &#124; `center` &#124; `flex-start` &#124; `baseline`.

{% highlight css %}
.container {
  display: flex; 
  align-items: center;
}
{% endhighlight %}

In onderstaand voorbeeld worden alle mogelijke waarden voor `align-items` getoond.

<iframe height='400' scrolling='no' title='Flexbox: align-items' src='//codepen.io/lesso/embed/eQJOBX/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### align-content

De `align-content` eigenschap bepaalt hoe **meerdere** lijnen van items worden verdeeld in de flexbox container wanneer er een overschot is aan witruimte. Ook bij deze eigenschap is de default waarde `stretch` waarbij de lijnen met items zich zullen strekken over alle beschikbare ruimte. De andere mogelijke waarden voor deze eigenschap zijn: `flex-start` &#124; `flex-end` &#124; `center` &#124; `space-between` &#124; `space-around`.

{% highlight css %}
.container {
  display: flex; 
  flex-wrap: wrap;
  align-content: center;
}
{% endhighlight %}

In onderstaand voorbeeld worden alle mogelijke waarden voor `align-content` getoond.

<iframe height='400' scrolling='no' title='Flexbox: align-content' src='//codepen.io/lesso/embed/VVeLGp/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

Flexbox **items** = children
----------------------------

Vervolgens zijn er nog een reeks eigenschappen die toepasbaar zijn op flexbox **items** elementen. Met andere woorden: de child elementen die als parent een flexbox **container** hebben.

### order

Standaard zullen alle flexbox items de volgorde hanteren die ze hebben gekregen in de html-code. We kunnen deze volgorde echter overrulen door gebruik te maken van de eigenschap `order`.

{% highlight css %}
.container {
  display: flex; 
}

.item1 {
  order: 2; 
}

.item2 {
  order: 1; 
}
{% endhighlight %}

In onderstaand voorbeeld zien we hoe van de standaard volgorde van items wordt afgeweken door gebruik te maken van `order` op de afzonderlijke items.

<iframe height='400' scrolling='no' title='Flexbox: order' src='//codepen.io/lesso/embed/KrdjgP/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### flex-grow

Met `flex-grow` kunnen we een bepaald flexbox item laten 'groeien' wanneer dit nodig zou blijken. Wanneer alle items de waarde '1' zouden krijgen voor de `flex-grow` eigenschap, zal alle ruimte in de flexbox container evenredig worden verdeeld over alle items. Passen we de waarde van `flex-grow` aan naar '2' voor één van de items, dan zal dit item dubbel zo veel beschikbare ruimte innemen.

{% highlight css %}
.container {
  display: flex; 
}

.item2 {
  flex-grow: 1; 
}
{% endhighlight %}

In onderstaand voorbeeld zien we hoe item 3 groeit ten opzichte van de rest door gebruik van `flex-grow`.

<iframe height='400' scrolling='no' title='Flexbox: flex-grow' src='//codepen.io/lesso/embed/NExbOL/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### flex-shrink

Met `flex-shrink` kunnen we het tegenovergestelde gedrag bekomen van `flex-grow`. Hierbij kunnen we bepaalde items laten 'krimpen' wanneer dit nodig zou zijn.

{% highlight css %}
.container {
  display: flex; 
}

.item2 {
  flex-shrink: 1; 
}
{% endhighlight %}

In onderstaand voorbeeld zien we hoe item 3 krimpt ten opzichte van de rest door gebruik van `flex-shrink`.

<iframe height='400' scrolling='no' title='Flexbox: flex-shrink' src='//codepen.io/lesso/embed/ZmQBNz/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### flex-basis

De `flex-basis` eigenschap kan worden ingezet om de grootte van een flexbox item in te stellen alvorens de beschikbare ruimte in de container zal worden verdeeld. Standaard heeft deze eigenschap de waarde `auto`, waarmee wordt gekeken naar de ingestelde `width` en `height`. De waarde kan de verschillende eenheden aannemen zoals %, px, em, etc. 

{% highlight css %}
.container {
  display: flex; 
}

.item2 {
  flex-basis: 200px; 
}
{% endhighlight %}

In onderstaand voorbeeld zien we hoe item 3 een aangepaste grootte krijgt toegewezen door gebruik te maken van `flex-basis`.

<iframe height='400' scrolling='no' title='Flexbox: flex-basis' src='//codepen.io/lesso/embed/wQMoVE/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### align-self

Met `align-self` kan de default positie van een flexbox item (zie eigenschap `align-items`) worden overschreven. We kunnen met andere woorden één of meerdere items er laten uitspringen.

{% highlight css %}
.container {
  display: flex;
  align-items: flex-end;
}

.item2 {
  align-self: center; 
}
{% endhighlight %}

In onderstaand voorbeeld zien we hoe item 3 telkens een andere positie toegewezen krijgt door gebruik te maken van `align-self`.

<iframe height='400' scrolling='no' title='Flexbox: align-self' src='//codepen.io/lesso/embed/aQdpZB/?height=407&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

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