#       Tabelle RegionTypes




| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| ID           | I+  | -     | P        | -                                        |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Kuerzel      | A   | 20    | -        | -                                        |
| Schluessel   | A   | 10    | -        | -                                        |
| Bezeichnung  | A   | 100   | -        | -                                        |
| Position     | S   | -     | -        | -                                        |
| Land         | I   | -     | V        | Verweis auf Tabelle **Staaten**          |
| StatistikID  | A   | 16    | -        | -                                        |
| InternalCode | A   | 3     | -        | Interner Code<br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |
| GueltigVon   | D   | -     | -        | -                                        |
| GueltigBis   | D   | -     | -        | -                                        |


