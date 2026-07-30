# Home Assistant Modern Room Dashboard

## Version 0.1.0 – Raumklima

Der erste kleine, direkt testbare Baustein des modularen Raum-Dashboards.

> Ein Smart Home soll Ruhe vermitteln – nicht Aufmerksamkeit verlangen.

## Enthalten

- eine einheitliche Raumklima-Karte
- dynamische Bewertung von Temperatur und Luftfeuchtigkeit
- feste Farben für Optimal, Beobachten, Warnung und fehlende Daten
- Platzhalter-Entitäten mit Mapping-Tabelle
- vollständiges YAML-Testdashboard
- Installationsanleitung

## Designregeln dieser Version

- klare Hierarchie
- keine unnötigen Animationen
- zurückhaltende Kartenfläche
- feste Rundung und Abstände
- Status wird durch Text, Icon und Farbe gleichzeitig erkennbar
- gleiche Funktion wird später in jedem Raum gleich dargestellt

## Dateien

```text
cards/01_room_climate.yaml       Einzelkarte zum Einfügen im UI-Editor
dashboard/test_dashboard.yaml    Eigenständiges Testdashboard
docs/ENTITY_MAPPING.md           Zuordnung der Platzhalter
docs/INSTALLATION.md             Installation und Testablauf
CHANGELOG.md                      Versionsverlauf
```

## Nächster Schritt

Erst nach dem Test auf Smartphone und Raspberry-Pi-Kiosk werden Maße, Schrift und Zustandsgrenzen festgeschrieben. Danach folgt der Türzustand als zweiter Baustein.
