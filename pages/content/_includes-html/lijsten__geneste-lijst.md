Geneste Lijst
-------------

> Definitie
> ---
> **Geneste lijsten** zijn een lijsten in lijsten.
{:.card.card-definition}

> Opgelet
> ---
> Een geneste lijst moet altijd tussen een `<li>`{:.e} … `</li>`{:.e} *(**List Item**)* staan, tussen de tekst.
{:.card.card-warning}

{% highlight html %}
<ul>
    <li>België:
        <ol>
            <li>Nederlands</li>
            <li>Frans</li>
            <li>Duits</li>
        </ol>
    </li>
    <li>Nederland:
        <ol>
            <li>Nederlands</li>
            <li>Fries</li>
        </ol>
    </li>
<ul>
{% endhighlight %}