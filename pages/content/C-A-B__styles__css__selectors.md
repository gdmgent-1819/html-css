---
title: Selectoren
title_long: Selectoren
permalink: styles/css/selectors/
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