# Tabelle TransportationStops



| Feldname | Typ | Größe | Funktion | Bemerkung                                |
|----------|-----|-------|----------|------------------------------------------|
| Mandant  | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID       | I+  | -     | P        | -                                        |
| EnbreaID | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Route    | I   | -     | V        | Verweis auf Tabelle **TransportationRoutes** |
| Code     | A   | 20    | -        | -                                        |
| Name     | A   | 100   | -        | -                                        |
| Distance | N   | -     | -        | -                                        |
| Duration | N   | -     | -        | -                                        |


