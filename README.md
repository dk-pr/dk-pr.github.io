# Pilzradar Rathenow

Fund-Chance für Steinpilz, Marone und Pfifferling im Havelland – für jede einzelne Waldfläche.

**Live: https://dk-pr.github.io/**

## Was die Karte zeigt

Einen experimentellen Bedingungsindex: wie günstig Wetter, Boden und Baumbestand gerade
für eine bestimmte Pilzart sind. Er sagt nicht, ob dort etwas steht.
Bestimme jeden Pilz selbst und iss nichts, was du nicht sicher kennst.

## Daten

- **Waldflächen, Schutzgebiete, Ortsnamen:** OpenStreetMap, Lizenz ODbL, geladen über Overpass.
  2631 Flächen der Kernregion liegen vorgerechnet in `pilzradar-waldflaechen.js`,
  Umrisse für die Darstellung vereinfacht. Außerhalb wird live nachgeladen.
- **Baumart (Laub-/Nadelanteil):** OSM-Tags wo vorhanden, sonst Copernicus Land Monitoring
  Service, HRL Forest Type 2012, © European Union / EEA. Deckt 98,4 % der Waldfläche ab.
- **Wetter und Bodendaten:** Open-Meteo, CC BY 4.0.
- **Kartenhintergrund:** basemap.de / BKG, OpenTopoMap, Esri.

## Technik

Statische Seite, kein Server, kein Build. `index.html` und `pilzradar-waldflaechen.js`
müssen im selben Ordner liegen. Karte mit Leaflet, Geometrien als Encoded Polylines,
nachgeladene Bereiche landen in IndexedDB.
