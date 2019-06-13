#  Tabelle Faecher


| Feldname        | Typ | Größe | Funktion | Bemerkung                                |
|-----------------|-----|-------|----------|------------------------------------------|
| Mandant         | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID              | I+  | -     | P        | -                                        |
| Kuerzel         | A   | 20    | -        | -                                        |
| Schluessel      | A   | 10    | -        | -                                        |
| Bezeichnung     | A   | 200   | -        | -                                        |
| Kategorie       | S   | -     | -        | Mögliche Werte:   <br/><br/>0   = Fremdsprache<br/>1   = Religion/Ethik<br/>2   = Deutsch<br/>3   = Mathematik<br/>4   = Kunst<br/>5   = Musik<br/>6   = Sport<br/>9   = Informatik<br/>10 = Philosophie<br/>11 = Geschichte<br/>12 = Physik<br/>13 = Chemie<br/>14 = Biologie<br/>15 = Erdkunde<br/>16 = Sozialkunde<br/>17 = Wirtschaft<br/>18 = Politik<br/>19 = Darstellendes Spiel<br/>20 = Evangelische Religion<br/>21 = Katholische Religion<br/>26 = Technik<br/>27  = Pädagogik<br/>28 = Sport-Theorie<br/>29 = BWL/RW<br/>30 = BWL/VWL<br/>31 = VWL<br/>32 = Seminar<br/>33 = Gesundheit<br/>34 = Psychologie<br/>35 = Recht |
| Aufgabenbereich | S   | -     | -        | Mögliche Werte:<br/><br/>0 = sprachl.-lit.-künstlerisch<br/>1 = gesellschaftswiss.<br/>2 = mathem.-nat.-technisch<br/>3 = Religion<br/>4 = Sport |
| Gruppe          | A   | 10    | -        | Verweis auf Tabelle Fachgruppen          |
| KeinAbgleich    | A   | 1     | -        | Kein Abgleich mit daVinci                |
| Zeugnismerkmal  | A   | 10    | -        | -                                        |
| StatistikID     | A   | 16    | -        | -                                        |
| GueltigBVon     | D   | -     | -        | -                                        |
| GueltigBis      | D   | -     | -        | -                                        |

