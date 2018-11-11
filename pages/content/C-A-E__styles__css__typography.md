---
title: Typography
title_long: Typography
permalink: styles/css/typography/
---


Er zijn heel wat verschillende lettertypes op de markt. Slechts enkele van deze staan standaard geïnstalleerd op een computer. Afhankelijk van je besturingssysteem *(Eng.: OS, Operating System)* en de versie (Windows, macOS, Linux, Android, iOS) heb je meer of minder standaard lettertypes.

Om lettertypes te kunnen gebruiken moeten deze (tijdelijk) geïnstalleerd staan op het toestel *(Eng.: device)* van de bezoeker.

Hieronder een overzicht van de verschillende mogelijkheden.

`font-family:`{:.p}
-------------------

`font-family:`{:.p} is de basis CSS-eigenschap om het lettertype aan te passen. Je kan meerdere lettertypes opgeven die gebruikt worden als 'fallback'. Dit wil zeggen dat als het eerste lettertype niet beschikbaar is, je kan terugvallen op het eerstvolgende in de lijst en zo verder.

{% highlight css linenos %}
body {
    font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
{% endhighlight %}

> Opgelet
> ---
> Als de naam van het lettertype **spaties** bevat, dan moet de naam tussen **rechte aanhalingstekens** staan.  
> Dit mag zowel **aanhalingstekens** (`"`) als **apostroffen** (`'`) zijn.
{:.card.card-warning}

In bovenstaande CSS zie je dat we het lettertype aanpassen voor de volledige body van ons HTML-document. Indien de bezoeker **Helvetica Neue** op zijn computer geïnstalleerd heeft dan zal dit lettertype gebruikt worden. Anders zal er overgegaan worden naar het volgende lettertype, in dit geval Helvetica. Dit gaat zo door tot een lettertype gevonden wordt.

> Opmerking
> ---
> Als laatste lettertype kies je **altijd** een van deze generieke types:
>
> - `serif`{:.k.d} (schreef)
> - `sans-serif`{:.k} (schreefloos)
> - `monospace`{:.k} (vaste letterbreedte)
> - `cursive`{:.k} (handgeschreven)
> - `fantasy`{:.k} (lettertype dat niet in de vorige types past)
{:.card.card-remark}

Doorheen de verschillende OS-versies zijn er diverse basis lettertypes gebruikt. Onderstaande lettertypes zijn het meest ondersteund:

| Type              | Lettertypes                                         |
|-------------------|-----------------------------------------------------|
| `serif`{:.k.d}    | Times New Roman, Times, Georgia, Palatina, Garamond |
| `sans-serif`{:.k} | Helvetica, Arial, Verdana, Tahoma                   |
| `monospace`{:.k}  | Courier New, Courier                                |
{:.table.table--primary}

`@font-face`
------------

Om af te stappen van de standaard lettertypes kan men gebruik maken van een techniek waarbij een lettertype die niet geïnstalleerd staat bij de bezoeker wordt gedownload en tijdelijk geïnstalleerd. Dit kan via `@font-face`. Je kan ieder lettertype gebruiken binnen je website. Daarnaast moet je er ook voor zorgen dat dit lettertype geëxporteerd wordt in verschillende bestandsformaten.

> Opgelet
> ---
> Controleer of de licentie die je hebt voor dit lettertype dit ook effectief toelaat! Lees daarom de **eindgebruikersovereenkomst** (EULA) van het lettertype dat je wil gebruiken.
{:.card.card-warning}

### Importeren van een lettertype in CSS

{% highlight css linenos %}
@font-face {
  font-family: 'MyWebFont';
  src: url('..path/to/webfont.eot'); /* IE9 Compat Modes */
  src: url('..path/to/webfont.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('..path/to/webfont.woff2') format('woff2'), /* Super Modern Browsers */
       url('..path/to/webfont.woff') format('woff'), /* Pretty Modern Browsers */
       url('..path/to/webfont.ttf')  format('truetype'), /* Safari, Android, iOS */
       url('..path/to/webfont.svg#svgFontName') format('svg'); /* Legacy iOS */
}
{% endhighlight %}

### Het lettertype gebruiken

{% highlight css %}
body {
    font-family: MyWebFont, Helvetica, Arial, sans-serif;
}
{% endhighlight %}

Google Fonts
------------

Als alternatief op de `@font-face` techniek kan je gebruik maken van [Google Fonts][]. Google Fonts gebruikt dezelfde techniek en heeft heel wat kwalitatief goede lettertypes samengebracht om op een eenvoudige manier te importeren in je eigen CSS file. [Fontsquirrel](https://www.fontsquirrel.com/fonts/list/hot_web) heeft ook een groot aanbod van fonts, maar moeten wel altijd gedownload worden om vervolgens te linken via `@font-face`.

Kies 1 of meerdere lettertypes die je wenst te gebruiken. Let wel: Hoe meer lettertypes we gebruiken, hoe trager de website zal werken. Probeer het aantal in te laden lettertypes en varianten dus te herleiden tot een minimum.
Je kan het lettertype op 3 manieren inladen:

### Inladen van de CSS in de `<head>`{:.e}

{% highlight html %}
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,300">
{% endhighlight %}

### Importeren van de CSS in je eigen CSS

{% highlight css %}
@import url(https://fonts.googleapis.com/css?family=Open+Sans:400,700,300);
{% endhighlight %}

### Via JavaScript

Deze manier is minder gebruikelijk.

{% highlight HTML %}
<script>
  WebFontConfig = {
    google: { families: [ 'Open+Sans:400,700,300:latin' ] }
  };
  (function() {
    var wf = document.createElement('script');
    wf.src = ('https:' == document.location.protocol ? 'https' : 'http') +
      '://ajax.googleapis.com/ajax/libs/webfont/1/webfont.js';
    wf.type = 'text/javascript';
    wf.async = 'true';
    var s = document.getElementsByTagName('script')[0];
    s.parentNode.insertBefore(wf, s);
  })(); 
</script>
{% endhighlight %}

Icon Fonts
----------

Je kan op verschillende manieren iconen toevoegen aan je website. Vroeger was het gebruikelijk om het icoon als afbeelding (JPEG of PNG) in je HTML of CSS te gebruiken. Maar doordat deze afbeeldingen een vaste pixelverhouding hebben is deze manier van werken niet voldoende voor ondermeer slechtzienden. Mede door de komst van smartphones en tablets is men overgegaan naar een techniek om lettertypes te gebruiken waarin icoontjes staan in plaats van letters.
Deze kunnen dan net zoals letters veranderen in grootte, kleur, ...

### Font Awesome

[Font Awesome][] is een voorbeeld van een lettertype met [een groot aanbod aan iconen](https://fontawesome.io/icons/) die grotendeels gratis zijn. [Fontastic](http://fontastic.me/) bevat heel veel iconfonts die we kunnen groeperen in packs. Het overgrote deel van de iconfonts in Fontastic zijn wel betalend.

#### CSS Importeren

In de `<head>`{:.e} voeg je onderstaande regel toe.

{% highlight HTML %}
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css" integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU" crossorigin="anonymous">
{% endhighlight %}

#### Icoon toevoegen in HTML

<i class="fa fa-graduation-cap"></i>

{% highlight html %}
<i class="fa fa-graduation-cap"></i>
{% endhighlight %}

> Opmerking
> ---
> Hier 'misbruiken' we het `<i>`{:.e}-element dat normaal gebruikt wordt om tekst **cursief** *(Eng.: italic)* te plaatsen, om een icoon in de tekst te plaatsen.
>
> Strikt gezien zou dit niet mogen en zou een `<span>`{:.e} gebruikt moeten worden, maar omdat het `<i>`{:.e}-element geen betekenis toevoegt is dit verdedigbaar omwille van de kortere code en de toevallige overeenkomst van de letter `i` van het HTML-element en de eerste letter van het woord `icon`. 
{:.card.card-remark}

#### Icoon groter maken

| Icoon                             | CSS-klasses             |
|:---------------------------------:|-------------------------|
| <i class="fa fa-cloud"></i>       | `fa` `fa-cloud`         |
| <i class="fa fa-cloud fa-lg"></i> | `fa` `fa-cloud` `fa-lg` |
| <i class="fa fa-cloud fa-2x"></i> | `fa` `fa-cloud` `fa-2x` |
| <i class="fa fa-cloud fa-3x"></i> | `fa` `fa-cloud` `fa-3x` |
| <i class="fa fa-cloud fa-4x"></i> | `fa` `fa-cloud` `fa-4x` |
| <i class="fa fa-cloud fa-5x"></i> | `fa` `fa-cloud` `fa-5x` |
{:.table}

{% highlight html %}
<i class="fa fa-cloud"></i>
<i class="fa fa-cloud fa-lg"></i>
<i class="fa fa-cloud fa-2x"></i>
<i class="fa fa-cloud fa-3x"></i>
<i class="fa fa-cloud fa-4x"></i>
<i class="fa fa-cloud fa-5x"></i>
{% endhighlight %}

Naast het groter plaatsen zijn er ook nog manier om iconen te roteren, animeren, combineren en dergelijke meer.
Hiervoor verwijzen we je door naar de website van [Font Awesome](http://fontawesome.io/examples/)

### Meer Icon Fonts

Er zijn uiteraard nog veel meer alternatieven voor Font Awesome. Een zoekopdracht naar ['CSS vector icons'](http://lmgtfy.com/?q=css+vector+icons) levert alvast heel wat resultaten op.

 - [Fontello](http://fontello.com)
 - [Glyphicons](https://glyphicons.com)
 - [Github Octicons](https://octicons.github.com)
 - [Linearicons](https://linearicons.com/free#cdn)


Typografische CSS-eigenschappen
------------------------------------

> - `color:`{:.p} `«kleur»`{:.v}
> - `font-family:`{:.p}
> - `font-size:`{:.p} `«lettergrootte»`{:.v}
> - `font-weight:`{:.p} `«lettergewicht»`{:.v} &#124;  
     `lighter`{:.k} &#124; `normal`{:.k.d} &#124; `bold`{:.k} &#124; `bolder`{:.k} &#124;  
     `100`{:.k} &#124; `200`{:.k} &#124; `300`{:.k} &#124; `400`{:.k.d} &#124; `500`{:.k} &#124; `600`{:.k} &#124; `700`{:.k} &#124; `800`{:.k} &#124; `900`{:.k}


### Font style, font weight, text transform, and text decoration


> References
> ---
> - [Mozilla Developer Network: Font style, font weight, text transform, and text decoration](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals#Font_style_font_weight_text_transform_and_text_decoration)
{:.card.card-source}

### Text drop shadows


> References
> ---
> - [Mozilla Developer Network: Text drop shadows](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals#Text_drop_shadows)
{:.card.card-source}


Text layout
-----------
> References
> ---
> - [Mozilla Developer Network: Text Layout](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals#Text_layout)
{:.card.card-source}

- Text alignment
- Line height
- Letter and word spacing
- ...