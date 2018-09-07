Descendant-combinator
---------------------

> `«voorouder» «nakomelingen»`{:.s} (` `, (spatie))
>
> Selecteert **nakomelingen** (kinderen, kleinkinderen, achterkleinkinderen, achterachterkleinkinderen …).

{% highlight css %}
div span,
p a,
.mijn-class div span {
    /* … */
}
{% endhighlight %}

Selecteert alle descendant-elementen die voldoen aan de selector.

Child-combinator
----------------

> `«ouder» > «kinderen»`{:.s} (`>`, groter dan-teken)
>
> Selecteert **directe nakomelingen** (kinderen).

{% highlight css %}
div > span,
p > a,
.mijn-class > div > span {
    /* … */
}
{% endhighlight %}

Selecteert alle child-elementen (directe descendants) die voldoen aan de selector.

Adjacent Sibling-combinator
---------------------------

> `«oudere-broer-of-zus» + «jongere-broer-of-zus»`{:.s} (`+`, plusteken)
>
> Selecteert **de jongere** broer of zus die **direct volgt**.

{% highlight css %}
h1 + p {
    /* … */
}
{% endhighlight %}

Het eerste sibling-element dat na het element komt en voldoet aan de selector. (`<p>`{:.e} die direct op de `<h1>`{:.e} volgt)

General Sibling-combinator
--------------------------

> `«oudere-broer-of-zus» ~ «jongere-broers-of-zussen»`{:.s} (`~`, tilde)
>
> Selecteert **alle jongere** broers of zussen.

{% highlight css %}
a.geselecteerd ~ a {
    /* … */
}
{% endhighlight %}

De sibling-elementen die na het element komen en voldoen aan de selector.

(alle volgende `<a>`{:.e}-sibling-elementen na `<a>`{:.e}-elementen met de klasse `.geselecteerd`{:.s}, moet niet direct opvolgend zijn)

<p data-height="265" data-theme-id="light" data-slug-hash="ZBqVJJ" data-default-tab="css,result" data-user="olivierparent" data-embed-version="2" data-pen-title="ZBqVJJ" class="codepen">See the Pen <a href="http://codepen.io/olivierparent/pen/ZBqVJJ/">ZBqVJJ</a> by Olivier Parent (<a href="http://codepen.io/olivierparent">@olivierparent</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>