#        Tabelle LehrerMedizinAkten



| Feldname     | Typ | Größe | Funktion | Bemerkung                         |
|--------------|-----|-------|----------|-----------------------------------|
| Mandant      | I   | -     | PV       | Verweis auf Tabelle **Mandanten** |
| ID           | I+  | -     | P        | -                                 |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA |
| Lehrer       | I   | -     | V        | Verweis auf Ansicht Lehrer        |
| Datum        | D   | -     | -        | -                                 |
| Behandlung   | M   | -     | -        | -                                 |
| Medikationen | M   | -     | -        | -                                 |
| Bemerkung    | M   | -     | -        | -                                 |


