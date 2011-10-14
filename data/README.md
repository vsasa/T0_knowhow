Skripte za import šifrarnika fmk u xtuple bazu
==================================================

* roba.csv - sadrži tekuće šifre robe koje se koriste u bring.out-u
* roba_map.xls - map fajl za xtuple CSVIMP

Kako importovati ?
------------------

Pokrenemo CSVIMP i otvorimo csv fajl na meniju open.

Zatim, nakon što se učita, idemo na opciju 'map->edit', nakon što se otvori prozor map
sa menija file->open otvaramo priloženi xml fajl.

Nakon što se učitao map fajl, prebacujemo se na csv prozor i biramo opciju start sa menija import.

Pogledaj upute na [aktivnosti #24699](http://redmine.bring.out.ba/issues/24699)

Priprema CSV fajla iz roba.dbf
-------------------------------

Otvoriti tabelu roba.dbf u openoffice-u te uraditi sljedeće korake:

* ukloniti kompletnu kolonu BRISANO
* izvršiti konverziju naših karaktera č, ć, ž... na polju NAZIV
* izvršiti konverziju na polju NAZIV, mjenjamo , (zarez) sa prazno - OVAJ KORAK JE JAKO BITAN!!!
* snimamo fajl kao CSV fajl i pri tome odabiremo sljedeće parametre, field delimiter: , (zarez), text delimiter: prazno

