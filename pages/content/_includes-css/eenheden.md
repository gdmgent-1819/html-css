Absolute lengte-eenheden
------------------------

| Eenheid *(Eng.: unit)* | Omschrijving                      |
|------------------------|-----------------------------------|
| `cm`                   | centimeter                        |
| `mm`                   | millimeter                        |
| `inch`                 | inch (`1in` = `96px` = `2.54cm`)  |
|------------------------|-----------------------------------|
| `px`                   | pixel (`1px` = 1/96ste van `1in`) |
| `pt`                   | point (`1pt` = 1/72ste van `1in`) |
| `pc`                   | pica (`1pc`  = `12pt`)            |
{:.table.table--primary.table--bordered}

Relatieve lengte-eenheden
-------------------------

| Eenheid *(Eng.: unit)* | Omschrijving                                                                           |
|------------------------|----------------------------------------------------------------------------------------|
| `em`                   | relatief t.o.v. de fontgrootte van het element                                         |
| `rem`                  | relatief t.o.v. de fontgrootte van het root-element                                    |
| `%`                    | relatief t.o.v. de breedte van het element                                             |
|------------------------|----------------------------------------------------------------------------------------|
| `vw`                   | relatief t.o.v. de `1%` van de breedte van de viewport                                 |
| `vh`                   | relatief t.o.v. de `1%` van de hoogte van de viewport                                  |
| `vmin`                 | relatief t.o.v. de kleinste waarde van de `1%` van de breedte en de `1%` van de hoogte |
| `vmax`                 | relatief t.o.v. de grootste waarde van de `1%` van de breedte en de `1%` van de hoogte |
|------------------------|----------------------------------------------------------------------------------------|
{:.table.table--primary.table--bordered}

Dimensies
---------

 - `width:`{:.p}  
   Breedte van een element. De `padding:`{:.p} en `border-width:`{:.p} worden niet meegerekend.
 - `height:`{:.p}  
   Hoogte van een element. De `padding:`{:.p} en `border-width:`{:.p} worden niet meegerekend.
 - `min-width:`{:.p}  
   De minimale breedte van een element. Dit voorkomt dat het element kleiner wordt dan de opgegeven waarde.
 - `min-height:`{:.p}  
   De minimale hoogte van een element. Dit voorkomt dat het element kleiner wordt dan de opgegeven waarde.
 - `max-width:`{:.p}  
   De maximale breedte van een element. Dit voorkomt dat het element groter wordt dan de opgegeven waarde. Overschrijft de `width:`{:.p} van het element.
 - `max-height:`{:.p}  
   De maximale hoogte van een element. Dit voorkomt dat het element groter wordt dan de opgegeven waarde. Overschrijft de `height:`{:.p} van het element.