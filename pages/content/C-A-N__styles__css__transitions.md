---
title: Transitions
title_long: Transitions
permalink: styles/css/transitions/
published: true
---

## Begrip

CSS transitions laten toe om een overgang/animatie tussen twee statussen van een element te definiëren. In plaats van een css-property meteen uit te voeren, kan je de veranderingen geleidelijk laten plaatsvinden over een bepaalde periode. Bijvoorbeeld, als je de kleur van een link wil veranderen van blauw naar rood bij het 'hoveren' met de muis, dan is deze verandering onmiddelijk. Indien er een CSS-transition op toegepast is, dan zal die verandering geleidelijk gebeuren over een tijdsinterval.

Deze statussen kunnen gedefinieerd worden via bepaalde pseudo-klassen, zoals: `:hover` en `active` (of via JavaScript (door het toevoegen of verwijderen van `class`-attribuut waarden).

{% include shared/figure.html src="https://developer.mozilla.org/files/4529/TransitionsPrinciple.png" alt="Transitions Principle" caption="CSS Transitions Principe" %}

Met CSS transitions kan je zelf kiezen welke properties je wil animeren (door ze expliciet op te lijsten).
- **property**: welke css-eigenschap je wil animeren
- **duration**: hoe lang de transitie duurt
- **timing**: hoe zal de transitie afspelen (vb. lineair of snel starten & traag eindigen)
- **delay**: wanneer de animatie start (vb. na 4 seconden)

## Transities definiëren

CSS-transities definieer je het beste met de shorthand `transition`-property. Dit is de beste manier om transitions te configureren en maakt het gemakkelijk om de verschillende parameters te definiëren.

{% highlight css %}
div {
    transition: <property> <duration> <timing-function> <delay>;
}
{% endhighlight %}

### transition-property
De `transition-property` wordt gebruikt om de CSS-eigenschappen te definiëren waarop de transitie zal toegepast worden, bv.: all (op alle CSS-eigenschappen), top, left, background, color, … .

#### Op welke css-properties kan een transitie ingesteld worden?

Als developer kies je zelf op welke css-properties je een transitie zet. Hierdoor ben je in staat om eenvoudige tot heel complexe transities te creëeren. Niet elke css-property is echter even geschikt om te animeren.

[**Lijst van animeerbare properties**](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties)

> Opmerking 1
> ---
> De lijst van animeerbare properties evolueert nog steeds, naarmate de specificaties verder ontwikkelen.
{:.card.card-remark}

> Opmerking 2
> ---
> Vermijd zoveel mogelijk transities bij een `auto`-value. De animatie werkt vaak niet of is onvoorspelbaar.
{:.card.card-remark}

{% highlight css %}
/* rechtermargin animeren */
transition-property: margin-right;
/* alle properties animeren */
transition-property: all;
{% endhighlight %}

### transition-duration
De **transition-duration** wordt gebruikt om de duur van de transitie te specificeren. De default-waarde bedraagt `0s`. De waarden kunnen uitgedrukt worden in **seconden** (s) of **milliseconden** (ms).

{% highlight css %}
/* transitie zal 6 seconden duren */
transition-duration: 6s;
/* transitie duurt 120 milliseconden */
transition-duration: 120ms;
{% endhighlight %}

> Opmerking voorbeelden
> ---
> Onderstaande transities loopen oneindig lang, ter illustratie. Dit is standaard niet het geval. Een transitie gebeurt standaard slechts één keer van start naar finish. 
> De voorbeelden zijn afkomstig van:  [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
{:.card.card-remark}

`transition-duration: 0.5s`
<iframe src="https://mdn.mozillademos.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions$samples/duration_0_5s?revision=1434632" class="live-sample-frame sample-code-frame" height="150" width="275" id="frame_duration_0_5s" frameborder="0" style="border: 1px solid #CCC; padding: 15px;"></iframe>


`transition-duration: 4s`
<iframe src="https://mdn.mozillademos.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions$samples/duration_4s?revision=1434632" class="live-sample-frame sample-code-frame" height="150" width="275" id="frame_duration_4s" frameborder="0" style="border: 1px solid #CCC; padding: 15px;"></iframe>

### transition-timing-function
De **transition-timing-function** wordt gebruikt om te beschrijven hoe de tussenliggende waarden van de CSS-eigenschappen beïnvloed worden door het transitie-effect. De snelheid van de transitie varieert over de duur van deze transitie door de acceleratie-curve, gekend als easing-functies.

Veel gebruikte timing-functies zijn `linear`{:.k.d}, `ease`{:.k}, `ease-in`{:.k}, `ease-out`{:.k}, `ease-in-out`{:.k}, `steps()`{:.k}, `step-start`{:.k}, `step-end`{:.k} en `cubic-bezier(x1, y1, x2, y2)`{:.k}.


<table>
  <thead>
    <tr>
      <th>Timing-function</th>
      <th>Curve</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code class="highlighter-rouge">linear</code></td>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/linear.png" alt="enter image description here"></td>
      <td>Constante snelheid: <code class="highlighter-rouge">cubic-bezier(0.0, 0.0, 1.0, 1.0)</code>
</td>
    </tr>
    <tr>
      <td><code class="highlighter-rouge">ease</code></td>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/ease.png" alt="enter image description here"></td>
      <td>Gelijkaardig met <code class="highlighter-rouge">ease-in-out</code>. De acceleratie in het begin is sneller en vanaf het midden treedt vertraging op:  <code class="highlighter-rouge">cubic-bezier(0.25, 0.1, 0.25, 1.0)</code>
</td>
    </tr>
    <tr>
      <td><code class="highlighter-rouge">ease-in</code></td>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/easein.png" alt="enter image description here"></td>
      <td>De animatie begint traag waarna de acceleratie progressief toeneemt: <code class="highlighter-rouge">cubic-bezier(0.42, 0.0, 1.0, 1.0)</code>
</td>
    </tr>
    <tr>
      <td><code class="highlighter-rouge">ease-out</code></td>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/easeout.png" alt="enter image description here"></td>
      <td>De annimatie start snel waarna de acceleratie progressief afneemt: <code class="highlighter-rouge">(0.0, 0.0, 0.58, 1.0)</code>
</td>
    </tr>
    <tr>
      <td><code class="highlighter-rouge">ease-in-out</code></td>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/easeinout.png" alt="enter image description here"></td>
      <td>De animatie start traag, accelereert dan, waarna het terug afneemt: <code class="highlighter-rouge">0.42, 0.0, 0.58, 1.0)</code>
</td>
    </tr>
    <tr>
      <td><code class="highlighter-rouge">step-start</code></td>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/stepstart.png" alt="enter image description here"></td>
      <td>De animatie springt direct naar de eindstatus: <code class="highlighter-rouge">steps(1, start)</code>
</td>
    </tr>
    <tr>
      <td><code class="highlighter-rouge">step-end</code></td>
        <td>
        <img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/stepend.png" alt="enter image description here"></td>
        <td>De animatie blijft in de initiële status en springt pas op het einde naar zijn eindstatus: <code class="highlighter-rouge">steps(1, end)</code>
    </td>
    </tr>
    <tr>
      <td style="vertical-align: top;"><code class="highlighter-rouge">cubic-bezier</code></td>
      <td style="vertical-align: top;"><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/bezier.png" alt="enter image description here"></td>
      <td>P0 (0,0) Initiële status. P3 (1,1) Finale status. P1 en P2 hebben meestal een waarde tussen 0 en 1. Ligt deze waarde daarbuiten, dan zullen we waarschijnlijk een <strong>bouncing-effect</strong> realiseren.

        {% highlight css %}
        cubic-bezier(x1, y1, x2, y2)
        {% endhighlight %}

        x1 en x2 moeten een waarde hebben tussen 0 en 1  
        y1 en y2 kunnen zowel postieve- als negatieve waarden bevatten
        
        {% highlight css %}
        Enkele voorbeelden:

        cubic-bezier(0.1, 0.7, 1.0, 0.1)
        cubic-bezier(0, 0, 1, 1)
        cubic-bezier(0.1, -0.6, 0.2, 0)
        cubic-bezier(0, 1.1, 0.8, 4)
        {% endhighlight %}

      </td>
    </tr>
  </tbody>
</table>

De `steps`{:.k} functie definieert het aantal stappen dat binnen de timing functie uitgevoerd zullen worden. Deze functie is beter gekend als een staircase functie. De syntax: `steps(number_of_steps, direction)`{:.k}. De `number_of_steps`{:.k} is een positieve integer (1 of hoger), de `direction`{:.k} is `start`{:.k} of `end`{:.k.d}. Dit laatste argument is facultatief en heeft `end`{:.k.d} als standaard waarde.

<table>
  <thead>
    <tr>
      <th>Direction: start</th>
      <th>Direction: end</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code class="highlighter-rouge">steps(2, start)</code></td>
      <td><code class="highlighter-rouge">steps(4, end)</code></td>
    </tr>
    <tr>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/steps1.png" alt="Steps: start"></td>
      <td><img src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/steps2.png" alt="Steps: end"></td>
    </tr>
  </tbody>
</table>

#### Voorbeelden

`transition-timing-function: linear`
<iframe src="https://mdn.mozillademos.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions$samples/ttf_linear?revision=1434632" class="live-sample-frame sample-code-frame" height="150" width="275" id="frame_ttf_linear" frameborder="0" style="border: 1px solid #CCC; padding: 15px;"></iframe>

`transition-timing-function: ease`
<iframe src="https://mdn.mozillademos.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions$samples/ttf_ease?revision=1434632" class="live-sample-frame sample-code-frame" height="150" width="275" id="frame_ttf_ease" frameborder="0" style="border: 1px solid #CCC; padding: 15px;"></iframe>

`transition-timing-function: steps(4, end)`
<iframe src="https://mdn.mozillademos.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions$samples/ttf_step4end?revision=1434632" class="live-sample-frame sample-code-frame" height="150" width="275" id="frame_ttf_step4end" frameborder="0"></iframe>

### transition-delay

Definieert hoe lang er gewacht moet worden alvorens te transitie werkelijk start.

## Voorbeelden

### Voorbeeld ease-in-out transition

**ease-in-out**: traag starten, versnellen, terug vertragen, traag eindigen.  
 
Hover over de grijze kader om de transitie te zien.

<iframe height='400' scrolling='no' title='jQLgLV' src='//codepen.io/fredroeg/embed/jQLgLV/?height=265&theme-id=dark&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

### Voorbeeld delay

Transition met een delay van twee seconden.  

Hover over **Hello GDM** om de transitie te bekijken.

<iframe height='265' scrolling='no' title='Delay Transition' src='//codepen.io/fredroeg/embed/MzvNmo/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

### Voorbeeld meerdere transities

Je kan meerdere transities toewijzen, door ze te scheiden met een komma.

<iframe height='300' scrolling='no' title='Multiple animated properties exampleSection' src='//codepen.io/fredroeg/embed/VVzoyR/?height=265&theme-id=dark&default-tab=css,result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

### Voorbeeld verschillende timing-functions

In onderstaand voorbeeld zie je dezelfde animatie, met dezelfde duration, maar met verschillende timing-functions.

<iframe height='650' scrolling='no' title='Transition Demo' src='//codepen.io/fredroeg/embed/mQMNLb/?height=648&theme-id=dark&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>
</iframe>

## Referenties

> Zie ook
> ---
> - [MDN: Using CSS Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
> - [MDN: Animatable CSS Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties)
> - [MDN: Transition Property](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-property)
> - [MDN: Transition Duration](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-duration)
> - [W3C / CSS Flexible Box Layout Module](https://www.w3.org/TR/css-flexbox/)
> - [CSS Tricks / A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
{:.card.card-book}