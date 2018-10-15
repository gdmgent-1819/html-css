---
title: Tabellen
title_long: Tabellen
permalink: markup/html/tables/
---

Tabulaire data
--------------

In [Microsoft Excel](https://products.office.com/en-us/excel) is een goed voorbeeld van software dat werkt met tabulaire data of "table data". Deze data is gestructureerd m.b.v. rijen en kolommen. Excel laat toe om de data te exporteren naar CSV[^CSV]. CSV is al redelijk oud en wordt nog dikwijls gebruikt als de standaard voor tabulaire data.

> Definitie
> ---
> CSV[^CSV] staat voor Comma-seperated values of character-seperated values.
{:.card.card-definition}

CSV wordt vaak omschreven als "Tabular data in plain text vorm". Bevat geen algemene standaard, maar een paar suggesties worden aangeboden via [RFC4180](https://tools.ietf.org/html/rfc4180). CSV bestaat uit een verzameling van **records** (rijen) gescheiden door een **line break** of iets gelijkaardigs. Meestal hebben alle records hetzelfde aantal velden. Ieder record bestaat uit een aantal velden gescheiden door een **comma** of iets gelijkaardigs, bijv: tab, `;` , … .

Het CSV-formaat is beschikbaar in vele applicaties via import/export functionaliteiten. Incompatibele programma’s kunnen via CSV data met elkaar uitwisselen, bijv.: export van gegevens uit een databank en vervolgens import van deze gegevens via CSV in een spreadsheet.

[^CSV]: CSV: Comma Seperated Values.

### Syntax

Enkele vooropgestelde regels om CSV op te stellen:

- **plain text** gebruik makend van een character set, zoals: ASCII en **Unicode**;
- bestaat uit records, meestal één record per regel;
- een record wordt onderverdeeld in velden;
- de velden worden gescheiden via een delimiter of separator;
- elk record bestaat uit hetzelfde aantal velden.

Deze regels zijn weliswaar niet vastgelegd in een standaard, maar worden toch algemeen aangenomen.

### Voorbeeld(en)

{% include shared/figure.html src="http://www.arteveldehogeschool.be/campusGDM/wanm/1617_nmdad1/csv_example1.png" alt="Tabulaire data: CSV Voorbeeld Locaties Gentse Feesten" caption="Tabulaire data: CSV Voorbeeld Locaties Gentse Feesten" %}

> References
> ---
> - [FRICTIONLESS DATA: CSV - Comma Separated Values](http://frictionlessdata.io/docs/csv/)
> - [Wikipedia: Comma Separated Values](http://en.wikipedia.org/wiki/Comma-separated_values)
> - [IETF: RFC4180](http://tools.ietf.org/html/rfc4180)
{:.card.card-source}


`<table>`{:.e}-element
----------------------

> Definitie
> ---
> Het `<table>`{:.e}-element representeert tabulaire (Eng.: tabular) data, dat is informatie dat beschreven is een twee dimensionale (Eng.: two-dimensional) tabel (cfr. array) bestaande uit rijen (Eng.: rows) en kolommen (Eng.: columns).
{:.card.card-definition}

| HTML-element   | Betekenis                      |
|----------------|--------------------------------|
| `<table>`{:.e} | tabel                          |
| `<tr>`{:.e}    | *table row*, tabelrij          |
| `<td>`{:.e}    | *table data*, tabelgegevenscel |
| `<th>`{:.e}    | *table heading*, tabelkopcel   |
{:.table.table--primary}

Een cel ( `<td>`{:.e} of  `<th>`{:.e}) heeft een aantal optionele attributen.

| HTML-attribuut | Waarde        | Betekenis                                           |
|----------------|---------------|-----------------------------------------------------|
| `colspan`{:.a} | `«aantal»`{:.v} | de cel overspant een `«aantal»`{:.v} **kolommen** |
| `rowspan`{:.a} | `«aantal»`{:.v} | de cel overspant een `«aantal»`{:.v} **rijen**    |
{:.table.table--primary}

Intermediair
------------

| HTML-element   | Betekenis              | Aantal toegestaan per tabel |
|----------------|------------------------|-----------------------------|
| `<thead>`{:.e} | *table head row group* | 1                           |
| `<tbody>`{:.e} | *table body row group* | 1 of meer                   |
| `<tfoot>`{:.e} | *table foot row group* | 1                           |
{:.table.table--secondary}


> References
> ---
> - [Mozilla Developer Network: Table element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
> - [UX Design: Design better Data tables](https://uxdesign.cc/design-better-data-tables-4ecc99d23356)
{:.card.card-source}