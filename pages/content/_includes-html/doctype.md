HTML-doctype
------------

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