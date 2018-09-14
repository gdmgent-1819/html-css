---
title: Structuur
title_long: Structuur van een webpagina
permalink: markup/html/structure/
---

Het HTML-bestand
----------------

Een **statische webpagina** bestaat uit een tekstbestand dat meestal de **bestandsextensie** `.html` heeft. Door deze extensie herkennen zowel de browser als de teksteditor het bestand als een HTML-document.

{% highlight html linenos %}
<!DOCTYPE html>
<html lang="nl">
    <head>
        <meta charset="UTF-8">
        <title>Hallo</title>
    </head>
    <body>
        <h1>Hallo GDM!</h1>
        <p>Mijn naam is Voornaam Naam.</p>
    </body>
</html>
{% endhighlight %}{:data-file="index.html"}

Als de webbrowser geen specifiek bestand opvraagt aan een webserver, dan zullen de meeste webservers ervan uitgaan dat het gevraagde bestand `index.html` is. Dit hangt af van de serverinstellingen die door de serverbeheerder ingesteld zijn.

> Opmerking
> ---
> De **startpagina** *(Eng.: home page)* van een website noem je best `index.html`.
{:.card.card-remark}

Anatomie van een HTML-document
------------------------------

{% highlight html linenos %}
<!DOCTYPE html>
<html lang="nl">
    <head>
        <meta charset="UTF-8">
        <title>Hallo</title>
    </head>
    <body>
        <h1>Hallo GDM!</h1>
        <p>Mijn naam is Voornaam Naam.</p>
    </body>
</html>
{% endhighlight %}{:data-file="index.html"}

> References
> ---
> - [Mozilla Developer Network: Anatomy of a HTML document](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#Anatomy_of_an_HTML_document#Anatomy_of_a_HTML_document)
{:.card.card-source}

### Doctype

<!DOCTYPE html>: The doctype. In the mists of time, when HTML was young (about 1991/2), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML, which could mean automatic error checking and other useful things. They used to look something like this:
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
However, these days no one really cares about them, and they are really just a historical artifact that needs to be included for everything to work right. <!DOCTYPE html> is the shortest string of characters that counts as a valid doctype; that's all you really need to know.

In HTML, the doctype is the required "<!DOCTYPE html>" preamble found at the top of all documents. Its sole purpose is to prevent a browser from switching into so-called “quirks mode” when rendering a document; that is, the "<!DOCTYPE html>" doctype ensures that the browser makes a best-effort attempt at following the relevant specifications, rather than using a different rendering mode that is incompatible with some specifications.

https://developer.mozilla.org/en-US/docs/Glossary/Doctype

https://developer.mozilla.org/en-US/docs/Web/HTML/Quirks_Mode_and_Standards_Mode

### `<html>`{:.e}-element

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
> - [Mozilla Developer Network: body](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)
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
