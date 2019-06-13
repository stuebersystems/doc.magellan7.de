# Tabelle Berufe


| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| ID           | I+  | -     | P        | -                                        |
| Kuerzel      | A   | 20    | -        | -                                        |
| Schluessel   | A   | 10    | -        | -                                        |
| BezeichnungM | A   | 240   | -        | Männliche Bezeichnung                    |
| BezeichnungW | A   | 240   | -        | Weibliche Bezeichnung                    |
| Fachrichtung | A   | 10    | V        | Verweis auf Tabelle **Fachrichtungen**   |
| Berufsfeld   | A   | 10    | V        | Verweis auf Tabelle **Berufsfelder**     |
| Kategorie    | S   | -     | -        | Mögliche Werte:  <br/>0 = Interne Schlüssel<br/>1 = Externe Schlüssel<br/>2 = Interne und Externe Schlüssel |
| StatistikID  | A   | 16    | -        | -                                        |
| GueltigVon   | D   | -     | -        | -                                        |
| GueltigBis   | D   | -     | -        | -                                        |

