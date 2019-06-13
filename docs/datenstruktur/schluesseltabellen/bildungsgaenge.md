# Tabelle Bildungsgaenge


| Feldname        | Typ | Größe | Funktion | Bemerkung                                |
|-----------------|-----|-------|----------|------------------------------------------|
| ID              | I+  | -     | P        | -                                        |
| Kuerzel         | A   | 20    | -        | -                                        |
| Schluessel      | A   | 10    | -        | -                                        |
| Bezeichnung     | A   | 240   | -        | -                                        |
| Bezeichnung2    | A   | 240   | -        | -                                        |
| Berufsfeld      | A   | 10    | V        | Verweis auf Tabelle **Berufsfelder**     |
| Schulform       | A   | 10    | V        | Verweis auf Tabelle **Schulformen**      |
| Organisation    | A   | 10    | V        | Verweis auf Tabelle **Organisationen**   |
| Unterrichtsform | A   | 10    | V        | Verweis auf Tabelle **Unterrichtsformen** |
| Fachrichtung    | A   | 10    | V        | Verweis auf Tabelle **Fachrichtungen**   |
| Schwerpunkt     | A   | 10    | V        | Verweis auf Tabelle **Schwerpunkte**     |
| Schwerpunkt2    | A   | 10    | V        | Verweis auf Tabelle **Schwerpunkte**     |
| Klassenstufe    | A   | 10    | V        | Verweis auf Tabelle **Klassenstufen**    |
| Dauer           | N   | -     | -        | -                                        |
| Kategorie       | S   | -     | -        | **Mögliche Werte:**  <br/>0 = Interne Schlüssel<br/>1 = Externe Schlüssel<br/>2 = Interne und Externe Schlüssel |
| StatistikID     | A   | 16    | -        | -                                        |
| GueltigVon      | D   | -     | -        | -                                        |
| GueltigBis      | D   | -     | -        | -                                        |


