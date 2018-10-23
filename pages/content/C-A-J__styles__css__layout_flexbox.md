---
title: Lay-out flexbox
title_long: Lay-out flexbox
permalink: styles/css/layout/flexbox
published: false
---

CSS Flexible Box Layout
-----------------------

> Zie ook
> ---
> - [MDN: CSS Flexible Boxes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes)
> - [Flexbox Froggy](http://flexboxfroggy.com)
> - [Flexbox Playground](https://demo.agektmr.com/flexbox/)
> - [Flexy Boxes](http://the-echoplex.net/flexyboxes/)
> - [W3C / CSS Flexible Box Layout Module](https://www.w3.org/TR/css-flexbox/)
> - [CSS Tricks / A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
{:.card.card-book}

### Flex Container (parent-element)

> - `display:`{:.p} `flex`{:.k} &#124; `inline-flex`{:.k}
> - `justify-content:`{:.p} `flex-start`{:.k.d} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `space-between`{:.k} &#124; `space-around`{:.k} &#124; `space-evenly`{:.k} 
>   Uitlijning op de **main-axis** (in de richting van de `flex-direction`{:.p}).
> - `align-items:`{:.p} `flex-start`{:.k} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `baseline`{:.k} &#124; `stretch`{:.k.d}  
>   Uitlijning op de **cross-axis** (dwars op de richting van de `flex-direction`{:.p}).  
>   `row`: van boven naar onder  
>   `column`: in de schrijfrichting, afhankelijk of het HTML-attribuut `dir`{:.a}  de waarde `ltr`{:.k} of `rtl`{:.k} is.
> - `align-content:`{:.p} `flex-start`{:.k.d} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `space-between`{:.k} &#124; `space-around`{:.k}  &#124; `stretch`{:.k}  
>    Uitlijning op de **cross-axis**, vergelijkbaar met `justify-content`{:.p}.  
>    Heeft enkel effect met een `flex-wrap:`{:.p} `wrap`{:.k} of `wrap-reverse`{:.k}
> - `flex-flow:`{:.p} `«flex-direction»`{:.v} `«flex-wrap»`{:.v}
>    1. `flex-direction:`{:.p} `row`{:.k.d} &#124; `row-reverse`{:.k} &#124; `column`{:.k} &#124; `column-reverse`{:.k}
>    2. `flex-wrap:`{:.p} `nowrap`{:.k.d} &#124; `wrap`{:.k} &#124; `wrap-reverse`{:.k}

### Flex Items (child-elementen)

> - `align-self:`{:.p} `auto`{:.k.d} &#124; `flex-start`{:.k} &#124; `flex-end`{:.k} &#124; `center`{:.k} &#124; `baseline`{:.k} &#124; `stretch`{:.k}  
>   Overschrijft `align-items`{:.p} voor een specifiek element.
> - `flex:`{:.p} `«flex-grow»`{:.v} `«flex-shrink»`{:.v} `«flex-basis»`{:.v} &#124;  
>   `«flex-grow»`{:.v} `«flex-basis»`{:.v} &#124; `«flex-grow»`{:.v} `«flex-shrink»`{:.v} &#124;  
>   `«flex-basis»`{:.v} &#124; `«flex-grow»`{:.v}
>   1. `flex-grow:`{:.p} `«groeifactor»`{:.v} &#124; `0` &#124; `.5` &#124; `1`{:.d} &#124; `1.5` &#124; `2` &#124; …
>   2. `flex-shrink:`{:.p} `«krimpfactor»`{:.v} &#124; `0` &#124; `.5` &#124; `1`{:.d} &#124; `1.5` &#124; `2` &#124; …
>   3. `flex-basis:`{:.p} `«afmeting-met-eenheid»`{:.v} &#124; `auto`{:.k.d} &#124; `content`{:.k} &#124; `100%` &#124; `123px` &#124; …
> - `order:`{:.p} … `-2` &#124; `-1` &#124; `0`{:.d} &#124; `1` &#124; `2` &#124; …

