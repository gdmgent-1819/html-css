Structuur
---------

### Het Root-element

> Zie ook
> ---
> - [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html)
{:.card.card-book}

> `<html>`{:.e} … `</html>`{:.e}

 - Alle andere elementen zitten ertussen vervat, die elementen noemt men **descendants**.
 - Het `<html>`{:.e}-element **moet altijd aanwezig** zijn!

> Definitie
> ---
> Alle elementen binnen een bepaald element noemt men **descendants** *(Ned.: nakomelingen)* van dat element.
{:.card.card-definition}

### `<head>`{:.e}-element

> Zie ook
> ---
> - [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head)
{:.card.card-book}

> `<head>`{:.e} … `</head>`{:.e}

 - `<head>`{:.e} Een **descendant** van `<html>`{:.e}.  
 - `<head>`{:.e} is het **eerste child**-element van het root-element (`<html>`{:.e}).  

> Definitie
> ---
> Een **child**-element is een **rechtstreekse** descendant *(Ned.: nakomeling).*
{:.card.card-definition}

Deze bevat de **meta**gegevens van het HTML-document. **‘Meta’** wil zeggen gegevens over het document zelf: 

 - titel
 - tekenset
 - stylesheetkoppelingen
 - …

    `<title>`{:.e} … `</title>`{:.e} Bevat de titel van de html-pagina. Deze titel verschijnt in het tabblad van de browser en in de favorietenlijst.

### `<body>`{:.e}-element

> Zie ook
> ---
> - [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)
{:.card.card-book}

> `<body>`{:.e} … `</body>`{:.e}

- `<body>`{:.e} is een **descendant** van `<html>`{:.e}.
- `<body>`{:.e} is het **tweede child**-element van het root-element (`<html>`{:.e}).  

Deze bevat de **eigenlijke inhoud** van de pagina:

 - tekst
 - afbeeldingen
 - audio
 - video
 - …
