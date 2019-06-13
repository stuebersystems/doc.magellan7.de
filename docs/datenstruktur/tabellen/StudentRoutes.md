# Tabelle StudentRoutes


| Feldname    | Typ | Größe | Funktion | Bemerkung                                |
|-------------|-----|-------|----------|------------------------------------------|
| Mandant     | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID          | I+  | -     | P        | -                                        |
| EnbreaID    | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Line        | I   | -     | V        | Verweis auf Tabelle **TransportationLines** |
| Method      | I   | -     | V        | Verweis auf Tabelle **TransportationMethods** |
| Origin      | I   | -     | V        | Verweis auf Tabelle **TransportationStops** |
| Destination | I   | -     | V        | Verweis auf Tabelle **TransportationStops** |
| Distance    | N   | -     | -        | -                                        |
| Duration    | N   | -     | -        | -                                        |


