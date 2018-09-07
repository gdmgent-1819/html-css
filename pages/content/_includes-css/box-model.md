> Zie ook
> ---
> - [W3C / CSS Box Model](https://www.w3.org/TR/CSS2/box.html)
{:.card.card-link}


Binnen &rarr; buiten:

 1. **Content** edge *(Ned.: inhoud)*  
   Vak dat de eigenlijke inhoud van het element omvat.
 2. **Padding** edge *(Ned.: vulling)*  
   Vak dat de vulling omvat.
 3. **Border** edge *(Ned.: rand)*  
   Vak dat de lijndikte omvat.
 4. **Margin** edge *(Ned.: marge)*  
   Vak dat de marge rond het element omvat.
 5. **Offset Positioning**  
   Afstand ten opzichte van de normale plaatsing.

{% include shared/figure.html src="content/box-model.svg" alt="Box Model en Offset Positioning" caption="Box Model en Offset Positioning" local=true %}

> HTML & CSS: design and build websites (Duckett, 2011)
> ---
> - Chapter 10 – **Introducing CSS** (p. 229 e.v.)
{:.card.card-book}

> Zie ook
> ---
> [CSS 2.1 Box Model](https://www.w3.org/TR/CSS2/box.html)
{:.card.card-link}

Elk element heeft een **box** *(Ned.: vak)* rond zich. Zowel block-level elementen als inline elementen.

Box Model *(Ned.: vakkenmodel)*
-------------------------------

### CSS Box Model + Offset Positioning

De inhoud heeft een `height:`{:.p} *(Ned.: hoogte)* en `width:`{:.p} *(Ned.: breedte).*

> Opgelet
> ---
> Hoogte en breedte kunnen bepaald worden door ingesloten elementen en eigenschappen van de inhoud.
{:.card.card-warning}

#### Visuele hoogte

{% highlight css %}
  border-top
+   padding-top
+     height
+   padding-bottom
+ border-bottom
{% endhighlight %}

> Opgelet
> ---
> **ZONDER** `margin-top`{:.p} en `margin-bottom`{:.p}!
{:.card.card-warning}

#### Visuele breedte

{% highlight css %}
  border-left
+   padding-left
+     width
+   padding-right
+ border-right
{% endhighlight %}

> Opgelet
> ---
> **ZONDER** `margin-left`{:.p} en `margin-right`{:.p}!
{:.card.card-warning}

> De **winterjas**metafoor
> ---
> Het is winter en **ik** (content met `height`{:.p} en `width`{:.p}, inhoud met hoogte en breedte)  
> heb warm door de **voering** (`padding`{:.p}, vulling)  
> van mijn **winterjas** (`border`{:.p}, rand).  
> Ik loop op **10 cm** (`margin`{:.p}, marge) van een pas geschilderde muur, dus moet ik opletten dat mijn jas niet vuil wordt.

> HTML & CSS: design and build websites (Duckett, 2011)
> ---
> - Chapter 13 – **Boxes** (p. 307 e.v.)
{:.card.card-book}

Invloed van Doctype op Box Model
--------------------------------

De doctype heeft invloed op het gebruikte box model. Het **Quirks Mode** box model verschilt per browser, terwijl het **Standards Mode** box model overal hetzelfde zou moeten zijn.

Gebruik dus steeds een correct Doctype!

`<!DOCTYPE html>`{:.dt} of `<!doctype html>`{:.dt}

Box Sizing
----------

Je kan de standaard manier waarop de visuele afmetingen bepaald worden veranderen met:

> `box-sizing:`{:.p} `content-box`{:.k.d} &#124; `border-box`{:.k}

| Waarde               | `height`{:.p} en `width`{:.p} zijn de afmetingen van |
|----------------------|------------------------------------------------------|
| `content-box`{:.k.d} | enkel de inhoud.                                     |
| `border-box`{:.k}    | de som van inhoud + `padding`{:.p} + `border`{:.p}.  |
{:.table.table--primary}