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

### Wat is een doctype?

De **doctype** of **Document Type Definition**:

- Vertelt de browser welk **soort document** het bestand bevat.
- Staat **helemaal bovenaan** het document, op de eerste lijn.

In onderstaand voorbeeld wordt de HTML5-doctype gebruikt.

{% highlight html linenos %}
<!DOCTYPE html>
{% endhighlight %}{:data-file="index.html"}

Zowel kapitalen als kleine letters zijn toegelaten, maar de **bovenstaande versie** wordt aangeraden.

{% highlight html linenos %}
<!doctype html>
{% endhighlight %}{:data-file="index.html"}

### Waarom is de doctype belangrijk?

Vroeger hadden browsers eigen interpretaties van de HTML-standaarden: 

 - Zonder doctype gaat de browser ervan uit dat het document geschreven is voor oudere browsers en wordt op **Quirks Mode**[ˆquirk] overgeschakeld.
 - Met correcte doctype schakelt de browser over op **Standards Mode** en wordt de HTML-standaard netjes gevolgd.

[ˆquirk]: *Eng.: Quirk* betekent rarigheid, gril, …

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
