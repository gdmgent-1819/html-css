---
title: CSS preprocessors
title_long: CSS preprocessors
permalink: styles/css-preprocessors/
published: true
---

Wat is een CSS preprocessor?
----------------------------

> Definitie
> ---
> CSS preprocessors zijn "scripting talen" om de CSS-taal uit te breiden met eigenschappen (Eng.: features) die standaard niet ondersteund worden door de CSS-taal. Ze voegen functinaliteit toe, die standaard niet bestaan in CSS, zoals: variabelen (Eng.: variables), nesten (Eng.: nesting), overerving (Eng.: inheritance), functies (Eng.: functions), operatoren (Eng.: operators), ... . Deze functionaliteiten zorgen ervoor dat de opmaak beter leesbaar, herbruikbaar (Eng.: Reusable), uitbreidbaar (Eng.: extensible) en beheersbaar (Eng.: maintainable), vooral bij grote en complexe projecten, zal worden.
{:.card.card-definition}

De CSS preprocessor talen hebben een **eigen unieke syntax** die **gecompileerd** (Eng.: compiled) of **geconverteerd** (Eng.: transpiled) moet worden naar reguliere "native" CSS-code. Deze talen vereisen dus dat er een CSS-compiler aanwezig actief is om hun eigen **syntax** te vertalen naar reguliere CSS.

> References
> ---
> - [Mozilla Developer Network: CSS preprocessor](https://developer.mozilla.org/en-US/docs/Glossary/CSS_preprocessor)
> - [ByteScout: Front-End Tooling Trends 2018 Plus…](https://bytescout.com/blog/front-end-trends-2018.html)
> - [Medium: CSS Preprocessors — Effective Tools for Faster Styling of Web Pages and User Interfaces](https://medium.com/@cabot_solutions/css-preprocessors-effective-tools-for-faster-styling-of-web-pages-and-user-interfaces-6ed4737a9804)
> - [Raygun: 10 Reasons to Use a CSS Preprocessor in 2018](https://raygun.com/blog/10-reasons-css-preprocessor/)
> - [Creative Bloq: Which is the best CSS preprocessor?](https://www.creativebloq.com/features/best-css-preprocessor)
> - [Wikipedia: Sass (stylesheet language)](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
{:.card.card-source}


Populaire CSS preprocessors
---------------------------

De meest populaire CSS preprocessors zijn:

- [Sass language](http://sass-lang.com/)
- [Less language](http://lesscss.org/)
- [Stylus language](http://stylus-lang.com/)
- [PostCSS language](http://postcss.org/)

Reguliere CSS
-------------

### Variabelen

In reguliere CSS kunnen we gebruik maken van variabelen. In tegenstelling tot variabelen in CSS preprocessors bevatten variabelen in regulaire CSS "scope".

{% highlight css %}
:root {
	--color-blue: #0052CC;
}

body {
	background-color: var(--color-blue);
}
{% endhighlight %}

CSS variabelen worden aangeduid met `--`(Eng.: double hyphen) en worden meestal geplaatst in de selector `:root`. Dit betekent dat deze variabelen globaal toegankelijk zijn binnen alle gekoppelde CSS-bestanden. Definiëren we een variabele binnen een bepaalde selector, bijvoorbeeld: `.article`, dan is deze variabele toegankelijk door deze selector en de geneste selectoren.

{% highlight html %}
<div class="article">
	<h1 class="article__title">
		NMD like Graphics love Code
	</h1>
</div>
<p class="jumbotron">dfjkjdlfjdlk</p>
{% endhighlight %}

{% highlight css %}
.article {
	--article-font-size: 44px;
}
.article > .article__title {
	font-size: var(--article-font-size);
}

.jumbotron {
	font-size: var(--article-font-size);
}
{% endhighlight %}

De selector `.article__title` heeft toegang tot de variabele `--article-font-size`. De selector `.jumbotron` heeft geen toegang tot deze variabele, omdat deze niet is toegekend aan één van de kinderen binnen het `article`-element.

{% highlight css %}
.headline {
    color: var(--base-text-color);
	font-size: var(--base-font-size, 16px);
}
{% endhighlight %}

Wat gebeurt er indien een variabele niet gedeclareerd is en we deze toch toekennen aan een CSS-eigenschap? `--base-text-color` is niet gedefinieerd binnen CSS. In dit geval zal de `color`-eigenschap de waarde `black` bevatten. `black` is het standaard kleur. De browser kijkt eigenlijk naar de boomstructuur van het document en gaat op zoek, steeds op een hoger niveau, naar de `color`-eigenschap. Wordt er één gevonden, dan zal hij de waarde hiervan toekennen als waarde van de `color`-eigenschap binnen de `headline`-selector.



> References
> ---
> - [Mozilla Developer Network: Using CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_variables)
> - [W3C: CSS Custom Properties for Cascading Variables Module Level 1](https://www.w3.org/TR/css-variables/)
{:.card.card-source}