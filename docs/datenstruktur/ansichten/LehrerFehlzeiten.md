# View LehrerFehlzeiten

Grundlage ist die Tabelle [tblLehrer](https://doc.magellan7.stueber.de/datenstruktur/tabellen/tblLehrerFehlzeiten/).



| Feldname        | Typ | Größe | Funktion | Bemerkung                                |
|-----------------|-----|-------|----------|------------------------------------------|
| Mandant         | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID              | I+  | -     | P        | -                                        |
| Lehrer          | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Von             | D   | -     | -        | -                                        |
| Bis             | D   | -     | -        | -                                        |
| Stunden         | N   | -     | -        | -                                        |
| Unterrichtstage | N   | -     | -        | -                                        |
| Fehltage        | N   | -     | -        | -                                        |
| Grund           | A   | 10    | V        | Verweis auf Tabelle **LehrerFehlgruende** |
| Voranfrage      | A   | 1     | -        | -                                        |
| Bemerkung       | M   | -     | -        | -                                        |


