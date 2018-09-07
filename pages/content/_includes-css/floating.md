Zwevende elementen
------------------

### Basis

Door een element zwevend te maken kan je dat element buiten de **normale flow** uiterst links of rechts in een omvattende blok plaatsen. Het zwevende element wordt **een blokelement** waar andere inhoud omheen loopt. Dit wordt vaak gebruikt bij het plaatsen van een afbeelding in een tekst. Door de afbeelding te laten zweven zal de tekst er mooi rond lopen. Het is aangeraden om het zwevende element altijd expliciet een width te geven, omdat het anders onvoorspelbaar kan zijn. 

Aangezien een zwevend element sowieso een block-level element is, wordt de box compleet weergegeven, inclusief paddings, borders en margins. De margins van een zwevend element en aangrenzende elementen schuiven niet in elkaar.

`float`{:.p}  
- `none`{:.k.d}  
  Standaard waarde. Het element zal niet zweven, maar weergegeven worden waar 
- `left`{:.k}  
  Het element zweeft uiterst links, alle andere content zal eromheen lopen.
- `right`{:.k}  
  Het element zweeft uiterst rechts, alle andere content zal eromheen lopen.

#### Voorbeeld 1
<iframe width="100%" height="500" src="//jsfiddle.net/rogerthat_be/tsyz5xos/embedded/result,css,html/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

#### Voorbeeld 2 (dynamisch voorbeeld)

In onderstaand voorbeeld kan je visueel het verschil zien als de afbeeldingen wel of niet de `float`-eigenschap toegewezen hebben.  
Als je op de rode knop klikt zal de tekst rond de afbeelding lopen *(class met float toegepast)*, klik je nog eens is de float terug uitgeschakeld.  
Er wordt gebruik gemaakt van Javascript om een class in of uit te schakelen.  
<iframe height='742' scrolling='no' title='Float Voorbeeld' src='//codepen.io/fredroeg/embed/bYORrw/?height=742&theme-id=0&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

#### Zwevende elementen naast elkaar plaatsen

Je kan meerdere elementen naast elkaar plaatsen door ze allemaal een float eigenschap te geven. 
{% highlight html %}
<div class="blokje"></div>
<div class="blokje"></div>
<div class="blokje"></div>
<div class="blokje"></div>
{% endhighlight %}
{% highlight css %}
/* aangezien elke div met class blokje de float: left property heeft, komen die naast elkaar te staan */
.blokje {
    float: left;
    width: 250px;
    height: 250px;
}
{% endhighlight %}

![Multiple Floating Elements](https://sf.rogerthat.be/1718/multiplefloats.png)

#### Clear

Als een zwevend element echter niet naast een ander zwevend element mag komen, kan je er een `clear` op toepassen.

`clear:`{:.p}  
- `none`{:.k.d}  
  Standaard waarde. Elementen mogen links en rechts zweven. 
- `left`{:.k}  
  Geen zwevende elementen toegestaan aan de linkerzijde
- `right`{:.k}  
  Geen zwevende elementen toegestaan aan de rechterzijde
- `both`{:.k}  
  Geen zwevende elementen toegestaan aan de linkerzijde, noch aan de rechterzijde


> Geavanceerd: Niet voor examen
> ---
> De onderstaande, geavanceerde info is louter achtergrondinformatie omtrent het gebruik van floating elements voor lay-outs.    
> Door de mogelijkheden van flexbox wordt dit voor nieuwe toepassingen nog slechts zelden gebruikt.
{:.card.card-warning}

#### Omvattend element

**Probleem:**

Wil je floating elements gebruiken om lay-outs te maken moet er rekening gehouden worden met de omvattende elementen. Indien je rond zwevende elementen een kader wil plaatsen (bijvoorbeeld een `div` met een `border`) kan dit *omvattend element* voor problemen zorgen. Browsers behandelen het omvattende element dan namelijk alsof het **nul pixels hoog** is.  

In onderstaand voorbeeld staat er een blauwe omvattende div met blauwe rand, rond de vier (zwevende) oranje blokjes. Bijgevolg komt de blauwe rand niet mooi rondom de blokjes.  
![nul pixels hoogte](https://sf.rogerthat.be/1718/geen-hoogte.png "nul pixels hoogte")

Dit hoogteprobleem kan ook opduiken als er tekst + afbeelding staat in een omvattende kader. In het onderstaande voorbeeld kan je opmerken dat enkel de tekst voor de hoogte zorgt binnen de omvattende groene kader. Er wordt geen rekening gehouden met de hoogte van de zwevende afbeelding (de `img`-tag heeft css-eigenschap `float: right;`.
![enkel de tekst neemt hoogte in](https://sf.rogerthat.be/1718/float-problem.png "enkel de tekst neemt hoogte in")

**Oplossing:**

Er is echter een oplossing voor, namelijk door een `clearfix` hack op toe te passen. Dit is een veelgebruikte hack om ervoor te zorgen dat het omvattende element rondom alle zwevende elementen spant.

Op het omvattende element wordt een `::after`-pseudo element toegepast:
{% highlight css %}
.omvattende-kader::after {
    content: "";
    clear: both;
    display: table;
}
{% endhighlight %}

![clearfix](https://sf.rogerthat.be/1718/clearfix.png "clearfix")

**Voorbeeld:**

<iframe width="100%" height="500" src="//jsfiddle.net/rogerthat_be/e32LbLh0/embedded/result,css,html/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>