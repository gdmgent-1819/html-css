---
title: Syntaxis
title_long: Syntaxis van CSS
permalink: styles/css/syntax/
---

CSS-regelset
------------

Een regelset bestaat uit:

  1. Een of meer **selectors** gescheiden door een **komma** *(Eng.: comma)* (`,`)
  2. **declaratieblok** *(Eng.: declaration block)* afgebakend met **accolades** *(Eng.: curly braces)* (`{`…`}`) met daartussen:
     - Een of meer **declaraties** *(Eng.: declarations)*  
       Een declaratie bestaat uit:
       1. een **eigenschap** *(Eng.: property)* gevolgd door een **dubbelepunt** *(Eng.: colon)* (`:`)
       2. een **waarde** *(Eng.: value)* gevolgd door een **puntkomma** *(Eng.: semicolon)* (`;`)

> Tip
> ---
> **Commentaar** schrijf je tussen `/*` en `*/` in CSS.
{:.card.card-tip}

{% highlight css linenos %}
/* Dit is een commentaarregel */
html,
body {
    font-family: Verdana, sans-serif;
    background: pink;
    /* Dit is nog een commentaarregel. */
}
{% endhighlight %}

CSS Toevoegen
-------------

- Inline *(Bad Practice)*
- Embedded (op paginaniveau)
- Externe stylesheet (op websiteniveau) 

### Inline (Bad Practice)

{% highlight html linenos %}
<p style="background-color: green;"> 
    Dit is tekst die op een groene achtergrondkleur te lezen is.
</p>
{% endhighlight %}

### Embedded (op paginaniveau)

{% highlight html %}
<head>
    <style>
        p {
            background-color: green; 
        }
    </style>
</head> 
<body>
    <p>Hier staat wat tekst.</p> 
</body>
{% endhighlight %}

### Externe stylesheet (op websiteniveau)

Gebruik externe stylesheets. Stop ze altijd op dezelfde plaats.

{% highlight html %}
<head>
    <link rel="stylesheet" href="css/style.css">
</head> 
<body>
    <p>Hier komt wat tekst.</p> 
</body>
{% endhighlight %}

> Mappen & Bestanden
> ---
> - projectmap/
>   - images/
>   - css/
>       - style.css
>   - index.html
{:.card.card-tree}