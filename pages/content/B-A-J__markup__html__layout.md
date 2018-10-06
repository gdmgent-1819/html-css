---
title: Lay-out
title_long: Lay-out
permalink: markup/html/layout/
---

Gekende web lay-outs
-------------------

Webpagina's zien er meestal anders uit ten opzichte van elkaar, maar ze bevatten structureel meestal dezelfde standaard componenten:

- **Header**  
Meestal zichtbaar op iedere webpagina van een website. Het bevat relevantie informatie voor alle webpagina's, zoals: de naam van de website, het logo, [courtesy navigation](http://maxsnitser.com/blog/7-tips-about-navigation-in-ux-design) en meestal ook de hoofdnavigatie (Eng.: main navigation). Dikwijls blijft deze component plakken (Eng.: stick) bovenaan in de browser tijdens het scrollen.
- **Hoofdnavigatie**  
Bevat links naar de belangrijkste interne webpagina's. Deze links worden meestal weergegeven via knoppen, ankers of tabs. Net zoals de header, is deze hoofdnavigatie consisten voor heel de website (aanwezig op iedere webpagina). De hoofdnavigatie, meestal gekend als de "navigation bar" is dikwijls een onderdeel van de header, maar kan ook onafhankelijk gestructureerd worden.
- **Hoofdinhoud**  
De hoofdinhoud (Eng.: main content) bevat de unieke inhoud eigen aan een webpagina. Deze inhoud varieert per webpagina, bijv.: een bepaald artikel, video, e.d. . Alles wat gerelateerd is met deze inhoud behoort tot de hoofdinhoud, meestal via een sidebar of een blokelement binnen dit element.
- **Sidebar**  
Bevat randinformatie (Eng.: peripheral info) omtrent de hoofdinhoud, zoals: gerelateerde informatie, quotes, advertienties (Eng.: ads), biography van de auteur e.d. en dikwijls een secundaire navigatie (Eng.: secondary navigation) waarin onderliggende belangrijke referenties worden gelinkt.
- **Footer**  
De footer staat bijna altijd onderaan de webpagina en bevat meestal: copyright info, gdpr info, cookie-beleid, links naar belangrijke / populaire inhouden, e.d. . De informatie die hierin staat is van secundair (Eng.: secondary) niveau. Deze inhoud kan ook de zoekmachines (Eng.: search engines) assisteren om de website te promoten.

> References
> ---
> - [Mozilla Developer Network: What do common web layouts contain?](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Common_web_layouts)
> - [Max Snitser: 7 TIPS ABOUT NAVIGATION IN UX DESIGN](http://maxsnitser.com/blog/7-tips-about-navigation-in-ux-design)
> - [Mozilla Developer Network: Document and website structure](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
{:.card.card-source}

https://developer.mozilla.org/en-US/docs/Web/CSS/Layout_mode
https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Introduction


Lay-out Elementen
-----------------

- `<main>`
- `<article>`
- `<section>`
- `<aside>`
- `<header>`
- `<footer>`
- `<nav>`
- `<div>`
- `<span>` 

> References
> ---
> - [Mozilla Developer Network: Layout elements](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
{:.card.card-source}

### `<main>`{:.e}-element

> Definitie
> ---
> Een `<main>`-element representeert de unieke hoofdinhoud op de webpagina, kortom in het <body>-element van een webdocument. De inhoud binnen dit element is gerelateerd tot bepaalde inhoud in de <head> van de webpagina, zoals: title, description, keywords, OpenGraph informatie, … . Er kan slechts één `<main>`-element zijn in een webpagina. 
{:.card.card-definition}

{% highlight html %}

<!-- other content -->

<main>
  <h1>New Media Development (Multimediaproductie)</h1>
  <p>Zijn Websites, Mobiele Applicaties, Internet of Things, Mixed Reality en Smart Assistants voor jou nu al passé? Werk mee aan de hype van morgen en ontwikkel bij ons de skills van de toekomst!</p>
  
  <article>
    <h2>Hackathon-week NMD 2de jaar</h2>
    <p>Onze studenten New Media Development ruilden voor een kleine week hun vertrouwde omgeving te Mariakerke in voor enkele workshops en een coole onderwijsvorm en dit op een vreemde locatie met focus op één opleidingsonderdeel Mobile Development II.</p>
    <p>... </p>
    <p>... </p>
  </article>

  ...
</main>

<!-- other content -->

{% endhighlight %}


> References
> ---
> - [Mozilla Developer Network: Main element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)
{:.card.card-source}

### `<article>`{:.e}-element

> Definitie
> ---
> Een `<article>`-element representeert een component op een webpagina dat bestaat uit een vrijstaande compositie in een document, pagina, applicatie of site. Indien we alle inhoud rondom een `<article>`-element wegdenken blijft dit element verstaanbaar. 
{:.card.card-definition}

Het is herbruikbaar en onafhankelijk distribueerbaar in syndicatie. Het kan een nieuwsartikel, commentaar, forum post, widget of elk ander onafhankelijke inhoud zijn. Wanneer een section wordt gedeeld in andere blogs, twitter, facebook, reddit, RSS feed … gebruik dan een `<article>`-element. De inhoud van statische pagina’s in een site, zoals "About" en "Contact" pagina, worden meestal omsloten door een article element.

{% highlight html %}

<!-- other content -->

<main>
  <h1>New Media Development (Multimediaproductie)</h1>
  <p>Zijn Websites, Mobiele Applicaties, Internet of Things, Mixed Reality en Smart Assistants voor jou nu al passé? Werk mee aan de hype van morgen en ontwikkel bij ons de skills van de toekomst!</p>
  
  <article>
    <h2>Hackathon-week NMD 2de jaar</h2>
    <p>Onze studenten New Media Development ruilden voor een kleine week hun vertrouwde omgeving te Mariakerke in voor enkele workshops en een coole onderwijsvorm en dit op een vreemde locatie met focus op één opleidingsonderdeel Mobile Development II.</p>
    <p>... </p>
    <p>... </p>
  </article>

  ...
</main>

<!-- other content -->

{% endhighlight %}

> Opmerking
> ---
> - Elk `<article>`-element moet geidentificeerd worden met een heading, meestal als eerst kind-element.
> - Een genest `<article>`-element (binnen een andere `<article>`-element) is gerelateerd met het buiten of ouder element.
{:.card.card-remark}

> References
> ---
> - [Mozilla Developer Network: Article element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article)
{:.card.card-source}

### `<section>`{:.e}-elementen

> Definitie
> ---
> Een `<section>`-element definieert een sectie in een web-document. Het groepeert gelijksoortige inhoud die samen slechts een eigenschap of thema vormen.
{:.card.card-definition}

{% highlight html %}
<article>
    <h1>Lay-out</h1>
    <section>
        <h2>Gekende web lay-outs</h2>
        <p>...</p>
    </section>
    <section>
        <h2>Lay-out Elementen</h2>
        <p>...</p>
    </section>
    <section>
        ...
    </section>
/<article>
{% endhighlight %}

> Opmerking
> ---
> - Een section bevat meestal een hoofdding. Iedere section zou geïdentificeerd moeten worden via `<h1>`-`<h6>`-element als een kind van dit element.
> - Een section mag niet gebruikt worden als een generieke container. 
> - Een section verschijnt in de ouline van het web-document via zijn hoofdding. 
> - Een section mag niet gebruikt worden in het geval dat article, aside of nav elementen beter geschikt zijn in bepaalde situaties.
{:.card.card-remark}

> References
> ---
> - [Mozilla Developer Network: Section element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)
{:.card.card-source}

### `<aside>`{:.e}-elementen

> Definitie
> ---
> Een `<aside>`-element is verbonden met de inhoud die het ondersteunt. Het is bijvoorbeeld gerelateerd met een post of artikel. Het kan bijvoorbeeld links bevatten die geralateerd zijn aan het artikel. De auteur en andere meta-informatie kan hierin ook vermeld worden. Secundaire navigatie wordt hierin niet vermeld omdat dit gerelateerd is tot het `<main>`-element, hiervoor moeten we een `<section>`-element gebruiken.
{:.card.card-definition}

{% highlight html %}
<article>
    <h1>Forza Horizon 4 Review</h1>
    <p></p>
    <aside>
      <h3>Getest</h3>
      <ul>
        <li><a href="https://tweakers.net/pricewatch/1183633/forza-horizon-4-xbox-one.html" target="_self">Forza Horizon 4, Xbox One</a></li>
        <li><a href="https://tweakers.net/product/781787/forza-horizon-4/" target="_self">Bekijk alle uitvoeringen</a></li>
        <li><a href="https://tweakers.net/pricewatch/1183633/forza-horizon-4-xbox-one.html target="_self">Vergelijk prijzen</a></li>
      </ul>
    </aside>
    <section>
        <h2>Mooiste racegame</h2>
        <p>...</p>
    </section>
/<article>
{% endhighlight %}

> References
> ---
> - [Mozilla Developer Network: Aside element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside)
{:.card.card-source}

### `<header>`{:.e}-elementen

> Definitie
> ---
> Een `<header>`-element bevat introducerende inhoud voor de omsluitende sectie. De inhoud bevat meestal een heading, supplementaire inhoud of andere navigatie-gereedschappen. Indien de ouder van een `<header>` het body-element is, dan zal deze header van toepassing zijn op de gehele webpagina. Een header moet minimaal één heading bevatten. Andere mogelijke bestandsdelen: “table of contents”, logo’s, zoekformulier, … . Een `<header>`is een blokelement. De header is geen sectioning element.
{:.card.card-definition}

{% highlight html %}
<header>
  <h1>The most important olod is NMDAD-I</h1>
  <p>It's mega cool :)</p>
</header>
{% endhighlight %}

De `<header>` in het bovenstaand voorbeeld fungeert als algemene header voor een webpagina. Deze bestaat een heading `<h1>` en een baseline. De baseline mag eventueel beschreven worden binnen een `<h2>`.

{% highlight html %}
<article>
  <header>
      <h2>Justin Bieber Ipsum</h2>
      <p>By Bietin Jusber</p>
  </header>
  <p> like The Notebook worst birthday ever we don't need no wings to fly. I like The Notebook I like The Notebook man, we steppin' out like whoa. Swag swag swag, on you, chillin by the fire while we eaten' fondue smile on your face, even though your heart is frowning I like The Notebook. Man, we steppin' out like whoa let the music blast we gon' do our dance I like Sour Patch Kids. Don't be so cold, we could be fire it's a Bieber world live it or die canada. I'ma make you shine bright like you're laying in the snow, burr I make good grilled cheese and I like girls I'd like to be an architect, that would be cool, cause I like drawing. Swag swag swag, on you, chillin by the fire while we eaten' fondue I'ma make you shine bright like you're laying in the snow, burr but something would be nothing. Man, we steppin' out like whoa swag you know I'm a real OG and baby I ain't from the TO.</p>
</article>
{% endhighlight %}

> References
> ---
> - [Mozilla Developer Network: Header element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)
{:.card.card-source}

### `<footer>`{:.e}-elementen

Een <footer> element bevat afsluitende inhoud voor de omsluitende sectie. De inhoud bevat meestal informatie over de sectie waaraan het verbonden is, zoals: auteur(s), publicatiedatum, gerelateerde documenten, copyright informatie, … . Een <footer>is een blokelement. Voeg een ARIA role=”contentinfo” toe als de footer een algemene footer is voor een webpagina. De footer is geen sectioning element.

> Definitie
> ---
> Een `<footer>`-element bevat afsluitende inhoud voor de omsluitende sectie. De inhoud bevat meestal informatie over de sectie waaraan het verbonden is, zoals: auteur(s), publicatiedatum, gerelateerde documenten, copyright informatie, … . Een `<footer>`is een blokelement.
{:.card.card-definition}

{% highlight html %}
<article>
  ...
  <footer>
    <ul>
      <li>copyright</li>
      <li>sitemap</li>
      <li>contact</li>
      <li>to top</li>
  </footer>
</article>
{% endhighlight %}

> References
> ---
> - [Mozilla Developer Network: Footer element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer)
{:.card.card-source}

### `<nav>`{:.e}-elementen

> Definitie
> ---
> Het `<nav>`-element representeert een sectie van een webpagina dat links bevat naar andere pagina’s of naar onderdelen binnen deze webpagina. Kortom het is een sectie met navigatielinks. Een `<nav>`-element groepeert links en zorgt voor betere semantische structuur ten behoeve van **screenreaders**.
{:.card.card-definition}

{% highlight html %}
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Over Ons</a></li>
    <li><a href="#">Diensten</a></li>
    <li><a href="#">Cases</a></li>
    <li><a href="#">Inzichten</a></li>
    <li><a href="#">Werken bij thefabric</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
{% endhighlight %}

Het `<nav>`-element wordt voornamelijk gebruikt voor primaire en secundaire navigatie. Niet zozeer voor de links vermeld in de footer van een webpagina. Dit element kan ook gebruikt worden voor: TOC (Table Of Contents), breadcrumbs, zoekformulier in de navigatie en eventueel paginering.

{% highlight html %}
<footer>
  <p>Copyright © 2019 The Fabriek</p>
  <p><a href="about.html">Over Ons</a> -
  <a href="policy.html">Privacy Policy</a> -
  <a href="contact.html">Contact Ons</a></p>
</footer>
{% endhighlight %}

> References
> ---
> - [Mozilla Developer Network: Nav element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)
{:.card.card-source}

### `<span>`{:.e}-elementen

> Definitie
> ---
> `<span>` is een **inline** non-semantisch (zonder waardevolle betekenis) element, die we gebruiken om een of meerdere woorden te stijlen bij voorkeur met behulp van een `class`-attribuut (met een specifieke waarde).
{:.card.card-definition}

{% highlight html %}
<span class="baseline">Like Graphics Love Code and make cool shit.</span>
{% endhighlight %}

### `<div>`{:.e}-elementen

> Definitie
> ---
> `<div>` is een **blok** non-semantisch element die we gebruiken wanneer het omsloten blok geen waardevolle betekenis bevat.
{:.card.card-definition}

{% highlight html %}
<div class="shopping-cart">
  <h2>Shopping cart</h2>
  <ul>
    <li>
      <p><a href=""><strong>Lynda.com</strong></a>: 25€.</p>
      <img src="http://blogs.nhtv.nl/nhtv-library/files/2016/03/lynda.png" alt="Lynda.com logo">
    </li>
    <li>
      ...
    </li>
  </ul>
  <p>Total cost: 164€</p>
</div>
{% endhighlight %}

Een winkelmandje (Eng.: Shopping Cart) behoort niet tot (ter zijde van `<aside>` of als onderdeel van `<section>`) de hoofdinhoud op een webpagina. Het is in dit geval ok om een `<div>`-element te gebruiken.

> Opmerking
> ---
> Gebruik enkel een `<div>` wanneer er geen betere sematische oplossing van toepassing is. Beperk het gebruik van `<div>`-elementen binnen een webpagina omdat dit zorgt voor een onoverzichtelijke structuur.
{:.card.card-remark}

### `<time>`{:.e}-elementen

> Definitie
> ---
> Het `<time>`-element representeert een tijd op een 24-uren klok of een precieze datum in de Gregorian calendar (met optioneel de tijd en tijdzone). De intentie van dit element is om datums en tijd te presenteren in een leesbaar formaat voor machines. Het machine leesbare gedeelte zit vervat in het attribuut datetime van dit element. Datums worden uitgedrukt in **YYYY-MM-DD**.
{:.card.card-definition}

- `<time datetime="1975">`jaar 1975
- `<time datetime="1975-12">` betekent Decenmber 1975
- `<time datetime="12-12">` betekent 12 december elk jaar
- `<time datetime="1975-W49">` betekent week 49 van 1975
- `<time datetime="1975-12-12T08:45">` betekent 12 December 1975 om 8:45 uur
- `<time datetime="08:45+2">` is 8:45 uur UTC+2
- `<time datetime="P2D">` is een duur van 2 dagen
- `<time datetime="PT23H 9M 2.343S">` is een duur van 23 uren, 9 minuten en 2.343 seconden

> References
> ---
> - [Mozilla Developer Network: Time element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time)
{:.card.card-source}