# Tabelle StudentTransportation




| Feldname      | Typ | Größe | Funktion | Bemerkung                                |
|---------------|-----|-------|----------|------------------------------------------|
| Mandant       | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID            | I+  | -     | P        | -                                        |
| EnbreaID      | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Student       | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| InboundRoute  | I   | -     | V        | Verweis auf Tabelle **TransportationRoutes** |
| OutboundRoute | I   | -     | V        | Verweis auf Tabelle **TransportationRoutes** |


