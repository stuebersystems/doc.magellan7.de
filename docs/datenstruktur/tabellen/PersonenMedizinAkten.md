#        Tabelle PersonenMedizinAkten


| Feldname     | Typ | Größe | Funktion | Bemerkung                         |
|--------------|-----|-------|----------|-----------------------------------|
| Mandant      | I   | -     | PV       | Verweis auf Tabelle **Mandanten** |
| ID           | I+  | -     | P        | -                                 |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA |
| Person       | I   | -     | V        | Verweis auf Tabelle **Personen**  |
| Datum        | D   | -     | -        | -                                 |
| Behandlung   | M   | -     | -        | -                                 |
| Medikationen | M   | -     | -        | -                                 |
| Bemerkung    | M   | -     | -        | -                                 |


