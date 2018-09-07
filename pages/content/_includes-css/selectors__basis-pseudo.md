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