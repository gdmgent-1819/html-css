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
