
### **I**talic

`<i>` … `</i>`

Wordt gebruikt om tekst cursief te zetten, zonder speciale betekenis.

> ##### **Opmerking** :point_up:
> ---
> - Vermijd dit element!
> - Je gebruikt beter `<em>` of CSS!
{:.alert.alert-info}

- Een descendant van `<body>`

Verkorte schrijfwijze van:

{% highlight html %}
<span style="font-style: italic"> … </span>
{% endhighlight %}

**Strong** importance *(sterke nadruk)*
---------------------------------------

`<strong>` … `</strong>`

Wordt gebruikt om sterke nadruk te leggen op bepaalde woorden.

 - De standaardopmaak is vet.
 - Een descendant van `<body>`

**B**old *(vet)*
----------------

`<b>` … `</b>`

Wordt gebruikt om tekst vet te zetten, zonder speciale betekenis.

 - Een descendant van `<body>`

> ##### **Opmerking** :point_up:
> ---
> - Vermijd dit element!
> - Je gebruikt beter `<strong>` of CSS!
{:.alert.alert-info}

Verkorte schrijfwijze van:

{% highlight html %}
<span style="font-weight: bold"> … </span>
{% endhighlight %}

**Code** *(programmeercode)*
----------------------------

`<code>` … `</code>`

Wordt gebruikt om code in de inhoud te zetten

- Een descendant van `<body>`
- Standaard wordt een monospace lettertype gebruikt.

{% highlight html %}
<code>&lt;meta&gt;</code>
{% endhighlight %}

Ziet er dan zo uit:

<code>&lt;meta&gt;</code>

**Pre**formatted text *(voorgeformateerde tekst)*
-------------------------------------------------

`<pre>` … `</pre>`

Wordt gebruikt om de witruimte van voorgeformaatterde tekst te behouden.

- Een descendant van `<body>`
- Standaard wordt een monospace lettertype gebruikt.
