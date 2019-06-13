# Tabelle Entschuldigungsgruende


| Feldname    | Typ | Größe | Funktion | Bemerkung                                |
|-------------|-----|-------|----------|------------------------------------------|
| ID          | I+  | -     | P        | -                                        |
| Kuerzel     | A   | 20    | -        | -                                        |
| Schluessel  | A   | 10    | -        | -                                        |
| Bezeichnung | A   | 100   | -        | -                                        |
| Kategorie   | A   | 10    | V        | Verweis auf Tabelle **Entscheidungskategorien** |
| StatistikID | A   | 16    | -        | -                                        |
| GueltigVon  | D   | -     | -        | -                                        |
| GueltigBis  | D   | -     | -        | -                                        |

