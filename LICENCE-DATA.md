# Data ve hře a jejich licence

## OpenStreetMap (ODbL 1.0)
Soubory ve složce `data/` (dlaždice, sítě chodců a ulic, scénáře) jsou odvozená databáze vytvořená z dat OpenStreetMap.
Mapa © přispěvatelé OpenStreetMap, https://www.openstreetmap.org/copyright

Tato odvozená databáze je zpřístupněna pod licencí Open Database License 1.0 (ODbL): https://opendatacommons.org/licenses/odbl/1-0/
Změny proti zdroji: výřez oblasti Prahy, převod souřadnic do metrů (S-JTSK posunuté na počátek u Staroměstského náměstí), zjednodušení geometrie, odhady výšek budov bez údaje a šířek silnic bez údaje (seznam odhadů je v dokumentaci projektu).

Hra samotná (kód a vykreslený obraz) je dílo vytvořené z databáze.

## IPR Praha (CC BY 4.0)
Tvary střech (`data/roof`, `roofpack`) jsou plochy střech 3D modelu budov IPR Praha (BD3) ořezané na půdorysy OSM. Výšky budov (pole `e`, `rh`, `s`, `ir` v dlaždicích) jsou spočítané z 3D modelu budov IPR Praha (BD3), z rastru relativních výšek budov a z vrstvy Podlažnosti; polohu 31 budov pipeline posunula podle DTM Prahy (ZPS).
Terén (`tn`, `t0` v dlaždicích, `ter.json`) a základy budov (`z0`) jsou z 3D modelu terénu IPR Praha (TER): výšky v uzlech mřížky 3,9–15,6 m spočítané z trojúhelníků modelu, na hranách dlaždic sjednocené, v decimetrech nad 190 m n. m.
Opěrné zdi (druh 6 v `ploty.json`) jsou z vrstvy IPR Praha „Opěrné zdi“ (TSK); výšky plošin a mostů nad podjezdy z modelu povrchu IPR (DSM 1 m), pilíře z Digitální technické mapy (ZPS).
Zdroj dat: data base © IPR Praha, https://www.geoportalpraha.cz, licence Creative Commons Uveďte původ 4.0 (https://creativecommons.org/licenses/by/4.0/deed.cs).
Změny: výška římsy a hřebene odvozená z ploch střech a základových desek uvnitř půdorysu OSM, zaokrouhlení na decimetry, převod souřadnic. Budovy bez dat IPR mají výšku z OSM nebo odhad (zdroj je u každé budovy v poli `s`).

## DTM Prahy – veřejná data ZPS (IPR Praha)
Plochy ulic v `data/ulice` (vozovka `road`/`rs`, chodník `side`, ostrůvky `isl`, tramvajový pás `tram`, nástupiště `nas`, parkoviště `park`, cyklostezka `cyc`, obrubníky `kb`) jsou z Digitální technické mapy Prahy, veřejná data základní prostorové situace (správce IPR Praha, Portál DMVS), přes převod souřadnic, ořez na dlaždice, zjednodušení (0,25 m) a zaokrouhlení na decimetry. Obrubník = hranice chodníku nebo ostrůvku s vozovkou; snížení u přechodů je odhad. Kde DTM data nemá, je vozovka z OSM (obálka podle šířky).
Zdroj dat: DTM hl. m. Prahy © IPR Praha. Licence u sady na portálu uvedena není; uvádíme původ jako u ostatních dat IPR (CC BY 4.0).

## Úseky parkování v zónách placeného stání, Uliční úseky TSK (IPR Praha, CC BY 4.0)
Parkovací stání (`pk` v `data/ulice`) jsou rozmístěná podle ploch a počtu stání z vrstvy „Úseky parkování v zónách placeného stání“ (druh a natočení stání jsou odhad, obsazenost 60 % je odhad). Třída komunikace TSK u hran sítě aut (`net/car.json`, pole `tk`) je z vrstvy „Uliční úseky TSK včetně zatřídění komunikací“. Zdroj dat: data base © IPR Praha, CC BY 4.0.

## Jízdní řády PID (ROPID, CC BY 4.0)
`data/mhd.json` (linky, zastávky, trasy a časy spojů tramvají, autobusů, trolejbusů a lanovky v oblasti hry) je odvozen z otevřených dat PID GTFS © ROPID, licence CC BY 4.0. Změny: výřez na oblast hry, sloučení spojů do vzorů, zjednodušení tras na 0,5 m, typové dny (pracovní den, sobota, neděle) z platnosti 20. 11.–3. 12. 2026; stání ve stanicích je odhad.

## Kašny a fontány (IPR Praha, CC BY 4.0)
Kašny, které v OSM nejsou, doplněné z vrstvy IPR „Kašny a fontány“ (`data/prvky.json`); ostatní prvky (sochy, lavičky, koše, podniky a vchody) jsou z OpenStreetMap (ODbL), viz výše.

## Další zdroje
Jakmile hra začne používat další zdroje (Wikidata – CC0; Open-Meteo – CC BY 4.0), budou uvedené tady i ve hře.

Zahrádky restaurací (`data/zahradky.json`): které podniky mají zahrádku, je z OpenStreetMap (`outdoor_seating`, ODbL); poloha a velikost zahrádky jsou odhad hry.

## Postavy (zatím jen za `?postavy2=1`)
Tělo postavy (`data/postavy/telo*.bin`) je vytvořené v MPFB 2 (MakeHuman Plugin For Blender); výstup MPFB je CC0. Pohyby (`data/postavy/klipy.bin`) jsou přepočtené animace z Adobe Mixamo (použití ve hře podle podmínek Mixamo; původní soubory FBX se nešíří).

## Písmo
Písma Barlow a Barlow Condensed (složka `fonts/`) © Jeremy Tribby, licence SIL Open Font License 1.1 (https://openfontlicense.org), soubory z balíčku @fontsource.
