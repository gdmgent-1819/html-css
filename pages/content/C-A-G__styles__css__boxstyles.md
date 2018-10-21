---
title: Box stijlen
title_long: Box stijlen
permalink: styles/css/boxstyles/
---

Background
----------


> References
> ---
> - [Mozilla Developer Network: background](https://developer.mozilla.org/nl/docs/Web/CSS/background)
{:.card.card-source}

### background

Met de `background`-property kan je verkort alle achterground-eigenschappen van een element toepassen, zoals de kleur, afbeelding, afmeting, herhaling, ...

- `background:`{:.p} `«background-color»`{:.v} `«background-image»`{:.v} `«background-repeat»`{:.v} `«background-attachment»`{:.v} `«background-position»`{:.v}
  1. `background-color:`{:.p} `«kleur»`{:.v}
  2. `background-image:`{:.p}  
     `url(«pad-naar-afbeelding»)`{:.f} &#124; `url("«pad-naar-afbeelding»")`{:.f} &#124;  
     `linear-gradient()`{:.f} &#124; `repeating-linear-gradient()`{:.f} &#124;  
     `radial-gradient()`{:.f} &#124; `repeating-radial-gradient()`{:.f} &#124;  

  3. `background-repeat:`{:.p} `repeat`{:.k.d} &#124; `repeat-x`{:.k} &#124; `repeat-y`{:.k} &#124; `no-repeat`{:.k} &#124; …
  4. `background-attachment:`{:.p} `scroll`{:.k.d} &#124; `fixed`{:.k}
  5. `background-position:`{:.p} `«x-as» «y-as»`{:.v} &#124; `«x-afstand» «y-afstand»`{:.v} &#124; `center`{:.k}
      - `«x-as»`{:.v}: `left`{:.k.d} &#124; `center`{:.k} &#124; `right`{:.k}
      - `«y-as»`{:.v}: `top`{:.k.d} &#124; `center`{:.k} &#124; `bottom`{:.k}

### background-color




### background-image

#### Afbeelding

- `background-image:`{:.p}  
    `url(«pad-naar-afbeelding»)`{:.f} &#124; `url("«pad-naar-afbeelding»")`{:.f} &#124;  
    `linear-gradient()`{:.f} &#124; `repeating-linear-gradient()`{:.f} &#124;  
    `radial-gradient()`{:.f} &#124; `repeating-radial-gradient()`{:.f} &#124;  

Met de background-image property kan je één of meerdere achtergrondafbeeldingen op een element toepassen. Je links met behulp van `url('...')` naar het pad van de afbeelding. Deze afbeelding kan in je images-map staan of online gehost zijn.  
Je kan ook gebruik maken van een **data-uri** waarbij de afbeeldingsinformatie rechtstreeks in de *string* vervat zit.

{% highlight css %}
/* Afbeelding staat in de images-folder */
div {
    background-image: url('../images/panda.png');
}

/* Afbeelding is online gehost */
footer {
    background-image: url('https://picsum.photos/1000/300');
}

/* Afbeelding met behulp van een data-uri */
li {
    background-image: url('data:image/gif;base64,R0lGODlhEAAQAMQAAORHHOVSKudfOulrSOp3WOyDZu6QdvCchPGolfO0o/XBs/fNwfjZ0frl3/zy7////wAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACH5BAkAABAALAAAAAAQABAAAAVVICSOZGlCQAosJ6mu7fiyZeKqNKToQGDsM8hBADgUXoGAiqhSvp5QAnQKGIgUhwFUYLCVDFCrKUE1lBavAViFIDlTImbKC5Gm2hB0SlBCBMQiB0UjIQA7');
}
{% endhighlight %}

Je kan meerdere achtergrondafbeeldingen toepassen door de `url(...)` te scheiden met een komma: `url('...'), url('...')`. De achtergrondafbeelding die als eerste komt zal bovenaan komen te staan.

<iframe height='500' scrolling='no' title='Background-Image' src='//codepen.io/fredroeg/embed/xyzNby/?height=265&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

#### Kleurverloop (gradient)

Met diezelfde background-image property kan je ook een kleurverloop erop toepassen. CSS onderscheidt twee types van gradients:
- **Lineair** (startpunt-eindpunt)
    - `background-image:`{:.p} `linear-gradient(richting, color-stop1, color-stop2, ...);`{:.k.d}
- **Radiaal** (vanuit het centrum naar buiten toe)
    - `background-image:`{:.p} `radial-gradient(color-stop1, color-stop2, ...);`{:.k.d}


Standaard gaat het verloop van boven naar onder, je kan meer dan twee kleuren definiëren.  
De kleuren worden gescheiden door middel van een komma.

De standaard richting is **to bottom** en is optioneel.  

Je kan volgende richtingen definiëren:

- **Horizontaal**
    - `to left`{:.k} (van rechts naar links)
    - `to right`{:.k} (van links naar rechts)
- **Verticaal**
    - `to bottom`{:.k.d} (**standaard**, boven naar onder)
    - `to top`{:.k} (van onder naar boven)
- **Diagonaal**
    - `to bottom right`{:.k} (linksboven->rechtsonder)
    - `to bottom left`{:.k} (rechtsbocen->linksonder)
    - `to top right`{:.k} (linksonder->rechtsboven)
    - `top top left`{:.k} (rechtsonder->linksboven)
    - `__deg`{:.k} (onder een hoek, vb `50deg` of `-75deg`)


<iframe height='500' scrolling='no' title='background-image gradient' src='//codepen.io/fredroeg/embed/OBEYbX/?height=265&theme-id=0&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

Er bestaan ook herhalende kleurverlopen (zie resources).

### Background-repeat

`background-repeat:`{:.p} `repeat`{:.k.d} &#124; `repeat-x`{:.k} &#124; `repeat-y`{:.k} &#124; `no-repeat`{:.k} &#124; …

Standaard wordt de achtergrondafbeelding herhaald over zowel de x-as als de y-as. Je kan dit veranderen met de `background-repeat`-property.

- `background-repeat:`{:.p}
    - `repeat`{:.k.d} (horizontaal herhalen + verticaal herhalen)
    - `repeat-x`{:.k} (enkel horizontaal herhalen)
    - `repeat-y`{:.k} (enkel verticaal herhalen)
    - `no-repeat`{:.k} (nooit herhalen)

### background-position

`background-position:`{:.p} `«x-as» «y-as»`{:.v} &#124; `«x-afstand» «y-afstand»`{:.v} &#124; `center`{:.k}
      - `«x-as»`{:.v}: `left`{:.k.d} &#124; `center`{:.k} &#124; `right`{:.k}
      - `«y-as»`{:.v}: `top`{:.k.d} &#124; `center`{:.k} &#124; `bottom`{:.k}

Standaard wordt de achtergrondafbeelding linksboven in het element geplaatst, maar je kan het veranderen met de `background-position`{:.p}-property.





### Background-size


### Background-attachment


> References
> ---
> - [Mozilla Developer Network: background-attachment](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment)
{:.card.card-source}

### Background-origin

> References
> ---
> - [Mozilla Developer Network: background-origin](https://developer.mozilla.org/en-US/docs/Web/CSS/background-origin)
{:.card.card-source}

### Background-clip

> References
> ---
> - [Mozilla Developer Network: background-clip](https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip)
{:.card.card-source}

Box shadow
----------

Box outline
-----------

> References
> ---
> - [Mozilla Developer Network: Outline]( https://developer.mozilla.org/en-US/docs/Web/CSS/outline)
{:.card.card-source}

### border vs outline