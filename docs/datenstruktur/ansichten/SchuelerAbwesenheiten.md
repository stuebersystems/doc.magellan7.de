# View SchuelerAbwesenheiten

Grundlage ist die Tabelle:
* [SchuelerFehlzeiten](https://doc.magellan7-datenstruktur.stueber.de/tabellen/SchuelerFehlzeiten/).


| Feldname  | Typ | Größe | Funktion | Bemerkung                                |
|-----------|-----|-------|----------|------------------------------------------|
| Mandant   | I   | -     | -        | -                                        |
| ID        | I   | -     | -        | -                                        |
| Schueler  | I   | -     | -        | -                                        |
| Von       | D   | -     | -        | -                                        |
| Bis       | D   | -     | -        | -                                        |
| Grund     | A   | 20    | V        | Verweis auf Tabelle **SchuelerFehlgruende** |
| Bemerkung | M   | -     | -        | -                                        |

