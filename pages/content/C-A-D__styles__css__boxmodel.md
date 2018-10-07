---
title: Boxmodel
title_long: Boxmodel
permalink: styles/css/boxmodel/
---

> Zie ook
> ---
> - [W3C / CSS Box Model](https://www.w3.org/TR/CSS2/box.html)
{:.card.card-link}


Binnen &rarr; buiten:

 1. **Content** edge *(Ned.: inhoud)*  
   Vak dat de eigenlijke inhoud van het element omvat.
 2. **Padding** edge *(Ned.: vulling)*  
   Vak dat de vulling omvat.
 3. **Border** edge *(Ned.: rand)*  
   Vak dat de lijndikte omvat.
 4. **Margin** edge *(Ned.: marge)*  
   Vak dat de marge rond het element omvat.
 5. **Offset Positioning**  
   Afstand ten opzichte van de normale plaatsing.

{% include shared/figure.html src="https://www.gdm.gent/1718-webtech1/assets/img/content/box-model.svg" alt="Box Model en Offset Positioning" caption="Box Model en Offset Positioning" local=true %}


> Zie ook
> ---
> [CSS 2.1 Box Model](https://www.w3.org/TR/CSS2/box.html)
{:.card.card-link}

Elk element heeft een **box** *(Ned.: vak)* rond zich. Zowel block-level elementen als inline elementen.

Box Model *(Ned.: vakkenmodel)*
-------------------------------

### CSS Box Model + Offset Positioning

De inhoud heeft een `height:`{:.p} *(Ned.: hoogte)* en `width:`{:.p} *(Ned.: breedte).*

> Opgelet
> ---
> Hoogte en breedte kunnen bepaald worden door ingesloten elementen en eigenschappen van de inhoud.
{:.card.card-warning}

#### Visuele hoogte

{% highlight css %}
  border-top
+   padding-top
+     height
+   padding-bottom
+ border-bottom
{% endhighlight %}

> Opgelet
> ---
> **ZONDER** `margin-top`{:.p} en `margin-bottom`{:.p}!
{:.card.card-warning}

#### Visuele breedte

{% highlight css %}
  border-left
+   padding-left
+     width
+   padding-right
+ border-right
{% endhighlight %}

> Opgelet
> ---
> **ZONDER** `margin-left`{:.p} en `margin-right`{:.p}!
{:.card.card-warning}

> De **winterjas**metafoor
> ---
> Het is winter en **ik** (content met `height`{:.p} en `width`{:.p}, inhoud met hoogte en breedte)  
> heb warm door de **voering** (`padding`{:.p}, vulling)  
> van mijn **winterjas** (`border`{:.p}, rand).  
> Ik loop op **10 cm** (`margin`{:.p}, marge) van een pas geschilderde muur, dus moet ik opletten dat mijn jas niet vuil wordt.


### Invloed van Doctype op Box Model

De doctype heeft invloed op het gebruikte box model. Het **Quirks Mode** box model verschilt per browser, terwijl het **Standards Mode** box model overal hetzelfde zou moeten zijn.

Gebruik dus steeds een correct Doctype!

`<!DOCTYPE html>`{:.dt} of `<!doctype html>`{:.dt}

### Box Sizing

Je kan de standaard manier waarop de visuele afmetingen bepaald worden veranderen met:

> `box-sizing:`{:.p} `content-box`{:.k.d} &#124; `border-box`{:.k}

| Waarde               | `height`{:.p} en `width`{:.p} zijn de afmetingen van |
|----------------------|------------------------------------------------------|
| `content-box`{:.k.d} | enkel de inhoud.                                     |
| `border-box`{:.k}    | de som van inhoud + `padding`{:.p} + `border`{:.p}.  |
{:.table.table--primary}

Content *(Ned.: inhoud)*
------------------------

- `width:`{:.p} `«breedte»`{:.v}
- `height:`{:.p} `«hoogte»`{:.v}

Voor variabele afmetingen kan er ook nog een minimum- en/of maximumwaarde opgegeven worden.

 - `min-width:`{:.p} `«minimale-breedte»`{:.v}
 - `max-width:`{:.p} `«maximale-breedte»`{:.v}
 - `min-height:`{:.p} `«minimale-hoogte»`{:.v}
 - `max-height:`{:.p} `«maximale-hoogte»`{:.v}

{% highlight css %}
div {
    width: 100%;
    min-width: 180px;
    max-width: 960px;
}
{% endhighlight %}


{% highlight css %}
.vierkant {
    background-color: #BADA55;
    width : 200px;
    height: 200px;
}
{% endhighlight %}

Padding *(Ned.: vulling)*
-------------------------

In **wijzerzin** vanaf boven:

 1. `padding-top:`{:.p} `«vulling-boven»`{:.v}
 2. `padding-right:`{:.p} `«vulling-rechts»`{:.v}
 3. `padding-bottom:`{:.p} `«vulling-onder»`{:.v}
 4. `padding-left:`{:.p} `«vulling-links»`{:.v}

In **shorthand** (wijzerzin van boven naar links):

> `padding:`{:.p} `«vulling-boven»`{:.v} `«vulling-rechts»`{:.v} `«vulling-onder»`{:.v} `«vulling-links»`{:.v}

{% highlight css %}
div {
    padding: 10px 2em 30% 4rem;
}
{% endhighlight %}

> `padding:`{:.p} `«vulling-boven»`{:.v} `«vulling-rechts-en-links»`{:.v} `«vulling-onder»`{:.v}

{% highlight css %}
div {
    padding: 10px 2em 30%;
    /* is hetzelfde als: */
    padding: 10px 2em 30% 2em;
}
{% endhighlight %}

> `padding:`{:.p} `«vulling-boven-en-onder»`{:.v} `«vulling-rechts-en-links»`{:.v}

{% highlight css %}
div {
    padding: 10px 2em;
    /* is hetzelfde als: */
    padding: 10px 2em 10px 2em;
}
{% endhighlight %}

> `padding:`{:.p} `vulling-rondom`{:.v}

{% highlight css %}
div {
    padding: 10px;
    /* is hetzelfde als: */
    padding: 10px 10px 10px 10px;
}
{% endhighlight %}

{% highlight css %}
.vierkant_binnen-ruimte {
    background-color: #BADA55;	
    width:200px;
    height:200px;
    padding: 20px;
    padding-left: 40px;
}
{% endhighlight %}

Border *(Ned.: rand)*
---------------------

> - `border-width:`{:.p} `«randdikte»`{:.v} &#124; `thin`{:.k} &#124; `medium`{:.k} &#124; `thick`{:.k}
> - `border-style:`{:.p} `«randstijl»`{:.v} &#124; `solid`{:.k} &#124; `dashed`{:.k} &#124; `dotted`{:.k} &#124; …
> - `border-color:`{:.p} `«randkleur»`{:.v}
>
> Shorthand:
>
>  - `border:`{:.p} `«border-width»`{:.v} `«border-style»`{:.v} `«border-color»`{:.v}
>
> In **wijzerzin** van boven naar links:
>
>  1. `border-top:`{:.p} `«border-top-width»`{:.v} `«border-top-style»`{:.v} `«border-top-color»`{:.v}
>    - `border-top-width:`{:.p} `«randdikte»`{:.v}
>    - `border-top-style:`{:.p} `«randstijl»`{:.v}
>    - `border-top-color:`{:.p} `«randkleur»`{:.v}
>  2. `border-right:`{:.p} `«border-right-width»`{:.v} `«border-right-style»`{:.v} `«border-right-color»`{:.v}
>    - `border-right-width:`{:.p} `«randdikte»`{:.v}
>    - `border-right-style:`{:.p} `«randstijl»`{:.v}
>    - `border-right-color:`{:.p} `«randkleur»`{:.v}
>  3. `border-bottom:`{:.p} `«border-bottom-width»`{:.v} `«border-bottom-style»`{:.v} `«border-bottom-color»`{:.v}
>    - `border-bottom-width:`{:.p} `«randdikte»`{:.v}
>    - `border-bottom-style:`{:.p} `«randstijl»`{:.v}
>    - `border-bottom-color:`{:.p} `«randkleur»`{:.v}
>  4. `border-left:`{:.p} `«border-left-width»`{:.v} `«border-left-style»`{:.v} `«border-left-color»`{:.v}
>    - `border-left-width:`{:.p} `«randdikte»`{:.v}
>    - `border-left-style:`{:.p} `«randstijl»`{:.v}
>    - `border-left-color:`{:.p} `«randkleur»`{:.v}

#### Afrondingen

> - `border-radius:`{:.p} `«straal»`{:.v}
> - `border-radius:`{:.p} `«x-straal»`{:.v} `/` `«y-straal»`{:.v}
> - `border-radius:`{:.p} `«straal-linksboven»`{:.v} `«straal-rechtsboven»`{:.v} `«straal-rechtsonder»`{:.v} `«straal-linksonder»`{:.v}
>
> In **wijzerzin** van linksboven naar linksonder:
>
>  1. `border-top-left-radius:`{:.p} `«straal-linksboven»`{:.v}
>  2. `border-top-right-radius:`{:.p} `«straal-rechtsboven»`{:.v}
>  3. `border-bottom-right-radius:`{:.p} `«straal-rechtsonder»`{:.v}
>  4. `border-bottom-left-radius:`{:.p} `«straal-linksonder»`{:.v}

{% highlight html %}
<div class="voorbeelden">
    <div class="voorbeelden__vierkant"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--rand"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--dikke-bovenrand"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--ronde-hoeken"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--ronde-linker-bovenhoek"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--vlakgeronde-hoeken"></div>
</div>
{% endhighlight %}

{% highlight css linenos %}
.voorbeelden__vierkant {
    background-color: #BADA55;	
    height: 200px;
    width: 200px;
}

.voorbeelden__vierkant--rand {
    border: 1px solid #F00;
}

.voorbeelden__vierkant--dikke-bovenrand {
    border: 1px dashed #F00;
    border-top: 10px solid #00F;
}

.voorbeelden__vierkant--ronde-hoeken {
    border-radius: 10px;
}

.voorbeelden__vierkant--ronde-linker-bovenhoek {
    border-top-left-radius: 50px;
}

.voorbeelden__vierkant--vlakgeronde-hoeken {
    border-radius: 100px/20px;
}
{% endhighlight %}{:data-file="main.css"}

Margin *(Ned.: marge)*
----------------------

> Opgelet
> ---
> Een marge neemt nooit de achtergrondkleur van het element aan;  
> daarom behoort het niet tot de visuele afmetingen van het element.
{:.card.card-warning}

> In wijzerzin vanaf boven:
>
> 1. `margin-top:`{:.p} `«marge-boven»`{:.v}
> 2. `margin-right:`{:.p} `«marge-rechts»`{:.v}
> 3. `margin-bottom:`{:.p} `«marge-onder»`{:.v}
> 4. `margin-left:`{:.p} `«marge-links»`{:.v}
>
> In **shorthand** (wijzerzin van boven naar links):

`margin:`{:.p} `«marge-boven»`{:.v} `«marge-rechts»`{:.v} `«marge-onder»`{:.v} `«marge-links»`{:.v}

{% highlight css %}
div {
    margin: 10px 2em 30% 4rem;
}
{% endhighlight %}

`margin:`{:.p} `«marge-boven»`{:.v} `«marge-rechts-en-links»`{:.v} `«marge-onder»`{:.v}

{% highlight css %}
div {
    margin: 10px 2em 30%;
    /* is hetzelfde als: */
    margin: 10px 2em 30% 2em;
}
{% endhighlight %}

`margin:`{:.p} `«marge-boven-en-onder»`{:.v} `«marge-rechts-en-links»`{:.v}

{% highlight css %}
div {
    margin: 10px 2em;
    /* is hetzelfde als: */
    margin: 10px 2em 10px 2em;
}
{% endhighlight %}

`margin:`{:.p} `«marge-rondom»`{:.v}

{% highlight css %}
div {
    margin: 10px;
    /* is hetzelfde als: */
    margin: 10px 10px 10px 10px;
}
{% endhighlight %}

{% highlight css linenos %}
.voorbeelden__vierkant {
    background-color: #BADA55;	
    height: 200px;
    width: 200px;
}
.voorbeelden__vierkant--buiten-ruimte {
    margin: 15px;
    margin-right: 30px;
}
{% endhighlight %}{:data-file=""}

#### Collapsing Margins

> Zie ook
> ---
> - [CSS 2.1 Box Model Collapsing Margins](https://www.w3.org/TR/CSS2/box.html#collapsing-margins)
{:.card.card-link}

Als de **verticale marge** (`margin-top`{:.p} en `margin-bottom`{:.p}) van twee **aangrenzende vakken** *(Eng.: adjoining boxes)* tegen elkaar komen, dan wordt de marge samengesmolten tot een enkele marge die even groot is als de grootste (positieve) marge van de twee.

> Opgelet
> ---
> Er zijn een heel aantal uitzonderingen op deze algemene regel!
{:.card.card-warning}

<iframe height='265' scrolling='no' title='Collapsing Margins' src='//codepen.io/olivierparent/embed/VPrOMW/?height=265&theme-id=light&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/olivierparent/pen/VPrOMW/'>Collapsing Margins</a> by Olivier Parent (<a href='http://codepen.io/olivierparent'>@olivierparent</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

#### Centreren met Margin *(Ned.: marge)*

Een block-level element horizontaal centreren.

{% highlight css linenos %}
div {
    margin: 0 auto;
    width: 200px;
}
{% endhighlight %}{:data-file=""}

De waarde `auto`{:.k} heeft enkel in speciale gevallen een horizontaal effect, dus kan je ook dit gebruiken:

{% highlight css linenos %}
div {
    margin: auto;
    width: 200px;
}
{% endhighlight %}{:data-file=""}

> Opgelet
> ---
> Declareer ook steeds een `width`{:.p}, want *block-level* -elementen nemen anders de volledige breedte in beslag.
{:.card.card-warning}

{% highlight css linenos %}
.voorbeelden__vierkant {
    background-color: #BADA55;
    height: 200px;
    width: 200px;
}
.voorbeelden__vierkant--centraal {
    margin: 0 auto;
}
{% endhighlight %}{:data-file=""}
