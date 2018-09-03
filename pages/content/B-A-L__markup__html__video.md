---
title: Video
title_long: Video
permalink: markup/html/video/
---

Externe bron
--------------------------

Je kan je filmpjes door een externe dienst laten hosten en op je website afspelen. Bekende diensten zijn Youtube, vimeo, ..
Zij voorzien gebruiksvriendelijke afspeler en extra parameters.
Je upload je filmpje op YouTube of Vimeo, daarom nemen ze geen ruimte op je eigen server in. Vervolgens **embed** je het filmpje.

{% highlight html %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/JAM3OjMTuNc?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
{% endhighlight %}

Dit zal resulteren in het volgende:

<iframe width="560" height="315" src="https://www.youtube.com/embed/JAM3OjMTuNc?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

Je zal zien dat de code gebruik maakt van de attributen `width` en `height`.

Zelf hosten
------------

Als je je filmpje niet wilt hosten op externe servers dan kan je het zelf hosten. De oplossing hiervoor is het `video`-element.
{% highlight html %}
<video src="video.mp4" controls></video>
{% endhighlight %}

We kunnen meerdere bronnen voor de video meegeven. Indien hij een `source` niet kan laden, gaat hij naar het volgende `source`-bestand. Waarbij hij uiteindelijk op de fallback-image komt.

{% highlight html %}
<video controls>
    <source src="video.webm" type="video/webm">
    <source src="video.mp4" type="video/mp4">
    <img src="video_fallback.jpg" alt="video fallback">
</video>
{% endhighlight %}

`video`-attributen

| HTML-attribuut | Betekenis                                                                |
|----------------|---------------|--------------------------------------------------------- |
| `autoplay`    | Geeft aan dat een video start met spelen wanneer het klaar is met laden.  |
| `controls`    | Geeft aan dat de bedieningsknoppen, zoals play/pause, zichtbaar zijn.     |
| `height`      | Geeft de hoogte weer                                                      |
| `loop`        | Geeft aan dat de video zichzelf herhaalt als de video gedaan is met afspelen. |
| `muted`       | Geeft aan dat het geluid van de video gedemt moet zijn.                   |
| `src`         | Geeft de URL van de video weer                                            |
| `width`       | Geeft de breedte weer                                                     |
{:.table.table--primary}