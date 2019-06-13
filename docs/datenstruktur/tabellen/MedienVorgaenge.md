# Tabelle MedienVorgaenge


| Feldname         | Typ | Größe | Funktion | Bemerkung                                |
|------------------|-----|-------|----------|------------------------------------------|
| Mandant          | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID               | I+  | -     | P        | -                                        |
| Exemplar         | I   | -     | V        | Verweis auf Tabelle **MedienExemplare**  |
| Ausleiher        | I   | -     | V        | Verweis auf Tabelle **MedienAusleiher**  |
| AusleiheVon      | D   | -     | -        | -                                        |
| AusleiheBis      | D   | -     | -        | -                                        |
| RueckgabeAm      | D   | -     | -        | -                                        |
| Mahnstufe        | S   | -     | -        | -                                        |
| Mahngebuehr      | N   | -     | -        | -                                        |
| LetzteMahnungAm  | D   | -     | -        | -                                        |
| MahnungBezahltAm | D   | -     | -        | -                                        |
| Verlaengern      | S   | -     | -        | -                                        |
| Status           | S   | -     | -        | Mögliche Werte:<br/>0 = Offen<br/>1 = Gemahnt<br/>2 = Abgeschlossen |


