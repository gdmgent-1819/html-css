Samengestelde Selectors
-----------------------

Je kan de basisselectors samenstellen in deze volgorde:

 1. Eerst: Type-selector.
 2. In willekeurige volgorde: `id`{:.a}-selector, `class`{:.a}-selector(s), Attribute-selector(s) en/of Pseudo Class-selector(s).
 3. Laatst: Pseudo Element-selector.

{% highlight html linenos %}
<nav>
    <a class="nav__item nav__item--primary" href="#" target="_self">lorem ipsum</a>
    <a class="nav__item nav__item--primary" href="#" target="_self">dolor sit</a>
    <a class="nav__item nav__item--primary nav__item--selected" href="#" target="_self">amet consectetur</a>
    <a class="nav__item nav__item--primary" href="#" target="_self">adipisicing elit</a>
    <a class="nav__item nav__item--primary" id="link" href="#" target="_self">maiores nostrum</a>
    <a class="nav__item nav__item--primary" href="#" target="_self">iusto eius</a>
</nav>
{% endhighlight %}{:data-file=""}

{% highlight css linenos %}
a {
  display: block;
  font-family: sans-serif;
  text-decoration: none; 
}
a.nav__item:nth-child(2)[target].nav__item--primary[href="#"]::first-letter {
  text-transform: uppercase;
}
a:hover[target].nav__item#link::before {
  content: '→ '
}
{% endhighlight %}{:data-file=""}

Is van toepassing op:

{% highlight html %}
    <a class="nav__item nav__item--primary nav__item--selected" href="#" target="_self">amet consectetur</a>
    <a class="nav__item nav__item--primary" id="link" href="#" target="_self">maiores nostrum</a>
{% endhighlight %}