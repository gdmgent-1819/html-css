Het HTML-element
----------------

> Opmerking
> ---
> HTML-elementen worden met **kleine letters** geschreven. 
{:.card.card-remark}

### Soorten HTML-elementen

#### Tweeledig

Tweeledige elementen en bestaan uit een **begintag** *(Eng.: opening tag)* en een **eindtag** *(Eng.: closing tag)*.

{% highlight html %}
<html> <!-- Begintag -->

</html> <!-- Eindtag -->
{% endhighlight %}

#### Zelfsluitend

Zelfsluitende elementen hebben maar een tag, een **zelfsluitende tag** *(Eng.: self-closing tag)*. 

{% highlight html %}
<meta> <!-- Zelfsluitend tag in HTML5 -->
{% endhighlight %}

Er is ook een XHTML-notatie (die de striktere regels van XML volgt) van die duidelijker is, maar tegenwoordig nog maar **weinig gebruikt** wordt.

{% highlight html %}
<meta /> <!--Zelfsluitend tag in XHTML5 -->
{% endhighlight %}

> Opmerking
> ---
> Zelfsluitende elementen hebben in XHTML een **forward slash** (`/`) als voorlaatste teken.
{:.card.card-remark}

> Opgelet
> ---
> - **HTML geniet de voorkeur** boven XHTML, omdat de code compacter is en ook omdat in de praktijk zelden perfecte XHTML-code geschreven werd.
> - XHTML en HTML mag je **niet mengen**.
{:.card.card-warning}