# Entity Mapping

Vor dem Testen diese Platzhalter durch die eigenen Home-Assistant-Entitäten ersetzen.

| Platzhalter | Bedeutung | Beispiel für echte Entität |
|---|---|---|
| `sensor.livingroom_temperature` | Temperatur im Wohnzimmer | `sensor.wohnzimmer_temperatur` |
| `sensor.livingroom_humidity` | Luftfeuchtigkeit im Wohnzimmer | `sensor.wohnzimmer_luftfeuchtigkeit` |

## Austausch

In Home Assistant unter **Entwicklerwerkzeuge → Zustände** nach den echten Entitäten suchen.
Danach beide Platzhalter in der YAML-Datei vollständig ersetzen.

Die Temperatur muss als numerischer Wert in °C und die Luftfeuchtigkeit als numerischer Wert in % vorliegen.
