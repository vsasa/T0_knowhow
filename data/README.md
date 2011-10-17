Skripte za import šifrarnika fmk u xtuple bazu
==================================================

* roba.csv - sadrži tekuće šifre robe koje se koriste u bring.out-u
* roba_map.xls - map fajl za xtuple CSVIMP

Kako importovati, osnovne informacije ?
---------------------------------------

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

Procedura importa šifrarnika robe
---------------------------------
Sada kada imamo spreman roba.csv fajl, te nakon što smo učitali csv i map u importer
treba da uzmemo podatke, putem pgAdmin-a, sljedećih tabela:

* uom (jedinice mjere)
* classcode (klase artikala)
* prodcat (kategorije artikala)

pobliže objašnjeno ovdje [aktivnost #24852](http://redmine.bring.out.ba/issues/24825#note-36)
Te vrijednosti id polja treba da ubacimo u naš map fajl, upravo kako je objašnjeno na aktivnosti.

Prije importa treba da setujemo i poreze i to na način opisan u [aktivnosti #24856](http://redmine.bring.out.ba/issues/24856)

Tek kada su svi ovi uslovi zadovoljeni, možemo da počnemo sa procedurom importa.

Procedura importa je jako zahtjevna i traži dosta vremena, zato budite strpljivi :)
