Universele selector
-------------------

> `*`{:.s} (asteri**sk**)
> 
> Selecteert **alle** elementen.

> Opgelet
> ---
> Pas deze selector spaarzaam toe, want het is zelden nodig.
>
> Een stijl toepassen op elk element verstoort de normale werking van de **cascade**.
{:.card.card-warning}

{% highlight css %}
* {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

Type-selector
-------------

> `«elementnaam»`{:.s.v}
>
> Selecteert **alle** HTML-elementen van dat **type** (de `«elementnaam»`{:.v}).

{% highlight css %}
h1, h2, h3, h4, h5, h6,
p {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

