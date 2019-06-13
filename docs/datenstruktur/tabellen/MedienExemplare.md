#       Tabelle MedienExemplare


| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Mandant        | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| Katalog        | I   | -     | PV       | Verweis auf Tabelle **MedienKataloge**   |
| ID             | I+  | -     | P        | -                                        |
| Medium         | I   | -     | V        | Verweis auf Tabelle **Medien**           |
| Barcode        | A   | 20    | -        | -                                        |
| BarcodePrint   | A   | 20    | -        | -                                        |
| BarcodeExtern  | A   | 20    | -        | Externer Barcode für importierte Mediendaten |
| Signatur       | A   | 50    | -        | -                                        |
| Zustand        | I   | -     | V        | Verweis auf Tabelle **MedienZustaende**  |
| Status         | S   | -     | -        | Mögliche Werte:<br/>0 = Frei<br/>1 = Vorgemerkt<br/>2 = Verliehen |
| Bestandsstatus | S   | -     | -        | Mögliche Werte:<br/>0 = Altbestand<br/>1 = Neukauf<br/>2  Spende<br/>3 = Schenkung<br/>4 = Dauerverleih<br/>5 = Dauerleihgabe |
| Eingangsdatum  | D   | -     | -        | -                                        |
| Ausgangsdatum  | D   | -     | -        | -                                        |
| Betrag         | N   | -     | -        | -                                        |
| Waehrung       | A   | -     | V        | Verweis auf Tabelle **Waehrungen**       |
| Lieferant      | I   | -     | V        | Verweis auf Tabelle **Lieferanten**      |
| Standort       | I   | -     | V        | Verweis auf Tabelle **Standorte**        |
| Bemerkung      | M   | -     | -        | -                                        |


