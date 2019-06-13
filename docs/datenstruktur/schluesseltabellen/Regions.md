#       Tabelle Regions



| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| ID           | I+  | -     | P        | -                                        |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Kuerzel      | A   | 20    | -        | -                                        |
| Schluessel   | A   | 10    | -        | -                                        |
| Bezeichnung  | A   | 100   | -        | -                                        |
| StatistikID  | A   | 16    | -        | -                                        |
| Land         | I   | -     | V        | Verweis auf Tabelle **Staaten**          |
| RegionTyp    | I   | -     | V        | Verweis auf Tabelle **RegionTypes**      |
| InternalCode | A   | 3     | -        | Interner Code<br/><br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |
| GueltigVon   | D   | -     | -        | -                                        |
| GueltigBis   | D   | -     | -        | -                                        |


