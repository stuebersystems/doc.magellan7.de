#     Tabelle Mandanten



| Feldname                | Typ | Größe | Funktion | Bemerkung                                |
|-------------------------|-----|-------|----------|------------------------------------------|
| ID                      | I+  | -     | P        | -                                        |
| Kuerzel                 | A   | 20    | -        | -                                        |
| Name1                   | A   | 100   | -        | -                                        |
| Name2                   | A   | 100   | -        | -                                        |
| Name3                   | A   | 100   | -        | -                                        |
| Strasse                 | A   | 100   | -        | -                                        |
| Land                    | A   | 3     | -        | -                                        |
| PLZ                     | A   | 5     | -        | -                                        |
| Ort                     | A   | 100   | -        | -                                        |
| Ortsteil                | A   | 100   | -        | -                                        |
| Gemeinde                | A   | -     | V        | Verweis auf Tabelle **Gemeinden**        |
| Telefon                 | A   | 30    | -        | -                                        |
| Telefax                 | A   | 30    | -        | -                                        |
| EMail                   | A   | 40    | -        | -                                        |
| Internet                | A   | 40    | -        | -                                        |
| Hauptstelle             | I   | -     | V        | Verweis auf Tabelle **Mandanten**        |
| Aussenstelle            | A   | 3     | -        | -                                        |
| Schulart                | A   | -     | V        | Verweis auf Tabelle **Schularten**       |
| Kategorie               | A   | -     | V        | Verweis auf Tabelle **Mandantenkategorien** |
| Betreuungsform          | A   | -     | V        | Verweis auf Tabelle **Betreuungsformen** |
| Schultraeger            | A   | -     | V        | Verweis auf Tabelle **Schultraeger**     |
| Schulstatus             | A   | -     | V        | Verweis auf Tabelle **Schulstati**       |
| Schulnummer             | A   | 12    | -        | -                                        |
| Schulleiter             | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Stellvertreter          | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Adresse1                | I   | -     | V        | Verweis auf Tabelle **Adressen**         |
| Adresse1Art             | S   | -     | -        | Mögliche Werte:<br/>0 = Schulträger<br/>1 = Schulamt<br/>2 = Ministerium |
| Adresse2                | I   | -     | V        | Verweis auf Tabelle **Adressen**         |
| Adresse2Art             | S   | -     | -        | Mögliche Werte:<br/>0 = Schulträger<br/>1 = Schulamt<br/>2 = Ministerium |
| Adresse3                | I   | -     | V        | Verweis auf Tabelle **Adressen**         |
| Adresse3Art             | S   | -     | -        | Mögliche Werte:<br/>0 = Schulträger<br/>1 = Schulamt<br/>2 = Ministerium |
| Bank                    | I   | -     | V        | Verweis auf Tabelle **Banken**           |
| Bankkonto               | A   | -     | 20       | -                                        |
| MinPersonalNr           | I   | -     | -        | -                                        |
| MaxPersonalNr           | I   | -     | -        | -                                        |
| Bemerkung               | M   | -     | -        | -                                        |
| MerkmalA1               | A   | -     | V        | Verweis auf Tabelle **MandantenMerkmale** |
| MerkmalA2               | A   | -     | V        | Verweis auf Tabelle **MandantenMerkmale** |
| MerkmalA3               | A   | -     | V        | Verweis auf Tabelle **MandantenMerkmale** |
| MerkmalA4               | A   | -     | V        | Verweis auf Tabelle **MandantenMerkmale** |
| MerkmalA5               | A   | -     | V        | Verweis auf Tabelle **MandantenMerkmale** |
| MerkmalA6               | A   | -     | V        | Verweis auf Tabelle **MandantenMerkmale** |
| daVinciDatei            | A   | 300   | -        | daVinci-Datei des Mandanten              |
| KBLetzteSynchronisation | DT  | -     | -        | Letzte Synchronisation mit dem Klassenbuch |
| Logo                    | M   | -     | -        | -                                        |
| Logo2                   | M   | -     | -        | -                                        |
| Rechtsstatus            | S   | -     | -        | Mögliche Werte:<br/>0 = öffentlich<br/>1 = Privat |
| PruefungsNr             | A   | 20    | -        | -                                        |
| EnbreaID                | A   | 24    | -        | Externer Identifikator aus ENBREA        |


