Border *(Ned.: rand)*
---------------------

> - `border-width:`{:.p} `«randdikte»`{:.v} &#124; `thin`{:.k} &#124; `medium`{:.k} &#124; `thick`{:.k}
> - `border-style:`{:.p} `«randstijl»`{:.v} &#124; `solid`{:.k} &#124; `dashed`{:.k} &#124; `dotted`{:.k} &#124; …
> - `border-color:`{:.p} `«randkleur»`{:.v}
>
> Shorthand:
>
>  - `border:`{:.p} `«border-width»`{:.v} `«border-style»`{:.v} `«border-color»`{:.v}
>
> In **wijzerzin** van boven naar links:
>
>  1. `border-top:`{:.p} `«border-top-width»`{:.v} `«border-top-style»`{:.v} `«border-top-color»`{:.v}
>    - `border-top-width:`{:.p} `«randdikte»`{:.v}
>    - `border-top-style:`{:.p} `«randstijl»`{:.v}
>    - `border-top-color:`{:.p} `«randkleur»`{:.v}
>  2. `border-right:`{:.p} `«border-right-width»`{:.v} `«border-right-style»`{:.v} `«border-right-color»`{:.v}
>    - `border-right-width:`{:.p} `«randdikte»`{:.v}
>    - `border-right-style:`{:.p} `«randstijl»`{:.v}
>    - `border-right-color:`{:.p} `«randkleur»`{:.v}
>  3. `border-bottom:`{:.p} `«border-bottom-width»`{:.v} `«border-bottom-style»`{:.v} `«border-bottom-color»`{:.v}
>    - `border-bottom-width:`{:.p} `«randdikte»`{:.v}
>    - `border-bottom-style:`{:.p} `«randstijl»`{:.v}
>    - `border-bottom-color:`{:.p} `«randkleur»`{:.v}
>  4. `border-left:`{:.p} `«border-left-width»`{:.v} `«border-left-style»`{:.v} `«border-left-color»`{:.v}
>    - `border-left-width:`{:.p} `«randdikte»`{:.v}
>    - `border-left-style:`{:.p} `«randstijl»`{:.v}
>    - `border-left-color:`{:.p} `«randkleur»`{:.v}

#### Afrondingen

> - `border-radius:`{:.p} `«straal»`{:.v}
> - `border-radius:`{:.p} `«x-straal»`{:.v} `/` `«y-straal»`{:.v}
> - `border-radius:`{:.p} `«straal-linksboven»`{:.v} `«straal-rechtsboven»`{:.v} `«straal-rechtsonder»`{:.v} `«straal-linksonder»`{:.v}
>
> In **wijzerzin** van linksboven naar linksonder:
>
>  1. `border-top-left-radius:`{:.p} `«straal-linksboven»`{:.v}
>  2. `border-top-right-radius:`{:.p} `«straal-rechtsboven»`{:.v}
>  3. `border-bottom-right-radius:`{:.p} `«straal-rechtsonder»`{:.v}
>  4. `border-bottom-left-radius:`{:.p} `«straal-linksonder»`{:.v}

{% highlight html %}
<div class="voorbeelden">
    <div class="voorbeelden__vierkant"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--rand"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--dikke-bovenrand"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--ronde-hoeken"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--ronde-linker-bovenhoek"></div>
    <div class="voorbeelden__vierkant voorbeelden__vierkant--vlakgeronde-hoeken"></div>
</div>
{% endhighlight %}

{% highlight css linenos %}
.voorbeelden__vierkant {
    background-color: #BADA55;	
    height: 200px;
    width: 200px;
}

.voorbeelden__vierkant--rand {
    border: 1px solid #F00;
}

.voorbeelden__vierkant--dikke-bovenrand {
    border: 1px dashed #F00;
    border-top: 10px solid #00F;
}

.voorbeelden__vierkant--ronde-hoeken {
    border-radius: 10px;
}

.voorbeelden__vierkant--ronde-linker-bovenhoek {
    border-top-left-radius: 50px;
}

.voorbeelden__vierkant--vlakgeronde-hoeken {
    border-radius: 100px/20px;
}
{% endhighlight %}{:data-file="main.css"}