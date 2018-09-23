---
title: Applicaties
title_long: Applicaties
permalink: introduction/applications/
published: false
---

> Taken
> ---
{:.card.card-task}

Wat is het internet?
--------------------

> Definitie
> ---
> Het **internet**[^internet] is het grootste computernetwerk ter wereld, en het bestaat eigenlijk uit verschillende aan elkaar gekoppelde netwerken.
{:.card.card-definition}

[^internet]: Het internet schrijven we met een **onderkast** (kleine letter) omdat het de laatste twee decennia zo alomtegenwoordig geworden is.

{% include shared/figure.html src="https://media.giphy.com/media/GrkrL1cGVv0FW/giphy.gif" alt="The internet: IT wrowd - Bron: Giphy.com" caption="The internet: IT wrowd - Bron: Giphy.com" %}

### Hoe moet je je dat voorstellen?

Het internet is een wereld waarin alle aangesloten computers een eigen, **uniek adres** hebben en waarin alle aangesloten computers gegevens kunnen uitwisselen over een wereldomspannend wegennet voor het vervoer van computerbestanden. Het unieke adres van de aangesloten computers wordt het **IP-adres** genoemd. Al die computers bij elkaar vormen de grootste, virtuele harde schijf van de wereld en je hebt toegang tot een heel groot deel van die wereldwijde harde schijf.

> Opgelet
> ---
> Het **World Wide Web** is slechts een onderdeel van het internet en is een gigantische verzameling van webpagina's 
{:.card.card-warning}

### Internetdiensten

Om de internetdiensten te kunnen voorzien, moeten er **protocollen** (afspraken) gemaakt worden. 

| Protocol      | Waarvoor wordt het gebruikt?                                |
|---------------|-------------------------------------------------------------|
| HTTP[^HTTP]   | Webpagina’s versturen.                                      |
| HTTPS[^HTTPS] | Webpagina’s versturen over een versleutelde verbinding.     |
| FTP[^FTP]     | Om bestanden te versturen.                                  |
| SFTP[^SFTP]   | Om bestanden te versturen over een versleutelde verbinding. |
| SMTP[^SMTP]   | Om e-mails te versturen en te ontvangen.                    |
{:.table.table--primary}

[^HTTP]: **HTTP**: Hypertext Transfer Protocol
[^HTTPS]: **HTTPS**: Hypertext Transfer Protocol Secure
[^FTP]: **FTP**: File Transfer Protocol
[^SFTP]: **SFTP**: SSH File Transfer Protocol
[^SMTP]: **SMTP**: Simple Mail Transfer Protocol

### Hoe werkt het internet?

> Definitie
> ---
> Een **pakketje** is een kleine hoeveelheid gegevens die als geheel verstuurd wordt. Het bevat onder andere de bestemmeling en gegevens.
{:.card.card-definition}

Via **TCP/IP**[^TCPIP] worden de pakketjes verstuurd:

[^TCPIP]: **TCP/IP**: Transmission Control Protocol/Internet Protocol

 - **Transmission Control Protocol**  
   Zorgt voor het opsplitsen in pakketjes en het terug samenstellen.
 - **Internet Protocol**  
   Zorgt voor het versturen van de individuele pakketjes. 

Een groot bestand versturen:

 1. Het bestand wordt eerst opgesplitst in vele pakketjes.
 1. Elk pakketje wordt afzonderlijk verstuurd.
 1. Het versturen verloopt via een aantal computers (servers).
 1. Elke tussenliggende computer stuurt een pakketje 1 **hop** verder en kiest een route via routering-tabellen. Elk pakketje kan een andere weg volgen.
 1. Bij de ontvanger wordt het bestand opnieuw samengesteld in de juiste volgorde.

> Tip
> ---
> Met de [Visual Trace Route Tool](http://www.monitis.com/traceroute/index.jsp?url=arteveldehogeschool.be&testId=1414916) kan je de **traceroute** (hops die de pakketjes volgen) naar een bepaald domein (bv. `arteveldehogeschool.be`) visueel laten weergeven.
{:.card.card-tip}

{% include shared/figure.html src="http://www.arteveldehogeschool.be/campusGDM/gdmgent/web-design/webd_traceroute_1.PNG" alt="Visual Trace Route Tool: facebook.com" caption="Visual Trace Route Tool: facebook.com" %}

> Definitie
> ---
> Een **server** is een gespecialiseerde computer die serversoftware bevat en diensten levert aan andere computers.
{:.card.card-definition}

Servers moeten doorgaans 24 uur per dag en 7 dagen per week hard werken en dat jaren aan een stuk. Daarom moet de hardware aan de hoogste kwaliteitseisen voldoen en is is die heel erg duur.

{% include shared/figure.html src="https://www.curvature.com/sites/default/files/poweredge-rack-servers-a.jpg" alt="Dell PowerEdge Rack Servers - Bron: Curvature" caption="Dell PowerEdge Rack Servers - Bron: Curvature" %}

### Adressen

Computers vinden elkaar via een IP-adres[^IP-adres]. Binnen een netwerk moeten IP-adressen uniek zijn.

[^IP-adres]: **IP-adres**: Internet Protocol-adres

Op Windows kunnen we met behulp van de [Command Prompt](https://www.lifewire.com/command-prompt-2625840) en CLI[^CLI] via het command `ipconfig` de IP-configuratie opvragen. Op [linux](https://www.linux.org/)-distributies kunnen we deze configuratie opvragen m.b.v [bash](https://linuxconfig.org/bash-scripting-tutorial) en CLI via het command [ifconfig](https://www.computerhope.com/unix/uifconfi.htm). Meer informatie omtrent CLI[^CLI] krijg je in het opleidingsonderdeel **besturingssystemen**.

[^CLI]: *CLI**: Command Line Interface

{% highlight bash %}
C:\Users\phildp>ipconfig

Windows IP Configuration


Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . : arteveldehs.be
   Link-local IPv6 Address . . . . . : fe80::1c55:bab6:71f2:c16d%4
   IPv4 Address. . . . . . . . . . . : 10.5.129.13
   Subnet Mask . . . . . . . . . . . : 255.255.254.0
   Default Gateway . . . . . . . . . : 10.5.129.254

Wireless LAN adapter Wi-Fi:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . : arteveldehs.be

Wireless LAN adapter Local Area Connection* 2:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 4:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Ethernet adapter Bluetooth Network Connection:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :
{% endhighlight %}

#### IPv4-adressen

IPv4[^IPv4] wordt momenteel nog veel gebruikt, maar biedt een onvoldoende aantal unieke IP-adressen voor alle toestellen die op het internet aangesloten zijn.

[^IPv4]: **IPv4**: Internet Protocol version 4

**32-bits** (4 groepen van 8-bits getallen).

Theoretisch zijn er $2^{32}$ mogelijke, unieke adressen. Dat zijn er meer dan **4 miljard**[^miljard].

[^miljard]: Een **miljard** [*(Eng. short scale: billion, (British) Eng. long scale: milliard)*](http://mathworld.wolfram.com/LargeNumber.html) is een getal met 9 nullen.

> Voorbeeld
> ---
> `192.168.0.1`
{:.card.card-example}

#### IPv6-adressen

IPv6[^IPv6] biedt een oplossing voor de tekortkomingen van IPv4, doordat het biedt: meer dan mogelijkheden.

[^IPv6]: **IPv6**: Internet Protocol version 6

**128-bits** (8 groepen van 4 hexadecimale cijfers).

Theoretisch zijn er $2^{128}$ mogelijke, unieke adressen. Dat zijn er meer dan **340 sexiljoen**[^sexiljoen].

[^sexiljoen]: Een **sexiljoen** [*(Eng. short scale: undecillion, (British) Eng. long scale: sexillion)*](http://mathworld.wolfram.com/LargeNumber.html) is een getal met 36 nullen.

> Voorbeeld
> ---
> `3ffe:6a88:85a3:08d3:1319:8a2e:0370:7344`
{:.card.card-example}

### Domeinnamen

#### Hoe kunnen mensen IP-adressen onthouden?

IP-adressen zijn makkelijk voor computers, maar niet zo gebruiksvriendelijk voor mensen. Die gebruiken liever makkelijk te onthouden **domeinnamen**.

**DNS**[^DNS] koppelt IP-adresssen aan domeinnamen. Meerdere IP-adressen kunnen aan 1 domeinnaam gekoppeld zijn, en vice versa.

[^DNS]: **DNS**: Domain Name System

> Voorbeeld
> ---
> - <http://www.arteveldehogeschool.be> is eigenlijk <http://193.191.137.217>
> - <http://www.gdm.gent> is eigenlijk <http://104.27.148.234> (Directe IP-toegang is in dit geval niet toegelaten)
> - <http://www.catawiki.be> is eigenlijk <http://88.221.69.175> (Directe IP-toegang is in dit geval niet toegelaten)
{:.card.card-example}

#### Anatomie van een domeinnaam

www.arteveldehogeschool.be

| Onderdeel             | Benaming  | Beheer             |
|-----------------------|-----------|--------------------|
| `www`                 | subdomein | Webserverbeheerder |
| `arteveldehogeschool` | domein    | DNS Belgium        |
| `.be`                 | TLD[^TLD] | ICANN              |
{:.table.table--primary}

[^TLD]: **TLD**: Top-Level Domain

> Task
> ---
> Hoeveel kost de registratie van een `.be`-domeinnaam voor een jaar?
{:.card.card-task}

[ICANN][] is een van oorsprong Amerikaanse non-profitorganisatie die de TLD's beheert:

| TLD         |  Type         | Betekenis                        |
|-------------|--------------:|----------------------------------|
| `.apple`    |  gTLD[^gTLD]  | Apple, Inc.                      |
| `.at`       | ccTLD[^ccTLD] | Oostenrijk                       |
| `.au`       | ccTLD         | Australië                        |
| `.com`      |  gTLD         | *Company*                        |
| `.ca`       | ccTLD         | Canada                           |
| `.cn`       | ccTLD         | China                            |
| `.de`       | ccTLD         | Duitsland                        |
| `.dk`       | ccTLD         | Denemarken                       |
| `.edu`      |  sTLD[^sTLD]  | *Education*                      |
| `.el`       | ccTLD         | Griekenland                      |
| `.es`       | ccTLD         | Spanje                           |
| `.eu`       | ccTLD         | Europese Unie                    |
| `.fi`       | ccTLD         | Finland                          |
| `.fr`       | ccTLD         | Frankrijk                        |
| `.google`   |  gTLD         | Google                           |
| `.ie`       | ccTLD         | Ierland                          |
| `.il`       | ccTLD         | Israël                           |
| `.it`       | ccTLD         | Italië                           |
| `.io`       | ccTLD         | Brits Indische Oceaanterritorium |
| `.lu`       | ccTLD         | Luxemburg                        |
| `.net`      |  gTLD         | *Network*                        |
| `.nl`       | ccTLD         | Nederland                        |
| `.no`       | ccTLD         | Noorwegen                        |
| `.org`      |  gTLD         | *Organization*                   |
| `.pt`       | ccTLD         | Portugal                         |
| `.se`       | ccTLD         | Zweden                           |
| `.tv`       | ccTLD         | Tuvalu                           |
| `.us`       | ccTLD         | Verenigde Staten                 |
| `.youtube`  |  gTLD         | YouTube                          |
| `localhost` |  tTLD[^tTLD]  | `127.0.0.1`                      |
| …           |             … | …                                |
{:.table.table--primary}

[^ccTLD]: **ccTLD**: Country-Code Top-Level Domain
[^gTLD]: **gTLD**: Generic Top-Level Domain
[^sTLD]: **sTLD**: Sponsored Top-Level Domain
[^tTLD]: **tTLD**: Test Top-Level Domain

> Opmerking
> ---
> Sinds **1 oktober 2016** is [ICANN een onafhankelijke organisatie](https://www.icann.org/news/announcement-2016-10-01-en) die niet langer afhangt van NTIA (Amerikaans Ministerie van Handel).
{:.card.card-remark}

| Belgische TLD |  Type | Beheer domeinnamen voor deze TLD |
|---------------|------:|----------------------------------|
| `.be`         | ccTLD | [DNS Belgium][]                  |
| `.brussels`   |  gTLD | [DNS Belgium][]                  |
| `.gent`       |  gTLD | [.GENT][]                        |
| `.vlaanderen` |  gTLD | [DNS Belgium][]                  |
{:.table.table--primary}

> Zie ook
> ---
> - [IANA Root Zone Database](http://www.iana.org/domains/root/db)
> - [IANA WHOIS](http://www.iana.org/whois)
{:.card.card-link}

De domeinnamen binnnen de Belgische TLD's domeinnamen (met als TLD `.be`, `.brussels` of `.vlaanderen`) worden beheerd door [DNS Belgium][].

Zelf een domeinnaam registreren doe je niet rechtstreeks bij [DNS Belgium][], maar via een erkende **Registrar**.

Om te weten wie achter een bepaalde domeinnaam schuil gaat, kun je de WHOIS-informatie raadplegen. Voor .be-domeinnamen kun je dat bijvoorbeeld via de website van dnsbelgium.be.

{% include shared/figure.html src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_webd1/whois_arteveldehogeschool.png" alt="" caption="In het voorbeeld hierboven kan je de WHOIS-gegevens van de domeinnaam <code>arteveldehogeschool.be</code> zien." %}

### Statistieken

Op 2018-09-12 zijn er:

 - [**7,649384491 miljard** mensen](http://www.worldometers.info/world-population/) op aarde.
 - [**4,018463745 miljard** internetgebruikers](http://www.internetlivestats.com/internet-users/), ca. **52,5 %** van de wereldbevolking.
 - [**1,47 miljard** dagelijks actieve Facebook-gebruikers](http://newsroom.fb.com/company-info/) per maand.

#### Meest bezochte websites (2018-09-12)

Het World Wide Web
------------------

> Definitie
> ---
> Het WWW[^WWW], ook gekend als **W3** of het **Web** is een met elkaar verbonden systeem van webdocumenten (webpagina's) en andere bronnen of **resources** (documenten, afbeeldingen, video's, audio-bestanden en andere content) en is toegankelijk via het internet.
{:.card.card-definition}

Het WWW is dus niet gelijk aan het internet. Het internet, de infrastructuur of het onderliggende netwerksysteem, geeft toegang tot o.a. het WWW. Het Web is dus een service gebouwd bovenop het internet, net zoals email, IRC[^IRC], ... . De meeste gebruikers gebruiken een webbrowser om toegang te krijgen tot het WWW.



[^WWW]: **WWW**: World Wide Web
[^IRC]: **IRC**: Internet Relay Chat

{% include shared/figure.html src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b2/WWW_logo_by_Robert_Cailliau.svg/2000px-WWW_logo_by_Robert_Cailliau.svg.png" alt="Origineel W3 logo door Robert Cailliau - Bron: Wikimedia" caption="Origineel W3 logo door Robert Cailliau - Bron: Wikimedia" %}




> References
> ---
> - [Technopedia: World Wide Web](https://www.techopedia.com/definition/5217/world-wide-web-www)
> - [Mozilla Developer Network: World Wide Web](https://developer.mozilla.org/en-US/docs/Glossary/World_Wide_Web)
{:.card.card-source}


Wat is een webpagina?
---------------------

> Definitie
> ---
> Een **webpagina** is een tekstbestand met daarin gestandaardiseerde codes, zoals HTML[^HTML] of CSS[^CSS].
{:.card.card-definition}

[^HTML]: **HTML**: Hypertext Markup Language
[^CSS]: **CSS**: Cascading Style Sheets

Deze tekst en codes kunnen door de browser omgezet worden in een grafische webpagina. Dit omzetten heet **renderen** (weergeven). 

Een webpagina bevat meerstal ook **hyperlinks** waarmee men naar een andere pagina kan springen (= surfen).

Dankzij standaardisatie renderen recente browsers elke webpagina bijna identiek. Dit is vroeger wel eens anders geweest!

> Opmerking
> ---
> Het **besturingssysteem** heeft nog altijd een belangrijke invloed op de weergave, omdat de manier waarop lettertypes gerenderd worden per besturingssysteem verschilt!
{:.card.card-remark}

> Taak
> ---
> Bekijk de broncode van de homepagina van deze websites:
>
> - [*&nbsp;*{:.fab.fa-fw.fa-facebook}Facebook][]
> - [*&nbsp;*{:.fab.fa-fw.fa-twitter}Twitter][]
> - [Stad Gent](https://stad.gent)
{:.card.card-task}

> Firefox Developer Edition
> ---
> De broncode van een webpagina bekijken.  
> <kbd class="menu"><kbd>RMK</kbd>&#9656;<kbd>Paginabron bekijken</kbd></kbd>
{:.card.card-firefox}

Webstandaarden
--------------

### Wat doet het W3C[^W3C]?

[^W3C]: **W3C**: World Wide Web Consortium

Het *[World Wide Web Consortium][W3C]* ontwikkelt open standaarden en richtlijen voor het web.

Het W3C heeft [meer dan 400 leden](https://www.w3.org/Consortium/Member/List).

Er is ook een afdeling voor de Benelux: [W3C Benelux](http://www.w3c.nl).

### Standaarden

Enkele belangrijke standaarden:

 - CSS3
 - DOM3
 - HTML5
 - MathML
 - SVG
 - XHTML 1.0
 - XML

Korte geschiedenis van het WWW
------------------------------

> Zie ook
> ---
> - [Mijlpalen in de geschiedenis van Nieuwe Media](http://www.gdm.gent/1718-wanm/mijlpalen/)
{:.card.card-link}

**1910**{:.badge.badge--default} [Mundaneum][]
: Twee juristen, **Paul Otlet** (BE) & **Henri La Fontaine** (BE), starten in het Brusselse Jubelpark een instituut om alle kennis van de wereld te verzamelen. Een soort “Google op papier”.

**1969**{:.badge.badge--default} ARPANET
: [DARPA][] (US) bouwt het ARPA Network, de eerste versie van het internet. Het is een netwerk van knooppunten die zeer betrouwbare communicatie toelaat, omdat communicatie tussen twee knooppunten nog altijd via een omweg kan gebeuren.

**1986**{:.badge.badge--default} [SGML](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.htm?csnumber=16387)
: SGML is een ISO-standaard voor de syntaxis van markuptalen. Met behulp een DTD kan een subset van SGML worden gemaakt, met een bepaalde syntaxis. HTML is zo een subset.
: *computertaal*{:.badge.badge--pill.badge--primary}

**1990**{:.badge.badge--default} WorldWideWeb & HyperText
: Twee medewerkers van [CERN][] (FR/CH), **Tim Berners-Lee** (UK) en **Robert Calliau** (BE), schrijven het projectvoorstel [WorldWideWeb: Proposal for a HyperText Project](https://www.w3.org/Proposal.html) waarin ze het concept van **HyperText** beschrijven.
: *computerwetenschappen*{:.badge.badge--pill.badge--primary}

**1990**{:.badge.badge--default} WorldWideWeb (Nexus)
: **Tim Berners-Lee** (UK) brengt de allereerste browser uit. Later krijgt WorldWideWeb de naam **Nexus** om verwarring met het *World Wide Web* te vermijden.
: *webbrowser*{:.badge.badge--pill.badge--primary}

**1993**{:.badge.badge--default} NCSA Mosaic (US)
: *webbrowser*{:.badge.badge--pill.badge--primary} De eerste populaire grafische browser en voorloper van Microsoft Internet Explorer

**1993**{:.badge.badge--default} HTML
: **Tim Berners-Lee** (UK) en **Daniel Connolly** (US) publiceren [HTML](https://www.w3.org/MarkUp/draft-ietf-iiir-html-01)
: *computertaal*{:.badge.badge--pill.badge--primary}

**1994**{:.badge.badge--default} World Wide Web Consortium (W3C)
: **Tim Berners-Lee** (UK) richt het [World Wide Web Consortium (W3C)](https://www.w3.org/Consortium/facts.html) op aan MIT/LCI in samenwerking met het CERN.

**1995**{:.badge.badge--default} HTML 2.0 &mdash; RFC 1866
: De *HTML Working Group* van IETF publiceert [RFC 1866](https://tools.ietf.org/html/rfc1866).
: *computertaal*{:.badge.badge--pill.badge--primary}

**1997**{:.badge.badge--default} HTML 3.2 &mdash; W3C Recommendation
: Het W3C publiceert [W3C Recommendation voor HTML 3.2](https://www.w3.org/TR/REC-html32).
: *computertaal*{:.badge.badge--pill.badge--primary}

**1999**{:.badge.badge--default} HTML 4.01 &mdash; W3C Recommendation
: Het W3C publiceert [W3C Recommendation voor HTML 4.01](https://www.w3.org/TR/html4/).
: *computertaal*{:.badge.badge--pill.badge--primary}

**2000**{:.badge.badge--default} XHTML 1.0 &mdash; W3C Recommendation
: Het W3C publiceert [W3C Recommendation voor XHTML](https://www.w3.org/TR/xhtml1/). Dit is eigenlijk HTML die in XML gemaakt is. XHTML is makkelijker door software te verwerken dan HTML, omdat het aan de strengere XML-syntaxisregels moet voldoen.
: *computertaal*{:.badge.badge--pill.badge--primary}

**2008**{:.badge.badge--default} HTML5 &mdash; W3C Working Draft
: Het W3C publiceert [W3C Working Draft voor HTML5](https://www.w3.org/TR/2008/WD-html5-20080122/), de aanzet voor de eerste nieuwe HTML-standaard sinds HTML 4.01 uit 1999.
: *computertaal*{:.badge.badge--pill.badge--primary}

**2012**{:.badge.badge--default} HTML5 &mdash; W3C Candidate Recommendation
: Het W3C publiceert [W3C Candidate Recommendation voor HTML5](https://www.w3.org/TR/2012/CR-html5-20121217/). Hoewel de standaard nog niet helemaal af is, is de browserondersteuning goed en wordt HTML5 al op grote schaal toegepast.
: *computertaal*{:.badge.badge--pill.badge--primary}

**2014**{:.badge.badge--default} HTML5 &mdash; W3C Recommendation
: Het W3C publiceert [W3C Recommendation voor HTML5][HTML5], de definitieve standaard voor HTML5, die de voorgaande versies van zowel HTML als XHTML vervangt.
: *computertaal*{:.badge.badge--pill.badge--primary}

Internetgebruik
---------------

> Taken
> ---
> Welke conclusies kun je trekken uit onderstaande informatie van [How We Browse The Web](http://howwebrowse.be):
>
> - [Apparaten - De afgelopen 12 maanden         ](http://howwebrowse.be/nl/report/device/last_12_months/e30=)
> - [Apparaten - Dagen van de week               ](http://howwebrowse.be/nl/report/device/weekdays/e30=)
> - [Besturingssystemen - De afgelopen 12 maanden](http://howwebrowse.be/nl/report/os/last_12_months/e30=)
> - [Besturingssystemen - Dagen van de week      ](http://howwebrowse.be/nl/report/os/weekdays/e30=)
> - [Browsers - De afgelopen 12 maanden          ](http://howwebrowse.be/nl/report/browser/last_12_months/e30=)
> - [Browsers - Dagen van de week                ](http://howwebrowse.be/nl/report/browser/weekdays/e30=)
>
> Welke conclusies kun je trekken uit de informatie van [W3 Counter Browser & Platform Market Share](https://www.w3counter.com/globalstats.php?year=2016&month=9)?
{:.card.card-task}

World Wide Web
--------------

Applicaties
----------- 