# Seeufer-Analyse: Wie verbaut sind Schweizer Seen?
## Einleitung
Im Sommer 2018 veröffentlichte [BLICK eine Serie an Artikel über Schweizer Seeufer](https://www.blick.ch/storytelling/2018/seeanalyse/). Im Januar 2024 erweiterte [das Hochparterre-Magazin diese Analyse](https://www.hochparterre.ch/nachrichten/landschaftsarchitektur/ufer-fuer-alle). Dazu wurden die Seen gemäss ihrem Verbauungsgrad kategorisiert. Diese Daten werden hier zur Verfügung gestellt.

## Lizenz
Die Daten dürfen für eigene Analysen und Publikationen mit Quellenhinweis weiterverwendet werden.

## Zitierung
* `Hochparterre und Blick`
* `...wie Daten vom Hochparterre und BLICK zeigen.`

## Datenherkunft
* **Hochparterre**, 2024 für die Seen Genfersee, Neuenburgersee, Luganersee und Lago Maggiore sowie die Überarbeitung der bereits kategorisierten Seen.
* **Blick**, 2018 für Zürichsee, Zugersee, Thunersee, Sempachersee, Vierwaldstädtersee, Hallwilersee, Bodensee, Bielersee und Baldeggersee. Diese wurden 2018 erstellt und 2024 überarbeitet.

## Daten
* [Shapefiles](Daten/shapefiles). Die Kategorie ist im Property `cat` erfasst
* [CSV](Daten/csv). Prozentuale Verteilung
* [SVGs](Daten/svg). Bilder der Seen als SVG.

## Kategorien
### fa (Free accessible, frei zugänglich)
Frei zugänglich im Sinne von: Es steht kein Gebäude oder privates/abgesperrtes Grundstück zwischen Seeufer und Weg. Das Seeufer muss aber nicht hindernisfrei erreichbar sein. So zählen etwa auch Strassen direkt am See als frei zugänglich, solange diese einen Gehweg für Fussgänger aufweisen. Als frei zugänglich zählen ebenfalls Wiesen, wenn sie für das Überqueren vorgesehen sind, wie zum Beispiel bei Parks.

Farbkodierung in SVG: ![#f03c15](https://placehold.co/15x15/28c23f/28c23f.png) `#28c23f`

### pa (Payed accessible, bezahlter Eintritt)
Dies sind Seeabschnitte, die einen öffentlichen Charakter aufweisen, aber trotzdem nur oder zweitweise gegen Eintritt begehbar sind. Typischerweise Badis. Restaurants mit Seeterasse zählen nicht zu dieser Kategorie und gelten als privat (pp).

Farbkodierung in SVG: ![#f03c15](https://placehold.co/15x15/e9a23d/e9a23d.png) `#e9a23d`

### ps (Public Streets & Train Tracks, Strassen und Eisenbahnlinien)
Strassen ohne Gehweg direkt am See ebenso wie Bahngeleise fallen in diese Kategorie. Das Ufer ist eigentlich frei zugänglich, allerdings nur mit Zug oder Fahrzeug.

Farbkodierung in SVG: ![#f03c15](https://placehold.co/15x15/ecffc5/ecffc5.png) `#ecffc5`

### pp (Private Property, Privat)
Kein Seezugang. Dies sind vor allem Privatgrundstücke.

Farbkodierung in SVG: ![#f03c15](https://placehold.co/15x15/ec4243/ec4243.png) `#ec4243`

### ff (Forrest, farming, moors, Wald, Landwirtschaft, Moore)
In diese Kategorie fallen unverbaute Grundstücke, die aber nicht über einen Weg zugänglich sind. Zum Beispei Wälder, Ackerbau oder Moore. Nicht dazu zählen Landwirtschaftsflächen, wenn sie abgesperrt sind, wie etwa Weinberge.

Farbkodierung in SVG: ![#f03c15](https://placehold.co/15x15/dbffe4/dbffe4.png) `#dbffe4`

### wr (Water, River, Wasser, Fluss)
Flussmündungen und Deltas.

Farbkodierung in SVG: ![#f03c15](https://placehold.co/15x15/71e0f8/71e0f8.png) `#71e0f8`

## Methode
Als Basis dient die Uferküste gemäss Open Street Map. Diese wurden unverändert übernommen. Betrachtet wurden nur zusammenhängende Abschnitte, Inseln wurden entfernt.

Für die Kategorisierung wurden folgende Quellen verwendet:
* [Strava Heatmap](https://www.strava.com/heatmap), um nicht eingezeichnete Wege und Zugänge zu erkennen
* [Google Street View](https://www.google.ch/maps/), um Zugange zu überprüfen
* [Katasterdaten](https://www.cadastre.ch/de/home.html) der Gemeinden (als WMS vom Bund), um Grundstücksgrenzen zu erkennen.
* [Open Street Map](https://www.openstreetmap.org/) für Wege
* [Wanderkarte des Bundes](https://map.geo.admin.ch/?lang=de&topic=ech&bgLayer=ch.swisstopo.pixelkarte-farbe&layers=ch.swisstopo.swisstlm3d-wanderwege&layers_opacity=0.8) für Uferwege
* [Bing Maps](https://bing.com/maps) für Birdview-Aufnahmen

## WMS-Services
* Wanderwege: [https://wms.geo.admin.ch/?VERSION=1.3.0](https://wms.geo.admin.ch/?VERSION=1.3.0), `Wanderwege`
* Katasterdaten: [https://wmts.geo.admin.ch/EPSG/3857/1.0.0/WMTSCapabilities.xml?lang=de](https://wmts.geo.admin.ch/EPSG/3857/1.0.0/WMTSCapabilities.xml?lang=de), `CadastralWebMap`
* SwissTopo: [https://wmts.geo.admin.ch/EPSG/3857/1.0.0/WMTSCapabilities.xml?lang=de](https://wmts.geo.admin.ch/EPSG/3857/1.0.0/WMTSCapabilities.xml?lang=de), `Karte swissTLM (farbig)`

##  Artikel
### 2024
* [Ufer für alle, Hochparterre](https://www.hochparterre.ch/nachrichten/landschaftsarchitektur/ufer-fuer-alle)
* [Nur ein Schweizer Ufer ist noch mehr in privater Hand als das des Zürichsees, Watson](https://www.watson.ch/schweiz/z%C3%BCrich/379474434-uferwege-so-zugaenglich-oder-eben-nicht-sind-die-schweizer-seeufer)

### 2018
* [So verbaut sind unsere Seen, Blick](https://www.blick.ch/storytelling/2018/seeanalyse/)
* [Behörden kuschen vor den Reichen, Blick](https://www.blick.ch/interaktiv/darum-sind-viele-seeufer-nicht-zugaenglich-behoerden-kuschen-vor-den-reichen-id8802484.html)
* [Im Namen Gottes für freie Ufer, Blick](https://www.blick.ch/interaktiv/victor-von-wartburg-kaempft-fuer-offene-ufer-im-namen-gottes-fuer-freie-ufer-id8808163.html)
* [Das sagen die verbautesten Gemeinden, Blick](https://www.blick.ch/news/politik/warum-gibt-es-hier-kaum-oeffentliche-ufer-das-sagen-die-verbautesten-gemeinden-id8810289.html)
* [So regeln es die Deutschen und Österreicher, Blick](https://www.blick.ch/news/ausland/uferzugang-am-bodensee-so-regeln-es-die-deutschen-und-oesterreicher-id8756864.html)

## Kontakt
simon.huwiler [a] nzz.ch