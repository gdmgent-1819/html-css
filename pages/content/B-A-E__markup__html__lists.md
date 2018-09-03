---
title: Lijsten
title_long: Lijsten
permalink: markup/html/lists/
---

Ongeordende lijst
-----------------

> Definitie
> ---
> Een **ongeordende lijst** is een lijst van **elementen** waarvan de volgorde **niet** van belang is.
{:.card.card-definition}

 - `<ul>`{:.e} … `</ul>`{:.e} *(`ul`: **Unordered List**)* is een *descendant* van `<body>`{:.e}.
 - Bevat een of meerdere *children:* `<li>`{:.e} … `</li>`{:.e} *(**List Item**).*

{% highlight html %}
<ul lang="nl">
    <li lang="en">English</li>
    <li>Nederlands</li>
</ul>
{% endhighlight %}

Geordende lijst
---------------

> Definitie
> ---
> Een **Geordende lijst** is een lijst van **elementen** waarvan de volgorde **wel** van belang is.
{:.card.card-definition}

 - `<ol>`{:.e} … `</ol>`{:.e} *(**Ordered List**)* is een *descendant* van `<body>`{:.e}.
 - Bevat een of meerdere *children:* `<li>`{:.e} … `</li>`{:.e} *(**List Item**).*

{% highlight html %}
<ol>
    <li>English</li>
    <li>Nederlands</li>
</ol>
{% endhighlight %}

> Opmerking
> ---
> Je kan de beginwaarde van de nummering instellen met het attribuut `start=""`{:.a} op de `<ol>`{:.e}
{:.card.card-remark}

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

Lijst van beschrijvingen
------------------------

 - `<dl>`{:.e} … `</dl>`{:.e} *(**Description List**)* is een *descendant* van `<body>`{:.e}
 - Bevat een of meerdere *children:* `<dt>`{:.e} … `</dt>`{:.e} *(**Description Term**)*  
   die onmiddellijk gevolgd worden door een of meerdere `<dd>`{:.e} … `</dd>`{:.e} *(**Description Data**).* 

{% highlight html %}
<dl>
    <dt>Hypertext Transfer Protocol</dt>
    <dd>Protocol voor webcommunicatie.</dd>
    <dd>Afgekort als <abbr title="Hypertext Transfer Protocol">HTTP</abbr>.</dd>
    <dt>Hypertext Transfer Protocol Secure</dt>
    <dd>Protocol voor webcommunicatie over een beveiligde verbinding.</dd>
    <dd>Afgekort als <abbr title="Hypertext Transfer Protocol Secure">HTTPS</abbr>.</dd>
</dl>
{% endhighlight %}