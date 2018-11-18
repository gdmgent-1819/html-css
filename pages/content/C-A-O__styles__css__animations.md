---
title: Animaties
title_long: Animaties
permalink: styles/css/animations/
published: true
---

## Begrip

In tegenstelling tot CSS transities, waar je meteen de nieuwe staat definieert, moet je bij CSS Animations eerst de animatie via de @keyframes stijlregel definiëren. 

Binnen de `@keyframes` stijlregel specifieer je op welke moment in de animatie er veranderingen in de stijlen moet plaatsvinden. Die momenten definieer je aan de hand van percentages (gaande van 0% tot 100%). Heb je een eenvoudige animatie met twee keyframes: '**0%** tot **100%**', dan kan dit ook vervangen worden door de woorden ‘**from**’ en ‘**to**’. 

Vervolgens koppel je deze animatie aan een element via de stijlregel ‘animation-name’.

## Properties

> - `animation-name`{:.p} De naam van de keyframe die je wil binden aan de selector
> - `animation-duration`{:.p} 	Hoeveel (milli)seconden de animatie zal duren voordat de animatie beëindigd is. 
> - `animation-timing-function`{:.p} 	De snelheidscurve van de animate
> - `animation-delay`{:.p} 	De wachttijd voordat de animatie mag starten
> - `animation-iteration-count`{:.p} 	Het aantal keer dat de animatie mag spelen
> - `animation-direction`{:.p} 	Specifieert in welke richting de animatie moet spelen (voorwaarts, achterwaarts, alternerend, ...)
> - `animation-fill-mode`{:.p} 	Specifies what values are applied by the animation outside the time it is executing
> - `animation-play-state`{:.p} 	Specifies whether the animation is running or paused
> - `animate`{:.p} shorthand-notatie


## Voorbeelden

### Voorbeeld 1, rijdende wagen
{% highlight css %}
/*  Definiëring van de animatie d.m.v. 2 of meer percentages. 0% is het begin van de animatie, 100% is het einde */
@keyframes autoRijden{
  0%{
    left:150px;
  }  100%{
    left:650px;
  }
}
/*  Koppelen van de animatie aan een klasse */
.animatie-auto{
  animation-name: autoRijden;
  animation-duration: 4s;
  animation-timing-function: ease-in-out;
  animation-fill-mode:forwards;
}
{% endhighlight %}


### Voorbeeld 2, #infiniteagangsta


<iframe height='265' scrolling='no' title='Animated DIV' src='//codepen.io/fredroeg/embed/bQoNPg/?height=265&theme-id=dark&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>


## animate.css

animate.css is een handige tool, boordevol vooraf gedefinieerde animaties die toepasbaar zijn op de html-elementen. In plaats van alle keyframes van de animaties zelf te definiëren, kan je door een class toe te voegen aan een element er een animatie aan toewijzen.

[BEKIJK ALLE ANIMATIES HIER](https://daneden.github.io/animate.css/)

**Bijvoorbeeld:**

{% highlight html linenos %}
<h1 class="animated infinite bounce delay-2s">Voorbeeld</h1>
{% endhighlight %}{:data-file="index.html"}

Op deze h1 zijn er een aantal classes toegepast:
> - `animated`{:.k} geeft aan dat het element een animatie moet krijgen
> - `infinite`{:.k} geeft aan dat de animatie oneindig lang moet loopen
> - `bounce`{:.k} is het type animatie
 > - `delay-2s`{:.k} er moet 2 seconden voorbijgaan alvorens de animatie start

<iframe height='265' scrolling='no' title='animate.css' src='//codepen.io/fredroeg/embed/QJqyRg/?height=265&theme-id=dark&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

### Mogelijke animaties

<table>
<thead>
<tr>
<th>Class Name</th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td><code>bounce</code></td>
<td><code>flash</code></td>
<td><code>pulse</code></td>
<td><code>rubberBand</code></td>
</tr>
<tr>
<td><code>shake</code></td>
<td><code>headShake</code></td>
<td><code>swing</code></td>
<td><code>tada</code></td>
</tr>
<tr>
<td><code>wobble</code></td>
<td><code>jello</code></td>
<td><code>bounceIn</code></td>
<td><code>bounceInDown</code></td>
</tr>
<tr>
<td><code>bounceInLeft</code></td>
<td><code>bounceInRight</code></td>
<td><code>bounceInUp</code></td>
<td><code>bounceOut</code></td>
</tr>
<tr>
<td><code>bounceOutDown</code></td>
<td><code>bounceOutLeft</code></td>
<td><code>bounceOutRight</code></td>
<td><code>bounceOutUp</code></td>
</tr>
<tr>
<td><code>fadeIn</code></td>
<td><code>fadeInDown</code></td>
<td><code>fadeInDownBig</code></td>
<td><code>fadeInLeft</code></td>
</tr>
<tr>
<td><code>fadeInLeftBig</code></td>
<td><code>fadeInRight</code></td>
<td><code>fadeInRightBig</code></td>
<td><code>fadeInUp</code></td>
</tr>
<tr>
<td><code>fadeInUpBig</code></td>
<td><code>fadeOut</code></td>
<td><code>fadeOutDown</code></td>
<td><code>fadeOutDownBig</code></td>
</tr>
<tr>
<td><code>fadeOutLeft</code></td>
<td><code>fadeOutLeftBig</code></td>
<td><code>fadeOutRight</code></td>
<td><code>fadeOutRightBig</code></td>
</tr>
<tr>
<td><code>fadeOutUp</code></td>
<td><code>fadeOutUpBig</code></td>
<td><code>flipInX</code></td>
<td><code>flipInY</code></td>
</tr>
<tr>
<td><code>flipOutX</code></td>
<td><code>flipOutY</code></td>
<td><code>lightSpeedIn</code></td>
<td><code>lightSpeedOut</code></td>
</tr>
<tr>
<td><code>rotateIn</code></td>
<td><code>rotateInDownLeft</code></td>
<td><code>rotateInDownRight</code></td>
<td><code>rotateInUpLeft</code></td>
</tr>
<tr>
<td><code>rotateInUpRight</code></td>
<td><code>rotateOut</code></td>
<td><code>rotateOutDownLeft</code></td>
<td><code>rotateOutDownRight</code></td>
</tr>
<tr>
<td><code>rotateOutUpLeft</code></td>
<td><code>rotateOutUpRight</code></td>
<td><code>hinge</code></td>
<td><code>jackInTheBox</code></td>
</tr>
<tr>
<td><code>rollIn</code></td>
<td><code>rollOut</code></td>
<td><code>zoomIn</code></td>
<td><code>zoomInDown</code></td>
</tr>
<tr>
<td><code>zoomInLeft</code></td>
<td><code>zoomInRight</code></td>
<td><code>zoomInUp</code></td>
<td><code>zoomOut</code></td>
</tr>
<tr>
<td><code>zoomOutDown</code></td>
<td><code>zoomOutLeft</code></td>
<td><code>zoomOutRight</code></td>
<td><code>zoomOutUp</code></td>
</tr>
<tr>
<td><code>slideInDown</code></td>
<td><code>slideInLeft</code></td>
<td><code>slideInRight</code></td>
<td><code>slideInUp</code></td>
</tr>
<tr>
<td><code>slideOutDown</code></td>
<td><code>slideOutLeft</code></td>
<td><code>slideOutRight</code></td>
<td><code>slideOutUp</code></td>
</tr>
<tr>
<td><code>heartBeat</code></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### Delay instellen

Om de animatie even uit te stellen, kan je een delay-class toevoegen aan het element. Let op, je kan maximaal tot 5 seconden uitstellen met behulp van de delay-class. Wil je een custom delay -> zie verderop bij **Custom Aanpassingen**

<table>
<thead>
<tr>
<th>Class Name</th>
<th>Delay Time</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>delay-2s</code></td>
<td><code>2s</code></td>
</tr>
<tr>
<td><code>delay-3s</code></td>
<td><code>3s</code></td>
</tr>
<tr>
<td><code>delay-4s</code></td>
<td><code>4s</code></td>
</tr>
<tr>
<td><code>delay-5s</code></td>
<td><code>5s</code></td>
</tr>
</tbody>
</table>

**voorbeelden**

{% highlight html linenos %}
<div class="animated jackInTheBox delay-5s">Example</div>
{% endhighlight %}{:data-file="index.html"}

<iframe height='361' scrolling='no' title='Trump doing the mexican wave' src='//codepen.io/fredroeg/embed/preview/mQBPWE/?height=361&theme-id=light&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>


### Traag, trager, snel, sneller

Je kan de animatie sneller of trager laten gaan door één van volgende classes toe te voegen:

<table>
<thead>
<tr>
<th>Class Name</th>
<th>Speed Time</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>slow</code></td>
<td><code>2s</code></td>
</tr>
<tr>
<td><code>slower</code></td>
<td><code>3s</code></td>
</tr>
<tr>
<td><code>fast</code></td>
<td><code>800ms</code></td>
</tr>
<tr>
<td><code>faster</code></td>
<td><code>500ms</code></td>
</tr>
</tbody>
</table>

**voorbeeld**

<iframe height='265' scrolling='no' title='RqLaRr' src='//codepen.io/fredroeg/embed/RqLaRr/?height=265&theme-id=light&default-tab=html,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>


### Custom aanpassingen

Het is mogelijk om de duration / delay / of aantal keer dat de animatie speelt, te wijzigen.

vb:

{% highlight css %}
.yourElement {
  animation-duration: 3s;
  animation-delay: 2s;
  animation-iteration-count: infinite;
}
{% endhighlight %}