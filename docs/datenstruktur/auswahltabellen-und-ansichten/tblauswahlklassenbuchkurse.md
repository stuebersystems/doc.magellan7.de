#  Tabelle tblAuswahlKlassenbuchKurse


| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Benutzer       | A   | 20    | -        | -                                        |
| Mandant        | I   | -     | V        | Verweis auf Tabelle **Mandanten**        |
| Zeitraum       | I   | -     | V        | Verweis auf Tabelle **Zeitraeume**       |
| Klasse         | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| Fach           | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Unterrichtsart | A   | 10    | V        | Verweis auf Tabelle **Unterrichtsarten** |
| Fachstatus     | A   | 10    | V        | Verweis auf Tabelle **Fachstati**        |
| KursNR         | S   | -     | -        | -                                        |
| VonDatum       | D   | -     | -        | -                                        |
| BisDatum       | D   | -     | -        | -                                        |


