#       Tabelle Groups


| Name        | Typ | Größe | Funkt. | Bemerkung                         |
|-------------|-----|-------|--------|-----------------------------------|
| Mandant     | I   | -     | PV     | Verweis auf Tabelle **Mandanten** |
| ID          | I+  | -     | P      | -                                 |
| EnbreaID    | A   | 24    | -      | Externer Identifikator aus ENBREA |
| GUID        | A   | 32    | -      | -                                 |
| Code        | A   | 20    | -      | -                                 |
| Name        | A   | 300   | -      | -                                 |
| Type        | A   | 100   | -      | -                                 |
| Street      | A   | 100   | -      | -                                 |
| State       | A   | 3     | -      | -                                 |
| ZipCode     | A   | 10    | -      | -                                 |
| City        | A   | 100   | -      | -                                 |
| Telephone   | A   | 30    | -      | -                                 |
| Telefax     | A   | 30    | -      | -                                 |
| Email       | A   | 100   | -      | -                                 |
| Internet    | A   | 100   | -      | -                                 |
| Bank        | I   | -     | V      | Verweis auf Tabelle **Banken**    |
| IBAN        | A   | 28    | -      | -                                 |
| Logo        | B   | -     | -      | -                                 |
| Description | M   | -     | -      | -                                 |

