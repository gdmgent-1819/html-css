---
title: Selectoren
title_long: Selectoren
permalink: styles/css/selectors/
---


Wat doet een selector?
----------------------

Met een **selector** selecteer je bepaalde elementen in de **DOM** van een webpagina. Op de selectie kan je vervolgens een bepaalde stijl toepassen.

Meerdere selectoren kunnen dezelfde **declaraties** (`{…}`) gebruiken. De selectoren scheid je dan met een **komma** (`,`).

Basisselectors
--------------
 
 1. Universal-selector
 1. Type selector
 1. `class`{:.a}-selector
 1. `id`{:.a}-selector
 1. Attribute-selector
 1. Attribuut-en-waarde-selector
 1. Pseudo Class-selector
 1. Pseudo Element-selector

Combinators
-----------
 1. Descendant-combinator
 1. Child-combinator
 1. Sibling-combinator
 1. General Sibling-combinator

Universele selector
-------------------

> `*`{:.s} (asteri**sk**)
> 
> Selecteert **alle** elementen.

> Opgelet
> ---
> Pas deze selector spaarzaam toe, want het is zelden nodig.
>
> Een stijl toepassen op elk element verstoort de normale werking van de **cascade**.
{:.card.card-warning}

{% highlight css %}
* {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

Type-selector
-------------

> `«elementnaam»`{:.s.v}
>
> Selecteert **alle** HTML-elementen van dat **type** (de `«elementnaam»`{:.v}).

{% highlight css %}
h1, h2, h3, h4, h5, h6,
p {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}


`class`{:.a}-selector
---------------------

> `.«klassenaam»`{:.s.v} (`.`, punt)
>
> Selecteert **alle** HTML-elementen die de **klasse** hebben in het `class`{:.a}-attribuut.

{% highlight css %}
.mijn-class,
.mijn-andere-class {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

`id`{:.a}-selector
------------------

> `#«id-naam»`{:.s.v} (`#`, hekje)
>
> Selecteert **het** HTML-element dat deze `id`{:.a} (**identifier**) heeft in het `id`{:.a}-attribuut.

> Opmerking
> ---
> Een `id`{:.a} identificeert een bepaald HTML-element op een pagina. Per webpagina kan **maar 1 element** die bepaalde `id`{:.a} hebben.
{:.card.card-remark}

{% highlight css %}
#mijn-id,
#mijn-andere-id {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}





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

Pseudo Class-selector
---------------------

> `:«pseudo-class»`{:.s.v} (`:`, dubbelepunt)
>
> Selecteert de elementen waarop de pseudo class van toepassing is.

{% highlight css %}
a:link,
a:hover,
a:visited,
a.unselected:active {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

Selecteert de `<a>`{:.e}-elementen volgens toestand:

| Selector                                 | Betekenis                                               |
|------------------------------------------|---------------------------------------------------------|
| `:link`{:.s}                             | Nog niet bezochte hyperlink.                            |
| `:visited`{:.s}                          | Bezochte hyperlink.                                     |
| `:hover`{:.s}                            | Als er over de hyperlink gezweefd wordt.                |
| `:active`{:.s}                           | Terwijl er op hyperlink geklikt wordt.                  |
|------------------------------------------|---------------------------------------------------------|
| `:checked`{:.s}                          | Aangevinkte of geselecteerde formulierelementen.        |
| `:disabled`{:.s}                         | Uitgeschakelde formulierelementen.                      |
| `:selected`{:.s}                         | Geselecteerde formulierelementen.                       |
|------------------------------------------|---------------------------------------------------------|
| `:first-child`{:.s}                      | Eerste child-element.                                   |
| `:nth-child(«geheel-getal»)`{:.s}        | Het *n*-de child-element, bv. 4de.                      |
| `:last-child`{:.s}                       | Laatste child-element.                                  |
| `:nth-last-child(«geheel-getal»)`{:.s}   | Het *n*-de laatste child-element, bv. 4de.              |
|------------------------------------------|---------------------------------------------------------|
| `:first-of-type`{:.s}                    | Eerste child-element van dat type.                      |
| `:nth-of-type(«geheel-getal»)`{:.s}      | Het *n*-de child-element van dat type, bv. 4de.         |
| `:last-of-type`{:.s}                     | Laatste child-element van dat type.                     |
| `:nth-last-of-type(«geheel-getal»)`{:.s} | Het *n*-de laatste child-element van dat type, bv. 4de. |
{:.table.table--primary}

> Opmerking
> ---
> "Hover" (van het werkwoord 'to hover', Ned.: zweven) spreek je uit als 'hovver', met een korte 'o'.
>
> Het werkwoord 'to hoover' (met lange 'o') betekent stofzuigen en verwijst naar het stofzuigermerk [Hoover](https://www.hoover.com).
{:.card.card-remark}

> Zie ook
> ---
> Verschil tussen `:nth-child(«geheel-getal»)`{:.s} en `:nth-of-type(«geheel-getal»)`{:.s} 
> - [The Difference Between :nth-child and :nth-of-type](https://css-tricks.com/the-difference-between-nth-child-and-nth-of-type)
{:.card.card-link}

{% highlight css %}
input[type="checkbox"]:checked,
input[type="radiobutton"]:checked,
input:disabled,
option:selected {
    /* Hier komen de stijldeclaraties. */
}
{% endhighlight %}

> Zie ook
> ---
> - [Developer Mozilla: Pseudo Class Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
{:.card.card-link}

Pseudo Element-selector
-----------------------

> `::«pseudo-element»`{:.s.v} (`::`, 2 × dubbelepunt)
>
> Selecteert het **Pseudo Element** dat bij het HTML-element hoort.

| Selector                             | Betekenis                                               |
|--------------------------------------|---------------------------------------------------------|
| `::after`{:.s}                       | Virtueel laatste child-element.                         |
| `::before`{:.s}                      | Virtueel eerste child-element.                          |
|--------------------------------------|---------------------------------------------------------|
| `::first-letter`{:.s}                | Eerste teken van een block.                             |
| `::first-line`{:.s}                  | Eerste lijn van een block.                              |
|--------------------------------------|---------------------------------------------------------|
| `::selection`{:.s}                   | Geselecteerde inhoud (bv. met de muis) van een element. |
{:.table.table--primary}

{% highlight css %}
p::before,
h1::after,
p::selection {
    /* Hier komen de stijldeclaraties */
}
{% endhighlight %}

> Zie ook
> --- 
> - [Developer Mozilla: Pseudo Element Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)
{:.card.card-link}

### Voorbeeld 

<iframe height='358' scrolling='no' title='CSS Pseudo Classes / Pseudo Selectors' src='//codepen.io/fredroeg/embed/EbRbNP/?height=358&theme-id=light&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/fredroeg/pen/EbRbNP/'>CSS Pseudo Classes / Pseudo Selectors</a> by Frederick Roegiers (<a href='https://codepen.io/fredroeg'>@fredroeg</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

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

Stijlvoorrang
-------------

> References
> ---
> - [Mozilla Developer Network: Cascade and inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)
{:.card.card-source}



> De **voorrang** van een stijl wordt bepaald door:
>
> 1. **Belangrijkheid** van de declaratie.
> 2. **Specificiteit** van de selector.
> 3. **Volgorde** van de declaraties.

### Volgorde

 - De laatste declaratie heeft voorrang op eerdere declaraties.
 - De laatste declaratie overschrijft de voorgaande.

### Specificiteit

#### Specificiteit van de selector.

Specifiekere selectors hebben voorrang op minder specifieke selectors.

Bij benadering kan je stellen:

 - Hoe minder elementen je met de selector kan selecteren, hoe specifieker.
 - Stijlen in een style-attribuut zijn het meest specifiek, want zijn enkel maar voor dat element.

### Belangrijkheid

Door `!important`{:.k} na de waarde toe te voegen dwing je voorrang af.

Gebruik dit enkel in uiterste nood, want omzeilt de normale ‘Cascade’, wat een *bad practice* is.

{% highlight css linenos %}
body {
    color: blue !important;
    color: red;
}
{% endhighlight %}{:data-file=""}

Voorrangscijfer
---------------

Cijfer voor de voorrang van een stijl: `0,0,0,0,0`

Berekening:

 1. **!**: wordt een `!important`{:.k} toegepast op de declaratie? (ja: `1`, nee: `0`)
 2. **S**: staat de declaratie in een `style`-attribuut? (ja: `1`, nee: `0`)
 3. **I**: aantal `id`-selectors (`#`{:.s})
 4. **C**: aantal `class`- (`.`{:.s}), Pseudo Class- (`:`{:.s}) en Attribute-selectors (`[]`{:.s})
 5. **T**: aantal Type-selectors (Element-selector of Pseudo Element-selector (`::`{:.s}))

| !                 | S               | I                   | C                          | T                           |
|:-----------------:|:---------------:|:-------------------:|:--------------------------:|:---------------------------:|
| `!important`{:.k} | `style=""`{:.a} | `#«id-naam»`{:.s.v} | `.«klassenaam»`{:.s.v}     | `element`{:.s.v}            |
|                   |                 |                     | `:«pseudo-class»`{:.s.v}   | `::«pseudo-element»`{:.s.v} |
|                   |                 |                     | `[«attribuut»]`{:.s.v}     |                             |
|===================|=================|=====================|============================|=============================|
| `1` of `0`        | `1` of `0`      | aantal: `0`         | aantal: `0`                | aantal: `0`                 |
{:.table.table--primary}

Voorbeelden:

|  Selector of inline style                            |  !  |  S  |  I  |  C  |  T  |   Cijfer   |
|:-----------------------------------------------------|:---:|:---:|:---:|:---:|:---:|:----------:|
| `p { color: #F00; }`                                 | `0` |  -  | `0` | `0` | `1` | `0,0,0,0,1`|
| `p::selection { color: #FF0; }`                      | `0` |  -  | `0` | `0` | `2` | `0,0,0,0,2`|
| `p.belangrijk {}`                                    | `0` |  -  | `0` | `1` | `1` | `0,0,0,1,1`|
| `p#allereerste-alinea {}`                            | `0` |  -  | `1` | `0` | `0` | `0,0,1,0,0`|
| `head + body > h1#hoofd1 + p.belangrijk > a:link {}` | `0` |  -  | `1` | `2` | `5` | `0,0,1,2,5`|
| `<p style="color: #F00">`                            | `0` | `1` |  -  |  -  |  -  | `0,1,0,0,0`|
| `<p style="color: #0F0 !important">`                 | `1` | `1` |  -  |  -  |  -  | `1,1,0,0,1`|
| `p { color: #00F !important }`                       | `1` |  -  | `0` | `0` | `1` | `1,0,0,0,1`|
{:.table.table--primary.table--bordered}

> Zie ook
> ---
> <https://specificity.keegan.st>
{:.card.card-book}