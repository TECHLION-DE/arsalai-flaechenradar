# ARSALAI Flächenradar

Bewertete Bestandsparkplätze für Deutschlandnetz-Schnellladeparks in 12 Suchräumen (Dortmund Ost, Duisburg, Oberhausen, Dorsten, Lünen, Herten, Schwerte, Lippstadt, Bergisch Gladbach, Bornheim, Lülsdorf, Würselen). Die 12 Suchräume sind die offiziellen 2-km-Kreise des Deutschlandnetzes (Region 6 West, Los 3), Mittelpunkte aus der Deutschlandnetz-Ebene des FlächenTOOLs der Nationalen Leitstelle Ladeinfrastruktur.

Die App ist eine einzelne HTML-Datei (`index.html`) mit eingebetteten Daten und läuft ohne Server-Logik. Status, Notizen, Wiedervorlagen und zusätzliche Suchräume werden im Browser des jeweiligen Geräts gespeichert (Sicherung und Übertragung über „Pipeline“).

`allego/index.html` ist dieselbe App als Konzept-Variante im Look des Betreibers (Demo der Agentur TECHLION, kein Produkt der Allego GmbH).

## Deutschland-Module

- **Ausfahrten DE:** alle Autobahn- und Schnellstraßen-Anschlussstellen, bewertet nach Verkehr (BASt-Dauerzählstellen 2024, aus den Stundenrohdaten berechnet), Schnellladern ab 150 kW im Umkreis und geeigneten Parkflächen mit Tankstelle, Gastro oder Markt direkt an der Ausfahrt.
- **Märkte DE:** Supermärkte, Discounter und Center mit Bedarfsindex aus Einwohnern in 2 km (Zensus 2022, 1-km-Raster), Verkehr der nächsten gezählten Straße, Einzelhandelsumfeld, Parkplatzgröße und bestehenden Schnellladern in 1 km.
- Die Daten liegen unter `data/` (JSON für die App, CSV-Vollexporte `ausfahrten_de.csv` und `maerkte_de.csv`) und werden von der App nachgeladen.

## Was die App kann

- 4.585 bewertete Parkflächen (Score 0 bis 100) mit Begründung je Fläche, Abzug für Flächen außerhalb des 2-km-Suchraums
- Deutschlandnetz-Check je Fläche: Lage im Suchraum, Ladepunkte-Vorgabe (4 oder 8) gegen Fläche und Stellplätze, Gastronomie und Sanitär in 250 m, amtliche Verkehrszahl, Autobahnanschluss, Schnelllader im Umkreis, Trafostation, Zugang
- Pachtrahmen je Ladepunktzahl für das Eigentümergespräch
- Flurstücke (Gemarkung, Flur, Nummer, amtliche Größe, Nutzung) für die Top 80 je Suchraum
- Recherchierte Ansprechstellen (Ketten, Center, Städte, Stadtwerke, Netzbetreiber) mit Prüfkennzeichen
- Im FlächenTOOL angebotene Flächen innerhalb der Suchräume
- Pipeline über alle Suchräume mit Wiedervorlage, Vergleich von bis zu 3 Flächen, Steckbrief als PDF, Direktlink je Fläche, Sortierung nach eigenem Standort
- Export als CSV (Excel) und Kurzliste

## Datenquellen

| Quelle | Inhalt | Stand |
|---|---|---|
| OpenStreetMap / Overture Maps | Parkflächen, Gebäude, Geschäfte, Gastronomie, Straßennetz (bundesweit für die Deutschland-Module) | 21.10.2026 |
| BASt Dauerzählstellen (Rohdaten) | DTV 2024 an 1.086 Autobahn- und 700 Bundesstraßen-Zählstellen | Jahr 2024 |
| Zensus 2022 (Destatis) | Einwohner im 1-km-Raster | 15.05.2022 |
| FlächenTOOL (NOW GmbH), Ebene Deutschlandnetz | Suchraum-Mittelpunkte, Kategorie, Los | 28.10.2026 |
| Straßen.NRW Verkehrswerte | DTV (Kfz/Tag, Lkw) für B-, L- und K-Straßen | 31.03.2026 |
| Bundesnetzagentur Ladesäulenregister (CC BY 4.0) | Bestehende Ladeeinrichtungen mit Betreiber und Leistung | 30.09.2026 |
| ALKIS NRW (WFS vereinfacht, dl-de/zero-2.0) | Flurstücke ohne Eigentümerangaben | 28.10.2026 |
| Offizielle Websites der Unternehmen, Städte und Netzbetreiber | Ansprechstellen | 27.10.2026 |

Die Bewertung ist automatisiert und ersetzt keine Prüfung vor Ort. Eigentümer stehen nicht in öffentlichen Karten; die App nennt den passenden Weg (Kette, Centerverwaltung, Kommune, Grundbuch).
