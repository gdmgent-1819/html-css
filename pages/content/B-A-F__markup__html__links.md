---
title: Links
title_long: Links
permalink: markup/html/links/
---

**A**nchor *(Ned.: anker)*
--------------------------
`<a>`{:.e} … `</a>`{:.e}

Wordt gebruikt om een hyperlink te maken naar een andere webpagina of om naar een bepaald element te verspringen in een webpagina.

Een descendant van `<body>`{:.e}

{% highlight html %}
<a href="http://www.google.be">Google</a>
{% endhighlight %}

> Opmerkingen
> ---
> - Een koppeling in de `<head>`{:.e} gebeurt **altijd** met een `<link href="" rel="">`{:.e}, bijv. een CSS-bestand.
> - Een koppeling in de `<body>`{:.e} gebeurt **altijd** met een `<a href=""></a>`{:.e}
> - Een koppeling naar een JavaScript-bestand gebeurt altijd met een `<script src=""></script>`{:.e} en dat kan zowel in de `<head>`{:.e} als de `<body>`{:.e}.
> - Bij `<link>`{:.e} en `<a>`{:.e} via een `href`{:.a} *(Hypertext Reference),* terwijl het bij een `<script>`{:.e} via een `src`{:.a} *(Eng.: **s**ou**rc**e, Ned.: bron)* gebeurt.
{:.card.card-remark}

| Attibuut      | Waarde         | Betekenis                                                           |
|---------------|----------------|---------------------------------------------------------------------|
| `href`{:.a}   | `#«id»`{:.v}   | Scroll naar het element met de ID `«id»`{:.v}.                      |
|               | `«uri»`{:.v}   | Ga naar de URI `«uri»`{:.v} (meestal een webpagina of een document) |
|---------------|----------------|---------------------------------------------------------------------|
| `target`{:.a} | `_self`{:.k.d} | Open in hetzelfde venster of tabblad. (Standaard)                   |
|               | `_blank`{:.k}  | Open in een nieuw venster of tabblad.                               |
{:.table.table--primary}