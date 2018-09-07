Lijst van beschrijvingen
------------------------

 - `<dl>`{:.e} … `</dl>`{:.e} *(**Description List**)* is een *descendant* van `<body>`{:.e}
 - Bevat een of meerdere *children:* `<dt>`{:.e} … `</dt>`{:.e} *(**Description Term**)*  
   die onmiddellijk gevolgd worden door een of meerdere `<dd>`{:.e} … `</dd>`{:.e} *(**Description Data**).* 

{% highlight html %}
<dl>
    <dt>Hypertext Transfer Protocol</dt>
    <dd>Protocol voor webcommunicatie.</dd>
    <dd>Afgekort als <abbr title="Hypertext Transfer Protocol">HTTP</abbr>.</dd>
    <dt>Hypertext Transfer Protocol Secure</dt>
    <dd>Protocol voor webcommunicatie over een beveiligde verbinding.</dd>
    <dd>Afgekort als <abbr title="Hypertext Transfer Protocol Secure">HTTPS</abbr>.</dd>
</dl>
{% endhighlight %}