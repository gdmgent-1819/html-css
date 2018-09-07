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

Indien er geen Ancestor-element een postionering heeft (een position anders dan static), dat wordt het absoluut gepositioneerd element ten opzichte van het browservenster gepositioneerd. Het element (rode paragraaf 4) verdwijnt uit de flow, zodat paragraaf 5 direct op paragraaf 3 volgt.


Indien een Ancestor-element zelf een position gekregen heeft anders dan static, dan wordt de rode paragraaf gepositioneerd ten opzichte van de inhoud + padding van dichtstbijzijnde het gepositioneerd Ancestor-element.

Met absolute positionering kan je ook elementen centreren: in de x-richting of y-richting of beide.