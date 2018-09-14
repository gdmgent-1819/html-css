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

> Definitie
> ---
> In het doctype[^Doctype] definieren we het type van het document. Het voornaamste doel is om de browser te beletten om te switchen naar een eigenaardige modus (Eng.: quirks mode) die incompatibel is met de standaard specificaties. 
{:.card.card-definition}

`<!DOCTYPE html>` zorgt ervoor dat de browser de volledige W3C[^W3C] standaard zal volgen. Enkele jaren geleden werd het doctype nog gebruikt om te linken naar een verzameling van regels die een webpagina moest volgen om te voldoen aan goede geldige HTML.

[^Doctype]: **Doctype**: Document Type
[^W3C]: **W3C**: World Wide Web Consortium

> Opmerking
> ---
> Het `<!DOCTYPE html>` staat helemaal bovenaan in het document.
{:.card.card-remark}

> References
> ---
> - [Mozilla Developer Network: Doctype](https://developer.mozilla.org/en-US/docs/Glossary/Doctype)
> - [Mozilla Developer Network: Quirks Mode](https://developer.mozilla.org/en-US/docs/Web/HTML/Quirks_Mode_and_Standards_Mode)
{:.card.card-source}

### `<html>`{:.e}-element

> Definitie
> ---
> Het `<html>`{:.e}-element bevat alle inhoud (Eng.: content) op de volledige pagina. Dit element is ook gekend als het root-element.
{:.card.card-definition}

> References
> ---
> - [Mozilla Developer Network: HTML element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html)
{:.card.card-source}

> Opmerking
> ---
> - Alle andere elementen zitten ertussen vervat, die elementen noemt men **descendants** (Ned.: nakomelingen).
> - Het `<html>`{:.e}-element **moet altijd aanwezig** zijn!
{:.card.card-remark}

### `<head>`{:.e}-element

> Definitie
> ---
> Het `<head>`{:.e}-element is een container voor al de dingen die je wil toevoegen aan een webpagina, die niet worden getoond aan de bezoeker van deze webpagina. Dit element bevat de **meta**gegevens van het HTML-document. **‘Meta’** wil zeggen gegevens over het document zelf: titel, omschrijving, tekenset, stylesheetkoppelingen, … .
{:.card.card-definition}

> References
> ---
> - [Mozilla Developer Network: Head element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head)
> - [Mozilla Developer Network: What’s in the head?](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)
{:.card.card-source}

> Opmerking
> ---
> - `<head>`{:.e} Een **descendant** van `<html>`{:.e}. 
> - `<head>`{:.e} is het **eerste child**-element van het root-element (`<html>`{:.e}).  
> - `<title>`{:.e} … `</title>`{:.e} Bevat de titel van de html-pagina. Deze titel verschijnt in het tabblad van de browser en in de favorietenlijst.
{:.card.card-remark}

### `<body>`{:.e}-element

> Definitie
> ---
> Het `<body>`{:.e}-element bevat de **eigenlijke inhoud** van de webpagina die ja aan de bezoeker van deze webpagina wil tonen, zoals: tekst, afbeeldingen, video's, audio-bestanden, … .
{:.card.card-definition}

The <body> element. This contains all the content that you want to show to web users when they visit your page, whether that's text, images, videos, games, playable audio tracks, or whatever else.

> References
> ---
> - [Mozilla Developer Network: body](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)
{:.card.card-book}

> Opmerking
> ---
> `<body>`{:.e} … `</body>`{:.e}
> - `<body>`{:.e} is een **descendant** van `<html>`{:.e}.
> - `<body>`{:.e} is het **tweede child**-element van het root-element (`<html>`{:.e}). 
{:.card.card-remark}