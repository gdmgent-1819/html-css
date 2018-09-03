---
title: Tabellen
title_long: Tabellen
permalink: markup/html/tables/
---

Basis
-----

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