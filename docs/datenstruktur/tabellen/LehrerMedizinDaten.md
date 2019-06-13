#       Tabelle LehrerMedizinDaten



| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| Mandant      | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID           | I+  | -     | P        | -                                        |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Lehrer       | I   | -     | V        | Verweis auf Ansicht Lehrer               |
| Kategorie    | I   | -     | V        | Verweis auf Tabelle **MedizinKategorien** |
| Art          | I   | -     | V        | Verweis auf Tabelle **MedizinArten**     |
| Medikationen | M   | -     | -        | -                                        |
| Medikamente  | M   | -     | -        | -                                        |
| Bemerkung1   | M   | -     | -        | -                                        |
| Bemerkung2   | M   | -     | -        | -                                        |
| AblaufAm     | D   | -     | -        | -                                        |


