Stijlvoorrang
-------------

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