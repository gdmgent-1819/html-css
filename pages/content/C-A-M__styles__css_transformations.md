---
title: Transformaties
title_long: Transformaties
permalink: styles/css/transformations/
published: true
---


> Definitie
> ---
> Transformaties laten toe om de positie, grootte en vorm van een element te veranderen.
{:.card.card-definition}

In CSS kunnen we een element op volgende manieren transformeren:

- verplaatsen **translate**
- schalen **scale**
- roteren **rotate**
- uitrekken/scheeftrekken **(skew)**

Zowel 2D als 3D transformaties kunnen toegepast worden in CSS. Transformaties kunnen toegekend worden aan een element via het `transform`{:.p} eigenschap.


> Opmerking
> ---
> Het transformatiepunt ligt standaard in het midden van het element!
{:.card.card-remark}

## 2D-transformaties

### 2D-translatie

Translatie of verschuiving van een element, in dit geval in de 2D-ruimte. Translatie wordt in CSS gerealiseerd via de translate methoden:

> - `translate(`{:.p}`tx, ty`{:.k}`)`{:.p} (ty is optioneel en standaard 0)
> - `translateX(tx)`{:.p} Translatie langs de X-as
> - `translateY(ty)`{:.p} Translatie langs de Y-as

De waarden van translatie (tx, ty) kunnen uitgedrukt worden in een lengte (getal gevolgd door een lengte-eenheid, zoals: px, em, in, pt, mm, …) of in percentage (%).

In onderstaand voorbeeld verplaatsen we een element: 20px verschuiving langs de X-as, 50% van de hoogte van het element verschuiving langs de Y-as.

<iframe height='265' scrolling='no' title='dQVyxK' src='//codepen.io/fredroeg/embed/dQVyxK/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

### 2D-schalen

Elementen kunnen geschaald worden in de X- en/of Y-richting. Schalen wordt in CSS gerealiseerd via de `scale`{:.p} methoden:

> - `scale(`{:.p}`sx, sy`{:.k}`)`{:.p} Indien sy niet gespecifieerd wordt, zal sy = 1
> - `scaleX(sx)`{:.p} Schalen over de X-as
> - `scaleY(sy)`{:.p} Schalen over de Y-as

De waarden van schalen (`sx`, `sy`) moeten uitgedrukt worden met een getal (positief of negatief floating-point getal).

<iframe height='265' scrolling='no' title='2D-scale' src='//codepen.io/fredroeg/embed/eQGmNv/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

### 2D-rotatie

Elementen kunnen geroteerd worden in de X- en/of Y-richting. Rotatie wordt in CSS gerealiseerd via de `rotate`{:.p} methoden:

> - `rotate(rz)`{:.p} roteren vanuit het center van het element (over de z-as)
> - `rotateX(rx)`{:.p} roteren over de x-as
> - `rotateY(ry)`{:.p} roteren over de y-as

De waarden van schalen (rx, ry, rz) moeten uitgedrukt worden met een getal (positief of negatief floating-point getal). 

Het rotatiegetal kan uitgedrukt worden in volgende eenheden:
- `deg`{:.k} (graden) (vb `45deg`)
- `turn`{:.k} (aantal draaien, vooral interessant bij het animeren) (vb `-2turn`)
- `rad`{:.k} (radialen) (vb `3.142rad`)

<iframe height='265' scrolling='no' title='2D-ROTATE' src='//codepen.io/fredroeg/embed/LXzEZB/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

> Zie ook
> ---
> - [MDN: Rotate](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotate)
> - [MDN: RotateX](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotateX)
> - [MDN: RotateY](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotateY)/en-US/docs/Web/CSS/transition-property)
> - [MDN: Transition Duration](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-duration)
> - [W3C / CSS Flexible Box Layout Module](https://www.w3.org/TR/css-flexbox/)
> - [CSS Tricks / A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
{:.card.card-book}

### 2D-scheeftrekken

Elementen kunnen scheefgetrokken worden in de X- en/of Y-richting. Scheeftrekken wordt in CSS gerealiseerd via de `skew`{:.p} methoden:

> - `skew(`{:.p}`ax, ay`{:.k}`)`{:.p}) Indien ay niet gespecifieerd wordt, zal ay = 0deg
> - `skewX(ax){:.p} Scheeftrekken langs de X-as
> - `skewY(ay){:.p} Scheeftrekken langs de Y-as

De waarden van scheeftrekken (ax, ay) wordt uitgedrukt in aantal graden: positief of negatief getal gevolgd door deg.

<iframe height='500' scrolling='no' title='2D-SKEW' src='//codepen.io/fredroeg/embed/oQGgZa/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

### 2D-transformatiepunt

Bij “default” ligt dit punt in het midden van het element, de initiële waarde bedraagt 50% 50%. Roteren we bv. een element, dan ligt het rotatiepunt initieel in het midden van het element. Het transformatie punt kunnen we via CSS op een andere plaats leggen en dit via de ``transform-origin` eigenschap:

> - `transform-origin(`{:.p}`x, y`{:.k}`)`{:.p})

De waarden van het transformatiepunt (x, y) kunnen uitgedrukt worden in een lengte (getal gevolgd door een lengte-eenheid, zoals: px, em, in, pt, mm, …) , in percentage (%) of via gedefinieerde keywords (left, center, right, top en bottom).

<iframe height='265' scrolling='no' title='2D-ROTATE (custom transform-origin)' src='//codepen.io/fredroeg/embed/PxJwJo/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### Combinatie

<iframe height='265' scrolling='no' title='TRANSFORMATIONS' src='//codepen.io/fredroeg/embed/JerorB/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

## 3D-transformaties

In CSS kunnen we CSS transformaties uitvoeren in de 3D-ruimte.

> - `translate3d(r-tx, ty, tz)`{:.p} 
> - `scale3d(r-tx, ty, tz)`{:.p} 

