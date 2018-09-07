Attribute-selector
------------------

> `[«naam»]`{:.s.v} (`[`…`]`, vierkante haken)
>
> Selecteert alle HTML-elementen die het **attribuut** met de naam `«naam»`{:.v} bevatten.

{% highlight css %}
[target] {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

{% highlight html %}
<a href="https://www.arteveldehogeschool.be" target="_self">Arteveldehogeschool</a>
<a href="https://http://www.arteveldeuniversitycollege.be" target="_blank">Artevelde University College Ghent</a>
{% endhighlight %}

Attribute&Value-selector
------------------------

> `[«naam»«operator»«waarde»]`{:.s.v} (`[`…`]`, vierkante haken)
>
> Selecteert alle HTML-elementen die het **attribuut** met de naam `«naam»`{:.v} bevatten die bovendien voldoet aan de **waarde** `«waarde»`{:.v} volgens de vereisten van de operator `«operator»`{:.v} .

| Operator | Betekenis                                                                                                |
|:--------:|----------------------------------------------------------------------------------------------------------|
|   `=`    | Exacte de waarde.                                                                                        |
|   `^=`   | Begint met de waarde.                                                                                    |
|   `|=`   | Begint met de waarde, maar enkel als het woord alleen staat of gevolgd wordt door een koppelteken (`-`). |
|   `*=`   | Bevat de waarde.                                                                                         |
|   `$=`   | Eindigt met de waarde.                                                                                   |
{:.table.table--primary}

In dit geval alle links met een `target`{:.a}-attribuut met de waarde `_blank`{:.v}

{% highlight css %}
a[target="_blank"] {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

Is van toepassing op:

{% highlight css %}
<a href="https://www.arteveldehogeschool.be" target="_blank">Arteveldehogeschool</a>
{% endhighlight %}

{% highlight css %}
a[href^="http"] {
    /* Hier komen de stijldeclaraties. */
}

img[src$=".svg"] {
    /* Hier komen de stijldeclaraties. */
}

p[class*="js"] {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}