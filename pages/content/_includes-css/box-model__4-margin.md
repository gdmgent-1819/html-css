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
