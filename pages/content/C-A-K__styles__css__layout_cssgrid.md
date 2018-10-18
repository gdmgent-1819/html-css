---
title: Lay-out grid
title_long: Lay-out grid
permalink: styles/css/layout/cssgrid
---

CSS Grid Layout
---------------

> Zie ook
> ---
> - [Grid Garden](http://cssgridgarden.com)
> - [W3C / CSS Grid Layout Module](https://www.w3.org/TR/css-grid/)
> - [CSS Tricks / A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
{:.card.card-book}

### Grid Container (parent-element)

> - `display:`{:.p} `grid`{:.k} &#124; `inline-grid`{:.k} &#124; `subgrid`{:.k}
> - `grid-template:`{:.p} `none`{:.k} &#124; `«grid-template-rows»`{:.v} `/` `«grid-template-columns»`{:.v}
>   1. `grid-template-rows:`{:.p} `«trackgrootte»`{:.v} …  &#124; `[«lijnnaam»]`{:.v} `«trackgrootte»`{:.v} … &#124; … `repeat(«herhalingen», «eigenschappen»)`{:.v}  …
>   2. `grid-template-columns:`{:.p} `«trackgrootte»`{:.v} …  &#124; `[«lijnnaam»]`{:.v} `«trackgrootte»`{:.v} … &#124; … `repeat(«herhalingen», «eigenschappen»)`{:.v}  …
> - `grid-template-area:`{:.p} `"«gridgebiednamen-per-rij-gescheiden-door-spaties»"`{:.v} …  
>    `«gridgebiednamen»`{:.v} kunnen zijn: `«gridgebiednaam»`{:.v} &#124; `.`{:.k} (lege gridcel) &#124; `none`{:.k} (geen gridgebied)
> - `grid-gap:`{:.p} `«grid-row-gap»`{:.v} `«grid-column-gap»`{:.v}
>   1. `grid-row-gap:`{:.p}
>   2. `grid-column-gap:`{:.p}
> - `justify-items:`{:.p} `start`{:.k.d} &#124; `end`{:.k} &#124; `center`{:.k} &#124; `stretch`{:.k.d}
>   Uitlijning op de **row-axis** (rijas).
> - `align-items:`{:.p} `start`{:.k.d} &#124; `end`{:.k} &#124; `center`{:.k} &#124; `stretch`{:.k.d}
>   Uitlijning op de **column-axis** (kolomas).
> - `justify-content:`{:.p} `start`{:.k.d} &#124; `end`{:.k} &#124; `center`{:.k} &#124; `stretch`{:.k.d} &#124; `space-around`{:.k} &#124; `space-between`{:.k} &#124; `space-evenly`{:.k}
>   Uitlijning op de **row-axis** (rijas).
> - `align-content:`{:.p} `start`{:.k.d} &#124; `end`{:.k} &#124; `center`{:.k} &#124; `stretch`{:.k.d} &#124; `space-around`{:.k} &#124; `space-between`{:.k} &#124; `space-evenly`{:.k}
>   Uitlijning op de **column-axis** (kolomas).

### Grid Items (child-elementen)

> - `grid-area:`{:.p} `«grid-row-start»`{:.v} `/` `«grid-column-start»`{:.v} `/` `«grid-row-end»`{:.v} `/` `«grid-column-end»`{:.v}.
>   1. `grid-row:`{:.p} `«grid-row-start»`{:.v} `/` `«grid-row-end»`{:.v}
>     1. `grid-row-start:`{:.p} `«geheel-getal»`{:.v}
>     2. `grid-row-end:`{:.p} `«geheel-getal»`{:.v}
>   2. `grid-column:`{:.p} `«grid-column-start»`{:.v} `/` `«grid-column-end»`{:.v}
>     1. `grid-column-start:`{:.p} `«geheel-getal»`{:.v}
>     2. `grid-column-end:`{:.p} `«geheel-getal»`{:.v}
> - `justify-self:`{:.p}
> - `align-self:`{:.p}
> - `order:`{:.p} … &#124; `-2` &#124; `-1` &#124; `0`{:.d} &#124; `1` &#124; `2` &#124; …
