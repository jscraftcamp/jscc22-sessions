# covid-karte.de

Tilman stellt vor, wie er die Site [covid-karte.de](https://covid-karte.de/) ohne Framework gebaut hat.
Source Code auf github: [t-animal/covid-karte](https://github.com/t-animal/covid-karte)

RKI Covid-19

Das RKI selbst veröffentlich die Daten mit [Arcgis](https://experience.arcgis.com/experience/478220a4c454480e823b17327b2bf1d4),
und verwenden nicht die API die sie selber zur Verfügung stellen.

Die ganze Seite besteht aus einer großen HTML-Datei,
und einem Ordner map-data mit den geojson und topojson Dateien.

Observables + Obeserver selbst implementiert, siehe modules/observers.ts

Kein JSX, also alles selber gebaut mit `createElement` und `.textContent`.
Alternative wäre [Template-Tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/template) gewesen.

snowpack verwendet, hat funktioniert, aber ist jetzt end of live wird durch [vitejs](https://vitejs.dev/) ersetzt.

Größter Pain Point: Data Loader selber schreiben, der cached. mit der [cache-api](https://developer.mozilla.org/en-US/docs/Web/API/Cache).

Was nicht mehr funktioniert hätte: routing.

Dependencies: Leaflet für die Karte.

Überraschende Erkenntnis: Landkreise ändern sich im Beobacthungszeitrum: Eisenach wurde eingemeindet.




