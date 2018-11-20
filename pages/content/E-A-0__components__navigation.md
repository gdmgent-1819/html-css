---
title: Navigatie
title_long: Navigatie
permalink: componenten/navigation/
---

De navigatie is een belangrijk onderdeel van je website.  
Hij toont je op welke pagina je bent en waar je naar toe kan gaan.  
De navigatie van een website geeft de belangrijke onderdelen van een webite aan. 

Navigatie schema
----------------

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/navigatieschema.png" alt="Navigatieschema" caption="Navigatieschema" %}

**1. Globaal**  
De hoofdnavigatie is een vaste navigatie en is overal aanwezig.  Waar ben ik en waar kan ik naar toe?

**2. Lokaal**  
De subnavigatie is enkel voor bepaalde delen. Wat is er in de buurt?

**3. Contextuele**  
Hyperlinks die tussen de informatie staat. Wat is er nog gerelateerd aan deze informatie?

**4. Aanvullende navigatie**  
- Sitemap
- Siteindex

Navigaties op basis van design
-----------------------------
  
### Horizontale navigatie

#### Voorbeeld 1 

Stap voor stap bouwen we een horizontale navigatie op.  

<iframe width="100%" height="200" src="//jsfiddle.net/rutsaert/67854g2f/58/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

We sarten met de basisstructuur in HTML.   
Een navigatie bouwen we op met de semantische ```nav```-tag. Die bevat een unorderd list ```ul ```. Voor elk menu-item plaatsen we een listitem ``` li ``` met ankerelement ``` a ```.

<iframe width="100%" height="250" src="//jsfiddle.net/rutsaert/67854g2f/39/embedded/html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<iframe width="100%" height="200" src="//jsfiddle.net/rutsaert/67854g2f/8/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

In de CSS verwijderen we de lijst-iconen met ```list-style:none```.  
Met flexbox plaatsen we al de listitem naast elkaar. 

<iframe width="100%" height="200" src="//jsfiddle.net/rutsaert/67854g2f/13/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

De tekst staat in het voorbeeld naast elkaar. Als we alle elementen willen verdelen over de volledige breedte maken we gebruik van ```justify-content: space-around; ```.  

<iframe width="100%" height="200" src="//jsfiddle.net/rutsaert/67854g2f/52/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

We zien dat de tekst een blauwe kleur heeft en onderlijnd is. Dit is de standaard opmaak van een anker-element. Dit resetten we.
We geven de menu wat meer opmaak.

<iframe width="100%" height="600" src="//jsfiddle.net/rutsaert/67854g2f/56/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

We implementeren een active-menu-status. Zo weet de gebruiker waar hij zich bevind op onze website.

{% highlight css %}
     nav ul li.active {
       color:#88898c;
       background-color:#f1f2f6;
     }
{% endhighlight %}

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/47/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

Als laatst voegen we de lay-out toe voor de hover-status,``` :hover ```. Die kan het zelfde zijn als de active-status.

{% highlight css %}
   nav ul li.active, nav ul li:hover {
       color:#88898c;
       background-color:#f1f2f6;
     }
{% endhighlight %}

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/49/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/58/embedded/html,css/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<iframe width="100%" height="250" src="//jsfiddle.net/rutsaert/67854g2f/58/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

#### Voorbeeld 2

**Resultaat**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/5hgrdsL6/28/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**HTML**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/5hgrdsL6/28/embedded/html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**CSS**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/5hgrdsL6/28/embedded/css/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

### Horizontale menu met dropdown

**Resultaat**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/qyj07g35/37/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**HTML**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/qyj07g35/35/embedded/html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**CSS**

<iframe width="100%" height="900" src="//jsfiddle.net/rutsaert/qyj07g35/34/embedded/css/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

### Verticale navigatie

#### Voorbeeld 1

**Resultaat**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/opfarmb2/2/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**HTML**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/opfarmb2/2/embedded/html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**CSS**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/opfarmb2/2/embedded/css/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

### Voorbeeld 2 
**Resultaat**

<iframe width="100%" height="400" src="//jsfiddle.net/rutsaert/7m0gwacv/7/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**HTML**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/7m0gwacv/7/embedded/html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

**CSS**

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/7m0gwacv/7/embedded/css/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

## Inspiratie

### Hoofdnavigatie

#### Wijs.be

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/wijs_desktop.png" alt="Wijs.be: Main navigation - desktop" caption="Wijs.be: Main navigation - desktop" %}

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/wijs_offcanvas_closed.png" alt="Wijs.be: Main navigation - desktop" caption="Wijs.be: Main navigation - mobile (hamburger)" %}

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/wijs_offcanvas_open.png" alt="Wijs.be: Main navigation - desktop" caption="Wijs.be: Main navigation - mobile (expanded)" %}

#### InThePocket.com

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/itp_desktop.png" alt="InThePocket.com: Main navigation - desktop" caption="InThePocket.com: Main navigation - desktop" %}

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/itp_offcanvas_closed.png" alt="InThePocket.com: Main navigation - desktop" caption="InThePocket.com: Main navigation - mobile (hamburger)" %}

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/itp_offcanvas_open.png" alt="InThePocket.com: Main navigation - desktop" caption="InThePocket.com: Main navigation - mobile (expanded)" %}

#### the-reference.com

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/thereference_closed.png" alt="InThePocket.com: Main navigation - desktop" caption="InThePocket.com: Main navigation - mobile (hamburger)" %}

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/thereference_open.png" alt="the-reference.com: Main navigation - desktop" caption="the-reference.com: Main navigation - mobile (expanded)" %}