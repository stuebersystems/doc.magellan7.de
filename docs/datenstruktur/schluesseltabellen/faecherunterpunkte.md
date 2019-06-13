#  Tabelle FaecherUnterpunkte


| Feldname      | Typ | Größe | Funktion | Bemerkung                             |
|---------------|-----|-------|----------|---------------------------------------|
| Mandant       | I   | -     | PV       | Verweis auf Tabelle **Mandanten**     |
| ID            | I+  | -     | P        | -                                     |
| Kuerzel       | A   | 20    | -        | -                                     |
| Schluessel    | A   | 10    | -        | -                                     |
| Thema         | I   | -     | V        | Verweis auf Tabelle **FaecherThemen** |
| FUBezeichnung | A   | 200   | -        | -                                     |
| Position      | S   | -     | -        | -                                     |
| StatistikID   | A   | 16    | -        | -                                     |
| GueltigBVon   | D   | -     | -        | -                                     |
| GueltigBis    | D   | -     | -        | -                                     |


