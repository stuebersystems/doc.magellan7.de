# Tabelle Betriebe



| Feldname   | Typ | Größe | Funktion | Bemerkung                                |
|------------|-----|-------|----------|------------------------------------------|
| Mandant    | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID         | I+  | -     | P        | -                                        |
| EnbreaID   | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| GUID       | A   | 32    | -        | -                                        |
| IDIntern   | I   | -     | -        | -                                        |
| IDExtern   | I   | -     | -        | -                                        |
| GUIDExtern | A   | 36    | -        | -                                        |
| Kuerzel    | A   | 15    | -        | -                                        |
| Name1      | A   | 50    | -        | -                                        |
| Name2      | A   | 50    | -        | -                                        |
| Strasse    | A   | 100   | -        | -                                        |
| Land       | A   | 3     | -        | -                                        |
| PLZ        | A   | 5     | -        | -                                        |
| Ort        | A   | 100   | -        | -                                        |
| Ortsteil   | A   | 100   | -        | -                                        |
| Gemeinde   | A   | 8     | V        | Verweis auf Tabelle **Gemeinden**        |
| Telefon    | A   | 30    | -        | -                                        |
| Telefax    | A   | 30    | -        | -                                        |
| Internet   | A   | 100   | -        | -                                        |
| Email      | A   | 100   | -        | -                                        |
| Branche    | A   | -     | V        | Verweis auf Tabelle **Branchen**         |
| Kammer     | A   | -     | V        | Verweis auf Tabelle **Kammern**          |
| Arbeitsamt | A   | -     | V        | Verweis auf Tabelle **Arbeitsaemter**    |
| Sponsor    | A   | -     | V        | Verweis auf Tabelle **Sponsoren**        |
| Status     | S   | -     | -        | Mögliche Werte:<br/>0 = Inaktiv<br/>1 = Aktiv |
| Bemerkung  | M   | -     | -        | -                                        |
| SYNC       | S   | -     | -        | -                                        |





