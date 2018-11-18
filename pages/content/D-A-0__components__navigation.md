---
title: Components
title_long: Components
permalink: Components/navigation
---

De navigatie is een belangrijk onderdeel van je website. 
De navigatie toont je op welke pagina je bent en waar je naar toe kan gaan. 

Het geeft de belangrijke onderdelen van een webite aan. 

## Navigatie schema

{% include shared/figure.html src="https://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/navigatieschema.png" alt="Navigatieschema" caption="Navigatieschema" %}

**1. Globaal**  
De hoofdnavigatie is een vaste navigatie en is overal aanwezig.  Waar ben ik en waar kan ik naar toe?

**2. Lokaal**  
De subnavigatie is enkel voor bepaalde delen. Wat is er in de buurt?

**3. Contextuele**  
Hyperlinks die tussen de informatie staat. Wat is er nog gerelateerd aan deze informatie?

**4. Aanvullende navigatie**  
- Sitemap
- Site index

## Soorten navigatie op basis van design
  
### Horizontale navigatie

Eerst bouwen we de html-structuur op.
Die bouwen we op met een Unorderd list.

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/6/embedded/html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/8/embedded/result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

In de CSS verwijderen we de lijst-iconen met ```list-type``` en met flexbox plaatsen we de listitems naast elkaar. 

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/13/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

De tekst staat in het voorbeeld naast elkaar. Als we alle elementen willen verdelen over de volledige breedte maken we gebruik van ```justify-content: space-around; ```. 
Ook zien we de standaard opmaak van een link, dit resetten we.

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/16/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>


Nu geef we onze menu wat meer opmaak.

<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/20/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

We implementeren een active-menu-status. Zo weet de gebruiker waar hij zich bevind op onze website.

```
     nav ul li.active {
       color:#88898c;
       background-color:#f1f2f6;
     }
```
<iframe width="100%" height="300" src="//jsfiddle.net/rutsaert/67854g2f/25/embedded/css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>


### Verticale navigatie

