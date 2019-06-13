# Tabelle Adressen




| Feldname                  | Typ | Größe | Funktion | Bemerkung                                |
|---------------------------|-----|-------|----------|------------------------------------------|
| Mandant                   | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                        | I+  | -     | P        | -                                        |
| Kuerzel                   | A   | 15    | -        | -                                        |
| Name1                     | A   | 50    | -        | -                                        |
| Name2                     | A   | 50    | -        | -                                        |
| Name3                     | A   | 50    | -        | -                                        |
| Strasse                   | A   | 100   | -        | -                                        |
| Land                      | A   | 3     | -        | -                                        |
| PLZ                       | A   | 5     | -        | -                                        |
| Ort                       | A   | 100   | -        | -                                        |
| Ortsteil                  | A   | 100   | -        | -                                        |
| Telefon                   | A   | 30    | -        | -                                        |
| Telefax                   | A   | 30    | -        | -                                        |
| Internet                  | A   | 100   | -        | -                                        |
| Email                     | A   | 100   | -        | -                                        |
| Kategorie                 | A   | 20    | V        | Verweis auf Tabelle **Adressenkategorien** |
| EmpfaengerUnfallbericht   | A   | 1     | -        | Mögliche Werte:<br/>J = Ja<br/>N = Nein  |
| EmpfaengerUnfallberichtNr | A   | 30    | -        | Nummer des Unfallversicherungsträgers    |
| Bemerkung                 | M   | -     | -        | -                                        |



