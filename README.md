# ARSALAI Flächenradar

Bewertete Bestandsparkplätze für Deutschlandnetz-Schnellladeparks in 12 Suchräumen (Dortmund Ost, Duisburg, Oberhausen, Dorsten, Lünen, Herten, Schwerte, Lippstadt, Bergisch Gladbach, Bornheim, Lülsdorf, Würselen).

Die App ist eine einzelne HTML-Datei (`index.html`) mit eingebetteten Daten und läuft ohne Server-Logik. Status, Notizen, Wiedervorlagen und gesetzte Suchräume werden im Browser des jeweiligen Geräts gespeichert (Sicherung und Übertragung über „Pipeline“).

## Was die App kann

- 4.425 bewertete Parkflächen (Score 0 bis 100) mit Begründung je Fläche
- Deutschlandnetz-Check je Fläche: Größenklasse S/M/L/XL, Gastronomie und Sanitär in 250 m, amtliche Verkehrszahl, Autobahnanschluss, Schnelllader im Umkreis, Trafostation, Zugang
- Flurstücke (Gemarkung, Flur, Nummer, amtliche Größe, Nutzung) für die Top 80 je Suchraum
- Recherchierte Ansprechstellen (Ketten, Center, Städte, Stadtwerke) mit Prüfkennzeichen
- 2-km-Suchraumkreise per Klick auf die Karte, eigener Suchraum als Polygon
- Pipeline über alle Suchräume mit Wiedervorlage, Vergleich von bis zu 3 Flächen, Steckbrief als PDF, Direktlink je Fläche, Sortierung nach eigenem Standort
- Export als CSV (Excel) und Kurzliste

## Datenquellen

| Quelle | Inhalt | Stand |
|---|---|---|
| OpenStreetMap / Overture Maps | Parkflächen, Gebäude, Geschäfte, Gastronomie, Straßennetz | 21.10.2026 |
| Straßen.NRW Verkehrswerte | DTV (Kfz/Tag, Lkw) für B-, L- und K-Straßen | 31.03.2026 |
| Bundesnetzagentur Ladesäulenregister (CC BY 4.0) | Bestehende Ladeeinrichtungen mit Betreiber und Leistung | 30.09.2026 |
| ALKIS NRW (WFS vereinfacht, dl-de/zero-2.0) | Flurstücke ohne Eigentümerangaben | 27.10.2026 |
| Offizielle Websites der Unternehmen und Städte | Ansprechstellen | 27.10.2026 |

Die Bewertung ist automatisiert und ersetzt keine Prüfung vor Ort. Eigentümer stehen nicht in öffentlichen Karten; die App nennt den passenden Weg (Kette, Centerverwaltung, Kommune, Grundbuch).
