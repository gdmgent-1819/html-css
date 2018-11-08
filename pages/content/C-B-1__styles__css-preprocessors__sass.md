---
title: Sass
title_long: Synthetic Awesome StyleSheet
permalink: styles/css-preprocessors/sass/
published: true
---

Wat is Sass?
------------

> Definitie
> ---
> Sass, Syntactically Awesome Stylesheets, is een scripttaal dat geïnterpreerd of geconverteerd wordt in Cascading Style Sheets (CSS). Sass bestanden zijn herkenbaar door de extensies `.sass` en `.scss`.
{:.card.card-definition}

De `.sass`-bestanden bevatten de oude syntax die gebasseerd is op **indentation** en **new line characters**. De nieuwere syntax in `.scss`-bestanden gebruikt **block formatting** zoals in CSS, een blok wordt gestart met `{` en afgesloten met `}`. Punt-comma's (semi-colons) `;` worden gebruikt om lijnen code binnen een blok te separeren. Kortom de synax van `.scss`-bestanden is nagenoeg identiek dan die van pure CSS. SassScript is de scripttaal voor Sass en brengt extra nuttige functies en eigenschappen toe aan Sass.

> References
> ---
> - [Sass language](http://sass-lang.com/)
> - [Wikipedia: Sass (stylesheet language)](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
{:.card.card-source}

Once you start tinkering with Sass, it will take your preprocessed Sass file and save it as a normal CSS file that you can use in your website.

The most direct way to make this happen is in your terminal. Once Sass is installed, you can compile your Sass to CSS using the sass command. You'll need to tell Sass which file to build from, and where to output CSS to. For example, running sass input.scss output.css from your terminal would take a single Sass file, input.scss, and compile that file to output.css.

You can also watch individual files or directories with the --watch flag. The watch flag tells Sass to watch your source files for changes, and re-compile CSS each time you save your Sass. If you wanted to watch (instead of manually build) your input.scss file, you'd just add the watch flag to your command, like so:

sass --watch input.scss output.css

You can watch and output to directories by using folder paths as your input and output, and separating them with a colon. In this example:

sass --watch app/sass:public/stylesheets
Sass would watch all files in the app/sass folder for changes, and compile CSS to the public/stylesheets folder.


Developer criticism includes the issue that CSS preprocessor variables are static and have lexical scope, whereas native CSS variables are dynamic and are scoped to the DOM. Variables are actually embodied in CSS properties. A common application where a variable scoped to the DOM is to create a layout with variable spacing for a gutter to accommodate different browser window sizes. This task is difficult for Sass, the most popular CSS preprocessor going into 2018, but it is more easily done with native CSS custom properties. Here is a layout with three window size variations:

Syntax
------

Sass laat toe om **variables**, **nested rules**, **mixins**, **inline imports**, ... te implementeren met een CSS-compatiebele syntax. Via Sass kunnen we grote stylesheets goed organiseren.

### Variables

{% highlight sass %}
$primary-color: #3bbfce;
$margin: 16px;

h1 {
  color: $primary-color;
  margin: $margin/2 0;
}
{% endhighlight %}

De resulterende CSS:

{% highlight css %}
h1 {
    color: #3bbfce;
    margin: 8px 0;
}
{% endhighlight %}

### Nesting

{% highlight sass %}
nav {
    background-color: #e50000;
    ul {
        list-style: none;
        li { 
            margin: 10px;
            float: left;
        }
    }
}

{% endhighlight %}

De resulterende CSS:

{% highlight css %}
nav {
    background-color: #e50000;
}
nav ul { 
    list-style: none;
}
nav ul li {
    margin: 10px;
    float: left;
}
{% endhighlight %}

### Mixins

Group of css code with the possibility to pass a variable

{% highlight sass %}
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

.block {
    @include border-radius(10px);
}
{% endhighlight %}

De resulterende CSS:

{% highlight css %}
.block {
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  -ms-border-radius: 10px;
  border-radius: 10px;
}
{% endhighlight %}

### Loops

`@for`, `@each`, `@while`

{% highlight sass %}
$columns: 12;
@for $i from 1 through $columns {
  .col-#{$i} {
    width: 100% / ($columns/$i);
    display: block;
    float: left;
   }
}
{% endhighlight %}

De resulterende CSS:

{% highlight css %}
.col-1 {
  width: 100%;
  display: block;
  float: left; 
}
...
.col-12 {
  width: 8.33333%;
  display: block;
  float: left; 
}
{% endhighlight %}

### Inheritance

{% highlight sass %}
.message {
    display: block;
    padding: 15px;
    @include border-radius(10px);
}

.error {
    color: #F00;
    @extend .message;
}

{% endhighlight %}

De resulterende CSS:

{% highlight css %}
.message {
    display: block;
    padding: 15px;
    -webkit-border-radius: 10px;
    -moz-border-radius: 10px;
    -ms-border-radius: 10px;
    border-radius: 10px;
}

.error {
    color: #F00;
    display: block;
    padding: 15px;
    -webkit-border-radius: 10px;
    -moz-border-radius: 10px;
    -ms-border-radius: 10px;
    border-radius: 10px;
}
{% endhighlight %}

> References
> ---
> - [Sass language: full documentation](http://sass-lang.com/documentation/file.SASS_REFERENCE.html)
{:.card.card-source}

Transpiling
-----------

### Optie 1: Via software

> References
> ---
> - [Koala app](http://koala-app.com/)
> - [Scout-App](http://scout-app.io/)
{:.card.card-source}

### Optie 2: Sass CLI

Installatie (globale) van het Sass CLI-tool via npm.

{% highlight bash %}
npm install -g sass
{% endhighlight %}

Op macOS is het mogelijk dat we dit commando moeten uitvoeren met `sudo`:

{% highlight bash %}
sudo npm install -g sass
{% endhighlight %}

### VSCode-pluigins

> References
> ---
> - Indented Sass syntax highlighting, autocomplete & snippets for VSCode(https://marketplace.visualstudio.com/items?itemName=robinbentley.sass-indented)
> - Live Sass Compiler(https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)
> - Sass Lint(https://marketplace.visualstudio.com/items?itemName=glen-84.sass-lint)
> - Beautify css/sass/scss/less(https://marketplace.visualstudio.com/items?itemName=glen-84.sass-lint)
{:.card.card-source}

### Optie 3: Gulp

#### Stap 1: npm (Node Package Manager)

Controlleer of je reeds npm geinstalleerd hebt door de versie op te vragen

{% highlight bash %}
npm --version
{% endhighlight %}

Indien niet installeer [node.js](https://nodejs.org/en/download/)

#### Stap 2: node-sass installeren

{% highlight bash %}
npm install -g node-sass
{% endhighlight %}

Mac gebruikers moeten eventueel dit commando uitvoeren onder Super User:

{% highlight bash %}
sudo npm install -g node-sass
{% endhighlight %}

#### Stap : gulp en gulp-sass installeren

{% highlight bash %}
npm install -g gulp
{% endhighlight %}

{% highlight bash %}
npm install -g gulp gulp-sass
{% endhighlight %}

Mac

{% highlight bash %}
sudo npm install -g gulp
{% endhighlight %}

{% highlight bash %}
sudo npm install -g gulp gulp-sass
{% endhighlight %}

#### Stap 4: creating a project

!!! In de **root** van je website run volgend commando uitvoeren

{% highlight bash %}
npm init --yes
{% endhighlight %}

Dit zal een package.json aanmaken in de root van je website.
Daarna voer je volgende commando uit:

{% highlight bash %}
npm install gulp --save-dev
{% endhighlight %}

{% highlight bash %}
npm install gulp-sass --save-dev
{% endhighlight %}

#### Stap 5: Maak je scss file aan

- Maak een folder `sass` aan in de root van je project. Deze folder dient enkel voor het coderen van je css en hoeven dus niet op de server geplaatst worden bij de deploy van je website.
- In deze folder maak je een main.scss aan met je eerste regels sass.
- Zorg ook dat er een `styles` folder aanwezig is. De gecompileerde css bestanden zullen in deze folder terecht komen.

#### Stap 6: gulp file

> **Automation of your workflow**

Maak een gulp file `gulpfile.js` aan in de root van je project

{% highlight js %}
'use strict';
 
var gulp = require('gulp');
var sass = require('gulp-sass');
 
gulp.task('sass', function () {
  return gulp.src('./sass/**/*.scss')
    .pipe(sass().on('error', sass.logError))
    .pipe(gulp.dest('./styles'));
});

gulp.task('watch', function () {
  gulp.watch('./sass/**/*.scss', ['sass']);
});
{% endhighlight %}

Run via terminal in de directory van je project:

{% highlight bash %}
gulp watch
{% endhighlight %}

#### Uitbereidingen

Je kan in deze gulp file nog meer automatisatie toevoegen. 
Zoals bijvoorbeeld:
- Javascript en css bestanden opkuisen en comprimeren (minify)
- Automatisch herladen van je browservenster telkens je aanpassingen doet aan je scss
- ...

[Lees meer over deze workflow en uitbereidingen hierop](https://css-tricks.com/gulp-for-beginners/)

