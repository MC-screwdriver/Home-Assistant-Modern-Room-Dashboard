# Installation und erster Test

## Voraussetzungen

- Home Assistant
- Mushroom Cards über HACS
- card-mod über HACS
- ein Temperatur- und ein Luftfeuchtigkeitssensor

Nach einer erstmaligen Installation oder Aktualisierung der HACS-Frontend-Komponenten den Browser beziehungsweise die Home-Assistant-App vollständig neu laden.

## Empfohlener Schnelltest im bestehenden Dashboard

1. Das gewünschte Dashboard öffnen.
2. **Bearbeiten → Karte hinzufügen → Manuell** auswählen.
3. Den vollständigen Inhalt aus `cards/01_room_climate.yaml` einfügen.
4. Die beiden Platzhalter-Entitäten anhand von `ENTITY_MAPPING.md` ersetzen.
5. Speichern.

Diese Methode verändert nur eine einzelne Karte und ist deshalb für den ersten Test am sichersten.

## Separates YAML-Testdashboard

Die Datei `dashboard/test_dashboard.yaml` kann als eigenständiges YAML-Dashboard verwendet werden.
Dazu beispielsweise folgende Konfiguration in `configuration.yaml` ergänzen:

```yaml
lovelace:
  mode: storage
  dashboards:
    monk-test:
      mode: yaml
      title: Monk Test
      icon: mdi:view-dashboard-outline
      show_in_sidebar: true
      filename: dashboards/monk-test.yaml
```

Anschließend:

1. Im Home-Assistant-Konfigurationsordner den Ordner `dashboards` anlegen.
2. `test_dashboard.yaml` dorthin kopieren und in `monk-test.yaml` umbenennen.
3. Die Platzhalter-Entitäten ersetzen.
4. Home Assistant neu starten.

## Zustandslogik

- **Grün / Optimal:** 20–24 °C und 40–60 %
- **Orange / Bitte beobachten:** 18–26 °C und 30–70 %, sofern nicht optimal
- **Rot / Handlungsbedarf:** außerhalb dieser Bereiche
- **Grau:** mindestens ein Sensor liefert keinen gültigen Wert

Diese Grenzwerte sind zunächst bewusst einfach gehalten. Sie werden erst nach dem Test auf Handy und Kiosk-Display angepasst.
