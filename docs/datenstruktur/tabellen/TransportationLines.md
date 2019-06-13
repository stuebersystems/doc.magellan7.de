# Tabelle TransportationLines



| Feldname      | Typ | Größe | Funktion | Bemerkung                                |
|---------------|-----|-------|----------|------------------------------------------|
| Mandant       | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID            | I+  | -     | P        | -                                        |
| EnbreaID      | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| InboundRoute  | I   | -     | V        | Verweis auf Tabelle **TransportationRoutes** |
| OutboundRoute | I   | -     | V        | Verweis auf Tabelle **TransportationRoutes** |
| Operator      | I   | -     | V        | Verweis auf Tabelle **Adressen**         |
| Code          | A   | 20    | -        | -                                        |
| Name          | A   | 100   | -        | -                                        |


