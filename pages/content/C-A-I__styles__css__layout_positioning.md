---
title: Lay-out position
title_long: Lay-out Flow - position
permalink: styles/css/layout/position
---

Lay-out en Flow
---------------

 1. Normal Flow
 1. Relative Positioning
 1. Absolute Positioning
 1. Fixed Positioning

> `position:`{:.p} `static`{:.k.d} &#124; `relative`{:.k} &#124; `absolute`{:.k} &#124; `fixed`{:.k}

Normal Flow
-----------

Bij de normal flow hebben alle elementen in css: `position:`{:.p} `static`{:.k.d}.

De standaardwaarde is `static`{:.k.d}.

Gebruik deze waarde enkel als de declaratie eerder overschreven werd.

{% highlight css %}
p {
    position: static;
}
{% endhighlight %}

{% comment %}
Alle paragrafen hebben een width: 400px. De rode paragraaf 4 volgt de normale flow.
{% endcomment %}

Relative Positioning
--------------------

Bij een relatieve positionering kan een offset (afwijking) ten opzichte van de ‘normale’ positie in de normale flow gedeclareerd worden.

Het element krijgt in css: 

`position: relative`

Bij conflict: top en left winnen?

{% highlight css %}
.gepositioneerd-1 {
    position: relative;
    left:  50px; /*offset x*/
    top : -10px; /*offset y*/
}

.gepositioneerd-2 {
    position: relative;
    right : 50px; /*offset x*/
    bottom: 10px; /*offset y*/
}
{% endhighlight %}


De rode paragraaf 4 is hier relatief gepositioneerd ten opzicht van de normale positie in de flow.

De offset is top: -10px en left: 50px

Absolute Positioning
--------------------

Bij een absolute positionering wordt het element uit de flow gehaald en met een offset ten opzichte van het dichtstbijzijnde Ancestor-element (omkoepelend element) met een positionering anders dan static geplaatst. (Op zoek naar offset parent.)

Het element krijgt in css: 
`position: absolute`

{% highlight css linenos %}
.gepositioneerd {
    position: absolute;
    right : 50px; /*offset x*/
    bottom: 10px; /*offset y*/
}
{% endhighlight %}{:data-file=".css"}

Indien er geen Ancestor-element een postionering heeft (een position anders dan static), dat wordt het absoluut gepositioneerd element ten opzichte van de body gepositioneerd. Het element (rode paragraaf 4) verdwijnt uit de flow, zodat paragraaf 5 direct op paragraaf 3 volgt.


Indien een Ancestor-element zelf een position gekregen heeft anders dan static, dan wordt de rode paragraaf gepositioneerd ten opzichte van de inhoud + padding van dichtstbijzijnde het gepositioneerd Ancestor-element.

Met absolute positionering kan je ook elementen centreren: in de x-richting of y-richting of beide.

Fixed Positioning
-----------------

Bij een fixed positionering wordt het element uit de flow gehaald en gepositioneerd ten opzichte van het browservenster.

In css:

`position: fixed`

{% highlight css %}
.gepositioneerd {
    position: fixed;
    right : 10px; /*offset x*/
    bottom: 10px; /*offset y*/
}
{% endhighlight %}

> Voorbeeld
> ---
> - [Fixed Positioning (1)]({{ '/examples/pages/04_fixed_positioning.html' | relative_url }})  
>   Het element is gepositioneerd ten opzichte van het browservenser
{:.card.card-example}


Sticky Positioning
------------------

Bij een sticky positionering staat het element in een normale flow. Na het overschrijden van een bepaalde drempel wordt het `fixed` gepositioneerd.

In css:

`position: sticky`

{% highlight css %}
.gepositioneerd {
    position: sticky;
    top: 8px; /*offset y*/
}
{% endhighlight %}

