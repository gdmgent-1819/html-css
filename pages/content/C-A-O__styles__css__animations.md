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
  }
  100%{
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


### Voorbeeld 2, Gangsta is rolling infinitely



<iframe height='265' scrolling='no' title='Animated DIV' src='//codepen.io/fredroeg/embed/bQoNPg/?height=265&theme-id=dark&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>


## animate.css