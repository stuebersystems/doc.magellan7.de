#       Tabelle MedienAusleiher




| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| Mandant      | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID           | I+  | -     | P        | -                                        |
| SVID         | I   | -     | V        | Verweis auf Tabelle **Schueler**, **Lehrer** oder **Personen** |
| SVTyp        | S   | -     | -        | Mögliche Werte:<br/>0 = Person<br/>1 = Lehrer<br/>2 = Schüler |
| Barcode      | A   | 20    | -        | -                                        |
| BarcodePrint | A   | 20    | -        | -                                        |
| Vorname      | A   | 30    | -        | -                                        |
| Nachname     | A   | 50    | -        | -                                        |
| Anrede       | A   | 1     | -        | Mögliche Werte:<br/>0 = Frau<br/>1 = Herr<br/>2 = Frau Dr.<br/>3 = Herr Dr.<br/>4 = Frau Prof.<br/>5 = Herr Prof.<br/>6 = Frau Prof. Dr.<br/>7 = HerrProf. Dr.<br/>:  = Ms.<br/>; = Mrs.<br/> < = Mr. |
| Geschlecht   | A   | 1     | -        | Mögliche Werte:<br/>W = Weiblich<br/>M  = Männlich |
| Geburtsdatum | D   | -     | -        | -                                        |
| Strasse      | A   | 100   | -        | -                                        |
| Land         | A   | 3     | -        | -                                        |
| PLZ          | A   | 5     | -        | -                                        |
| Ort          | A   | 100   | -        | -                                        |
| Telefon      | A   | 30    | -        | -                                        |
| Telefax      | A   | 30    | -        | -                                        |
| Mobil        | A   | 30    | -        | -                                        |
| Email        | A   | 100   | -        | -                                        |
| Passfoto     | A   | 30    | -        | -                                        |
| Status       | S   | -     | -        | Mögliche Werte:<br/>0 = Nicht Aktiv<br/>1 = Aktiv |
| GueltigVon   | D   | -     | -        | -                                        |
| GueltigBis   | D   | -     | -        | -                                        |

