Padding *(Ned.: vulling)*
-------------------------

In **wijzerzin** vanaf boven:

 1. `padding-top:`{:.p} `«vulling-boven»`{:.v}
 2. `padding-right:`{:.p} `«vulling-rechts»`{:.v}
 3. `padding-bottom:`{:.p} `«vulling-onder»`{:.v}
 4. `padding-left:`{:.p} `«vulling-links»`{:.v}

In **shorthand** (wijzerzin van boven naar links):

> `padding:`{:.p} `«vulling-boven»`{:.v} `«vulling-rechts»`{:.v} `«vulling-onder»`{:.v} `«vulling-links»`{:.v}

{% highlight css %}
div {
    padding: 10px 2em 30% 4rem;
}
{% endhighlight %}

> `padding:`{:.p} `«vulling-boven»`{:.v} `«vulling-rechts-en-links»`{:.v} `«vulling-onder»`{:.v}

{% highlight css %}
div {
    padding: 10px 2em 30%;
    /* is hetzelfde als: */
    padding: 10px 2em 30% 2em;
}
{% endhighlight %}

> `padding:`{:.p} `«vulling-boven-en-onder»`{:.v} `«vulling-rechts-en-links»`{:.v}

{% highlight css %}
div {
    padding: 10px 2em;
    /* is hetzelfde als: */
    padding: 10px 2em 10px 2em;
}
{% endhighlight %}

> `padding:`{:.p} `vulling-rondom`{:.v}

{% highlight css %}
div {
    padding: 10px;
    /* is hetzelfde als: */
    padding: 10px 10px 10px 10px;
}
{% endhighlight %}

{% highlight css %}
.vierkant_binnen-ruimte {
    background-color: #BADA55;	
    width:200px;
    height:200px;
    padding: 20px;
    padding-left: 40px;
}
{% endhighlight %}