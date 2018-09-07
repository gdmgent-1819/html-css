HTML-commentaar
---------------

Soms is het handig of zelfs nodig om HTML-code te becommentariëren. Door commentaar te voorzien help je de code te verduidlijken, niet enkel voor andere HTML-coders, maar ook voor je toekomstige zelf, want weet je over pakweg een jaar nog hoe je die complexe webpagina precies hebt opgebouwd? Die commentaar is enkel zichtbaar in de broncode en nooit op de pagina zelf.

Commentaar schrijven tussen de HTML-code doe je tussen de **begintag** (`<!--`{:.e}) en **eindtag** (`-->`{:.e}).

{% highlight html %}
<!-- Dit is commentaar. Alles, ook HTML-elementen, binnen deze twee tags wordt genegeerd door de browser. -->
{% endhighlight %}

> Opmerking
> ---
> Overdrijf niet met HTML-commentaar, want bij elk paginabezoek moet die ook gedownload worden terwijl dit geen enkel nut heeft voor de doorsnee websitebezoeker. Liefst wordt de commentaar verwijderd voor de website op de productieserver geplaatst wordt.
>
> Duidelijk geschreven code heeft weinig tot geen commentaar nodig, maar als beginner kan het wel een handige geheugensteun zijn. 
{:.card.card-remark}

> Tip
> ---
> Omdat de browser HTML-tags binnen commentaar negeert kan je dit gebruiken om code tijdelijk uit te schakelen, bijvoorbeeld om iets uit te proberen.
{:.card.card-tip}