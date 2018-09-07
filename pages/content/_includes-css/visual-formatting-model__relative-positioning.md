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